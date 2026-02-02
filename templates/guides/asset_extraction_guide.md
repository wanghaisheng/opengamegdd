# 从 GDD 提取资产并判定格式的说明（视频 / 序列帧 / 图片）

## 1. 目标与范围
- 目标：建立从 GDD 文档快速提取资产需求的流程，并为每条资产选择合适的格式（video / image_sequence / image）。
- 范围：适用于过场、展示动画、背景循环、UI/2D 动画、特效素材与静态视觉。

## 2. 输入来源（GDD 章节）
- 3 游戏概述：产品定位、关键视觉风格（影响视频 vs 序列帧的比例）。
- 4 玩法与机制：战斗/经济/成长的表现需求（特效、UI 动效、结算画面）。
- 5 故事与角色：过场、角色登场、名牌展示等镜头。
- 6 关卡：关卡演出、奖励揭示、环境特效。
- 7 界面：主界面/活动页/结算/抽卡揭示等 UI 场景与分镜表。
- 9 技术：媒体编码档位、性能与包体预算、格式校验。
- 10 美术：风格规范、格式维度、命名与管线。
- 13 附录：资产清单与路线图。

## 3. 提取流程（五步法）
- 步骤 1：逐章扫描，标注“可见元素”（角色、背景、道具、FX、UI、音频）与“关键镜头/界面状态”。
- 步骤 2：以场景为单位拆分“分镜/界面状态”，记录 Intro → Build-up → Reveal → Outro。
- 步骤 3：为每个元素确定用途与展示方式（长时段展示/透明叠加/UI动效/纹理）。
- 步骤 4：按决策规则选择格式（video / image_sequence / image），并记录元数据与依赖。
- 步骤 5：写入资产清单（CSV/MD），进入资产路线图。

## 4. 格式决策规则
- 适合 video（视频）：
  - 过场/展示：统一高质、时长 3–30 秒、交互少或无交互。
  - 背景循环：主界面/活动页循环背景，需稳定表现与低计算。
  - 复杂合成：多图层调色/后期，运行时不易复现。
  - 要求：多档分辨率/码率、容器与编码规范、文件大小控制。
- 适合 image_sequence（序列帧）：
  - 透明背景动画：火焰、能量轨迹、魔法阵、UI 高光/微动效。
  - 引擎内混合：与粒子、后处理叠加，逐帧可控。
  - 插值/节奏需精细控制：帧级别节奏、可变速播放。
  - 要求：统一分辨率与帧率、命名 SEQ_*_0001.png、Alpha 正常、内存预算。
- 适合 image（图片）：
  - 静态视觉：UI 图标、海报、插图、静态背景帧。
  - 纹理贴图：PBR 通道（_D/_N/_R/_AO/_M 或 _RMA）。
  - 要求：尺寸与压缩规范、色彩空间一致、通道命名正确。

## 5. 映射参考（常见场景 → 格式）
- 过场/剧情片段：video
- 英雄/皮肤展示：video 或 image_sequence（透明特效层）
- 抽卡揭示：video（预渲染）或 image_sequence（引擎合成）
- 主界面背景：video（循环）或 image（静帧）
- 活动页动效：image_sequence（UI 叠加）或 sprite_sheet（大量轻量动效）
- 战斗 FX：image_sequence（需要透明与逐帧控制）
- 结算界面：image（静态）+ image_sequence（名牌/粒子）

## 6. 写入资产清单（建议字段）
- 使用 [asset_list_template.csv](GDDMarkdownTemplate/templates/asset_list_template.csv) 或 [asset_list_template.md](GDDMarkdownTemplate/templates/asset_list_template.md)。
- 关键字段：ID、类别、格式（Format）、名称、描述、数量、变体、规格、分辨率、FPS/时长（如适用）、平台、优先级、依赖、负责人、来源（GDD页/分镜帧）、文件路径、状态、标签。
- 元数据：使用 [asset_metadata_schema.json](GDDMarkdownTemplate/templates/asset_metadata_schema.json)（format 枚举）。

## 7. 校验与编码（技术协同）
- 视频编码档位：参考 [video_encoding_profiles.csv](GDDMarkdownTemplate/templates/video_encoding_profiles.csv)。
- 格式校验：参见技术章节 9.13（媒体编码与格式校验）。
- 序列帧检查：命名连续、分辨率一致、Alpha 正常；可生成 GIF/低码率视频作为评审预览。

## 8. 示例（抽卡揭示片段）
- 分镜：Entry（能量聚合）→ Reveal（英雄现身）→ Nameplate → Loop → Exit。
- 资产拆分：
  - 背景循环：video（1080p@60fps，Mid 档）
  - 英雄出现光效：image_sequence（透明 PNG，SEQ_GachaReveal_FX_0001.png）
  - 名牌与星级：image_sequence 或 sprite_sheet（UI 叠加）
  - 音频：BGM + SFX（音量曲线与循环点）
- 清单条目：类别=Reveal、格式=video/image_sequence，来源=4/6/7 章与分镜帧编号。

