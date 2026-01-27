# API驱动分镜视频生产指南（2–8 秒，文本提示词 + 输入文件）

## 1. 能力与约束
- 输出：2–8 秒视频（video，MP4/WebM），支持多档分辨率/FPS/码率。
- 输入：文本提示词（Prompt）、图片（角色/精灵/背景，PNG/JPG/WebP）、参考视频（动作/特效）。
- 用途：Cutscene、Reveal/Showcase、Background Loop、Promo、Tutorial 等短片。

## 2. 输入规范
- 文本提示词结构（推荐分层）：
  - 场景摘要：一句话描述核心事件（发生了什么）。
  - 风格与关键词：色彩/光影/材质/情绪（如 史诗、金色粒子、体积光）。
  - 分镜大纲：S01 Intro → S02 Build-up → S03 Key → S04 Detail → S05 Outro。
  - 图层指令：BG（背景）、CHAR（角色）、FX（特效）、UI（名牌/字幕）、AUDIO（BGM/SFX/VO）。
  - 情绪曲线与节奏：蓄力→揭示→高光→收束；节奏快/中/慢。
- 图片输入：
  - 角色/精灵：PNG（含 Alpha），命名 T_hero_body.png / SPR_UI_atlas.png；分辨率与素材授权明确。
  - 背景：BG_city_night.jpg（1920x1080 或竖屏 1080x1920）；色彩空间 sRGB。
- 参考视频：
  - 动作参考：stick_motion_ref.mp4（1–4 秒），用于镜头节奏与动作对拍。
  - 特效参考：fx_glow_ref.webm（透明或黑底），用于高光节点参考。
- 元数据字段（建议）：
  - subject、category（reveal/bg_loop 等）、platforms、resolution、fps、durationSeconds、encodingProfile。

## 3. 分镜映射与镜头设计
- 原则：视觉递进（远→全→中→近→特）、叙事锚定（核心事件）、分层表达（空间/主体/细节/氛围）。
- 时间分配（示例，总 6 秒）：
  - S01 Intro 1.5s：定场景与基调（稳镜/大全景）
  - S02 Build-up 1.5s：主体入场与蓄势（中景/缓推）
  - S03 Key 1.5s：关键揭示（近景/快速推/摇）
  - S04 Detail 0.8s：特写细节确认
  - S05 Outro 0.7s：收束与转场
- Shot 字段建议：
  - Shot/Time、Scene/State、Camera/Movement、Focus
  - Characters/Actions、Background/Lighting、FX Layers、UI Overlay
  - Audio（BGM/SFX/VO）、Text/Localization、Transition
  - Performance（编码档位/分辨率/FX 层预算）、Analytics（enter/exit/skip/CTA）

## 4. 图层绑定与素材映射
- 背景：BG_layer ← 背景图片（或参考视频静帧/循环）
- 角色：CHAR_layer ← 人物立绘/精灵；动作节奏参考 stick_motion_ref.mp4
- 特效：FX_layer ← 序列帧（SEQ_FX_*_0001.png）或由 API 内置生成；高光节点对齐 FX 参考视频
- UI：UI_layer ← 名牌/字幕/稀有度星星（sprite_sheet 或 image_sequence）
- 音频：AUDIO ← BGM/SFX/VO，提示词中标注入场/峰值/淡出节点

## 5. 生成参数与编码
- 分辨率/FPS：1080p@60（Mid 档），竖屏 1080x1920；可选 720p@30（Low）、1440p/4K@60（High）
- 编码：MP4/H.264 或 H.265；WebM/VP9（Web）
- 音频：48kHz/160 kbps，淡入淡出与循环点
- 命名：VID_API_[Type]_[Subject]_[Profile]_v001.mp4

## 6. 质量与校验
- 画面：无明显伪影/断帧；调色与光影符合风格关键词
- 动作与节奏：与参考视频对拍；分镜时间控制在 2–8 秒
- 特效：Alpha 正常、混合模式无黑/白边；高光节点与音效同步
- UI/文案：清晰易读、语言变体正确
- 性能：各档位解码流畅；文件大小控制

## 7. 迭代流程（人机协作）
- 第 1 版：提交提示词与素材 → 生成预览 → 评审（镜头/节奏/氛围）
- 修订点：微调分镜时间、镜头运动、FX 强度、调色与音频节点
- 版本命名：v001/v002…；保留差异说明（变更点列表）
- 通过标准：满足风格与信息传达、性能达标、埋点完整

## 8. 集成与埋点
- enterEventId / exitEventId、interactiveStartTimestamp
- 指标：观看时长、跳过率、CTA 点击率、加载失败率

## 9. 请求示例（自然语言 + 文件清单）

文本提示（摘要）：

“英雄登场短片，城市夜景氛围。Intro 稳镜开场，Build-up 粒子蓄势，Key 近景揭示家族徽记与名牌，Detail 特写星芒与徽记纹理，Outro 淡出回到主界面。色彩冷→暖过渡，体积光与能量轨迹为主。BGM 峰值在揭示，SFX 提示音与高光同步。”

文件清单：
- BG_city_night.jpg（1920x1080）
- T_hero_body.png（含 Alpha）
- SPR_UI_nameplate_atlas.png + index.json
- stick_motion_ref.mp4（动作节奏参考）
- fx_glow_ref.webm（高光参考）

参数：
- resolution=1920x1080，fps=60，durationSeconds=6，encodingProfile=Mid_H264_1080p60

