# 试玩广告（Playable Ad）预渲染视频指南（可点击串联分镜）

## 1. 目标与范围
- 目标：用预渲染视频片段与可点击热点（Hotspot）在 15–45 秒内模拟核心玩法，支持“点击选择/继续”的交互，串联不同分镜，实现轻量可玩广告体验。
- 范围：Intro/选择节点/结果片段/Outro/CTA；支持多语言字幕与UI Overlay；无需代码开发游戏逻辑，仅制作视频分段与热点路由。

## 2. 体验结构与路由
- 段落（Segment）：S01 Intro → S02 选择 A（攻击）/S03 选择 B（闪避） → S04 结果 A（奖励）/S05 结果 B（失败） → S06 Outro/CTA。
- 每段为独立视频文件，段尾或段中出现热点，引导下一段；至少包含 2 次点击交互。
- 路由规则：热点点击 → 跳转目标 SegmentId；未点击超时 → 默认路由（如继续播放或跳转“失败/教程”）。

## 3. 分镜与镜头设计（自然语言 + 表格）
- 每镜头要素：核心事件一句、景别/运动、主体动作、背景/灯光/FX、UI/文案、本地化、音频节点、过渡、性能预算、热点（定义/出现时机/停留/目标路由）。
- 分镜表字段（建议）：
| Shot | 时间 | 景别/运动 | 主体动作 | 背景 | 灯光 | FX/动画 | UI/HUD | 音频 | 文案 | 过渡 | 热点定义 | 跳转目标 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
- 示例描述：
  - S01（Intro，大全景，稳镜）：定场景与题材；字幕“选择你的动作”；2 秒后显示热点“攻击/闪避”
  - S02（选择 A，中景，缓推）：演示攻击；热点“继续连击”与“改为闪避”；点击后分别进入 S04/S03
  - S03（选择 B，近景，快速推）：演示闪避；热点“反击”进入 S04；未点击超时进入 S05
  - S04（结果 A，特写）：奖励结算与浮字；字幕“获得装备”；热点“继续体验”或“预约”
  - S05（结果 B，中景）：失败提示与教程字幕；热点“再试一次”回 S02 或“查看攻略”
  - S06（Outro，中/大全景，淡出）：回到主界面背景循环；CTA“继续/预约/下载”

## 4. 互动热点（Hotspot）与路由定义
- 热点字段建议：hotspotId、shape（rect/circle）、position/size（百分比坐标）、appearTime、disappearTime、label、targetSegmentId、defaultRoute、analyticsEventId。
- 出现时机：镜头稳定段或信息明确段；停留 1.5–3s；避免与字幕/UI重叠。
- 命名：HSP_[Segment]_[Action]_v001；路由：RT_[From]_[To]_v001。
- 指标埋点：点击率、停留时长、未点击率、首次点击时间、完成率。

## 5. 视频素材与拼装（Layering & Compositing）
- 段视频（必需）：VID_PLAY_[SegmentId]_[Lang]_[Profile]_v001.mp4
- 背景层：静帧或循环视频；统一调色。
- 主体层：角色/对象动作参考；节奏与热点出现对齐。
- FX 层：image_sequence 或 sprite_sheet；控制透明填充率与混合层数。
- UI 层：HUD/提示/热点可视化（按钮/高亮区域）；九宫格与切图规范。
- 音频层：BGM 情绪曲线；关键节点 SFX；VO 与字幕同步。

## 6. 编码与交付
- 分辨率/FPS：1080p@60（Mid），可提供 720p@30（Low）、1440p/4K@60（High）；参考编码档位：[video_encoding_profiles.csv](file:///e:/workspace/GDDMarkdownTemplate/docs/templates/video_encoding_profiles.csv)
- 容器与编码：MP4/H.264 或 H.265；Web 场景可用 WebM。
- 命名：VID_PLAY_[SegmentId]_[Lang]_[Profile]_v001.mp4；热点/路由表可用 CSV/JSON（随工程交付）。
- 交付包：分段视频、工程/合成文件、分层素材、字幕/本地化、热点路由表、元数据 JSON（format=video）。

## 7. 质量与评审指标
- 信息清晰：热点出现时机明确；文案与 UI 指示直观；镜头稳定段放置热点。
- 交互节奏：点击–反馈–跳转顺畅；默认路由容错合理。
- 情绪曲线：Intro→选择→结果→CTA；避免冗长与割裂。
- 市场验证：热点点击率、完成率、首次点击时间、CTA 点击率、视频流畅度与解码兼容性。

## 8. 迭代流程
- v001：完成基本段落与热点；评审收集交互与节奏意见
- v002：优化镜头稳定度、热点尺寸与位置；微调字幕/音频节点
- v003：本地化与多分辨率；导出正式档位与交付包

## 9. 示例路由（文本版）
- S01 → 选择A=攻击→ S02 → 继续连击→ S04 → CTA（预约/下载）
- S01 → 选择B=闪避→ S03 → 未点击超时→ S05（失败/教程）→ 再试一次→ 回 S02
- 全局默认：任一段未点击 → 默认路由指向“教程/继续”

## 10. 参考与模板
- 方法论：见 [universal_storyboard_method.md](file:///e:/workspace/GDDMarkdownTemplate/docs/templates/guides/universal_storyboard_method.md)
- MVP 游玩视频：见 [mvp_gameplay_video_guide.md](file:///e:/workspace/GDDMarkdownTemplate/docs/templates/guides/mvp_gameplay_video_guide.md)
- 视频分镜说明：见 [storyboard_for_video_assets.md](file:///e:/workspace/GDDMarkdownTemplate/docs/templates/guides/storyboard_for_video_assets.md)
- 视频制作指南：见 [video_asset_guide.md](file:///e:/workspace/GDDMarkdownTemplate/docs/templates/guides/video_asset_guide.md)
