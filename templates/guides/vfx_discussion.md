# 特效格式讨论与资产映射（武器 / 技能 / 皮肤）

## 1. 目标与范围
- 统一“武器特效、技能特效、皮肤特效”的资产载体选型与制作规范。
- 明确不同表现诉求下的最佳格式：fx_particle、image_sequence、sprite_sheet、3d_model+shader/material、video。
- 适配过场/展示/界面与实时战斗场景；支持多平台的性能与降级策略。

## 2. 格式与载体选择
- fx_particle：引擎粒子系统（Niagara/ParticleSystem 等）。优势是实时、可交互、与状态/参数联动；适用于火焰、爆炸、能量轨迹、体积光、天气。
- image_sequence：透明逐帧图层（PNG/TGA，Alpha）。可精细控制、与后处理/粒子混合；适用于过场/展示、UI 叠加的发光/符印/字幕动效。
- sprite_sheet：2D 精灵表，适合大量轻量动效与 UI 装饰；Atlas 管理、索引清晰、占用小。
- 3d_model + shader/material：实体类或体积类视觉，如能量刃、武器光带、弹道网格、扭曲/流动材质；与骨骼/动作强耦合。
- video：预渲染展示（MP4/WebM），不参与交互；用于 Cutscene、背景循环、Promo；透明层可用 image_sequence 叠加。说明：image_sequence 非 video（不同载体与用途）。

参考：
- 视频分镜说明：[storyboard_for_video_assets.md](GDDMarkdownTemplate/templates/guides/storyboard_for_video_assets.md)
- 序列帧指南：[image_sequence_guide.md](GDDMarkdownTemplate/templates/guides/image_sequence_guide.md)
- 粒子/特效生产：[fx_particle_production_guide.md](GDDMarkdownTemplate/templates/guides/fx_particle_production_guide.md)
- 通用分镜方法：[universal_storyboard_method.md](GDDMarkdownTemplate/templates/guides/universal_storyboard_method.md)

## 3. 武器特效映射（示例）
- 枪口火焰/剑光边缘高光：fx_particle（Additive/AlphaBlend）；低端机改为 sprite_sheet。
- 弹道轨迹/能量刃：3d_model+shader（Trail/Ribbon/Flow）或 fx_particle Mesh；远距离合并/关闭细枝。
- 命中火花/碎片：fx_particle + image_sequence 叠加近景细节；控制透明填充率与发射器峰值。
- 武器入场/检视展示：video（中近景 S02–S04）+ image_sequence 透明层；参见视频分镜 S01–S05 递进。

## 4. 技能特效映射（示例）
- 施放提示/蓄力环：fx_particle（环形/径向发射）+ 低频光影；UI 叠加使用 sprite_sheet。
- 投射物/范围技能：3d_model+shader（扭曲/折射/流动）+ fx_particle（次发射器）；远距离降级为 image_sequence。
- 命中/持续效果（DOT/AOE）：fx_particle（GPU 发射器）+ LOD 切换；视频用于展示版或教程片段。
- 终结/关键时刻（Key Moment）：近景高光与字幕同步，image_sequence 细节层叠加；参见 S03 框架。

## 5. 皮肤特效映射（示例）
- 入场展示：video（1080p@60，Mid 档）+ image_sequence 透明 FX；支持多语言字幕与 UI Overlay。
- 站立/移动常驻特效：fx_particle（低开销，距离关闭/合并）；材质轻度流动/发光。
- 攻击/技能替换特效：fx_particle + 3d_model+shader；遵循相同性能预算，确保与原技一致节奏。
- UI 装饰/名牌/按钮动效：sprite_sheet 或 image_sequence（透明）；统一 Atlas 与索引。

## 6. 选型建议与性能策略
- 半透明填充率：控制屏幕覆盖与层数，避免多层半透明叠加造成过度开销。
- 发射器数量与寿命：平台分档；峰值控制与时间线节奏化；远距离关闭高频细节。
- LOD 与距离策略：近远两到三级；远距离合并/关闭子发射器或替换为 image_sequence。
- 后处理预算：Bloom/Glow/DOF 等按平台档位；低端机关闭或降低强度。
- 混合模式：Additive/AlphaBlend/Multiply 按表现选择；与背景/灯光协调，避免过曝。

## 7. 命名与交付规范
- 命名建议：
  - 粒子/特效：FX_[Category]_[Subject]_v001
  - 序列帧：SEQ_FX_[Subject]_0001.png
  - 精灵表：SPR_UI_[Overlay]_atlas_v001.png
  - 视频：VID_[Scene]_[KeyEvent]_v001.mp4
  - 材质/着色器：MAT_[Effect]_[Subject]_v001 / SHD_[Technique]_[Subject]_v001
- 交付清单：工程资源、纹理/序列帧、预览视频/GIF、性能报告、元数据（format=fx_particle/image_sequence/sprite_sheet/3d_model/shader/material/video）。
- 元数据与清单：见 [asset_list_template.csv](GDDMarkdownTemplate/templates/asset_list_template.csv)、[asset_metadata_schema.json](GDDMarkdownTemplate/templates/asset_metadata_schema.json)、[video_asset_metadata_schema.json](GDDMarkdownTemplate/templates/video_asset_metadata_schema.json)。

## 8. 与分镜/视频集成
- 视频资产：按 S01–S05（Intro/Build-up/Key/Detail/Outro）递进；透明 FX 使用 image_sequence 叠加。
- 教程/展示：近景关键时刻（S03）用字幕/UI Overlay 强化信息；皮肤入场展示用 S02–S04 结构。
- 埋点与指标：enter/exit、观看时长、跳过率、CTA 点击率；参见分镜表与埋点建议。

## 9. 快速决策矩阵（简版）
- 实时互动（战斗/施放）优先：fx_particle + 3d_model+shader/material
- 展示/过场优先：video + image_sequence（透明层）
- UI 装饰优先：sprite_sheet 或 image_sequence
- 移动端与低端机：降级 image_sequence、关闭高频细节、减少半透明层
