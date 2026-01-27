# MVP 游玩预渲染视频生产指南（无需代码的模拟玩法体验）

## 1. 目标与范围
- 目标：在不开发代码的情况下，用现有或临时资产制作 30–90 秒的预渲染视频，模拟核心玩法循环（Core Loop）与关键体验，用于评审与市场验证。
- 范围：战斗/解谜/竞速/收集等核心片段；UI 叠加（HUD/提示/奖励）、音频（BGM/SFX/VO）、过场与转场。

## 2. 方法与结构（参考通用分镜方法论）
- 视觉递进：远→全→中→近→特；从环境到主体、从整体到局部。
- 叙事锚定：围绕“核心事件”（发生了什么）组织镜头与 UI 信息。
- 分层表达：空间（景别）/主体（角色/对象）/细节（动作/特写）/氛围（背景/光影/音频）。
- 推荐结构（示例分配，总 60 秒）：
  - Intro 8s：定场景与题材；标注玩法目标（HUD/文案）
  - Build-up 12s：进入玩法状态；演示基本操作与反馈
  - Core Loop 24s：2–3 个循环片段（操作→反馈→奖励/失败）
  - Progress 10s：展示成长/解锁（等级/货币/道具）
  - Outro 6s：收束与 CTA（继续/预约/反馈）

## 3. 输入资产与映射
- 背景：静帧图片或视频循环（BG_city_day.jpg / BG_forest_loop.mp4）
- 角色与动作：立绘/精灵；需要动作参考视频可用 stick_motion_ref.mp4
- 特效与动画：序列帧（SEQ_FX_*_0001.png）或精灵表 atlas（SPR_*）
- UI 叠加：HUD/图标/名牌/提示；使用 sprite_sheet 或 image_sequence
- 音频：BGM（情绪曲线）、SFX（操作/命中/奖励）、VO（旁白可选）
- 文案与本地化：关键提示与字幕，准备语言变体

## 4. 分镜与镜头设计（自然语言 + 表格）
- 每镜头要素：核心事件一句、景别/运动、主体动作、背景/灯光/FX、UI/文案、音频节点、过渡、性能预算（视频/序列帧/精灵表）、埋点（评审用）
- 分镜表字段（建议）：
| Shot | 时间 | 景别/运动 | 主体动作 | 背景 | 灯光 | FX/动画 | UI/HUD | 音频 | 文案 | 过渡 | 备注 |
|---|---|---|---|---|---|---|---|---|---|---|---|
- 示例描述：
  - S01（Intro，大全景，稳镜）：开阔战场环境与题材风格；字幕提示目标“击败 10 个敌人”
  - S02（Build-up，中景，缓推）：角色移动与基础攻击；HUD 显示生命/能量；SFX 击中反馈
  - S03（Core Loop 1，近景，快速推）：连击与闪避动作；FX 边缘高光；奖励浮字 UI
  - S04（Core Loop 2，近景/特写，切入）：技能释放与冷却提示；能量轨迹序列帧叠加
  - S05（Progress，中景）：获得装备/货币，面板弹出；BGM 略升；字幕提示解锁内容
  - S06（Outro，中/大全景，淡出）：回到主界面背景循环；CTA“继续/预约”

## 5. 资产拼装与合成（Layering & Compositing）
- 背景层：图片或视频循环；色彩与调色统一
- 主体层：角色/对象；动作节奏参考视频对拍
- FX 层：序列帧或精灵表；控制填充率与混合层数
- UI 层：HUD/提示/奖励浮字；九宫格与切图规范
- 音频层：BGM 情绪曲线；关键节点 SFX；VO 与字幕同步

## 6. 编码与交付
- 分辨率/FPS：1080p@60（Mid），可提供 720p@30（Low）、1440p/4K@60（High）
- 编码与容器：MP4/H.264 或 H.265；WebM（Web）
- 命名：VID_MVP_[Scene]_[Subject]_v001.mp4
- 交付：视频文件、工程/合成文件、分层素材、字幕/本地化、元数据 JSON（format=video）

## 7. 质量与评审指标
- 视觉与节奏：镜头与 UI 信息清晰；核心循环演示充分；情绪曲线合理
- 可信度：操作–反馈–奖励的因果链清晰（即使是模拟）
- 性能模拟：视频档位与解码流畅（评审端）；文件大小控制
- 市场验证：观看完成率、CTA 点击率、反馈问卷结果（如适用）

## 8. 迭代流程
- v001：基础循环与 UI 信息完整；评审收集具体意见
- v002：镜头运动与节奏优化；FX/调色与音频节点微调
- v003：本地化与多分辨率；导出最终档位与交付包

## 9. 参考与模板
- 分镜方法：见 [universal_storyboard_method.md](file:///e:/workspace/GDDMarkdownTemplate/docs/templates/guides/universal_storyboard_method.md)
- 视频分镜说明：见 [storyboard_for_video_assets.md](file:///e:/workspace/GDDMarkdownTemplate/docs/templates/guides/storyboard_for_video_assets.md)
- 视频制作指南：见 [video_asset_guide.md](file:///e:/workspace/GDDMarkdownTemplate/docs/templates/guides/video_asset_guide.md)
- 资产提取：见 [asset_extraction_guide.md](file:///e:/workspace/GDDMarkdownTemplate/docs/templates/guides/asset_extraction_guide.md)
