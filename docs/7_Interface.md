# 7. Interface（界面与交互系统）

> 定义所有玩家看得见、点得着的层：HUD、菜单、输入方式与反馈。

## 7.1 Visual System（可视化系统）

### 7.1.1 HUD（战斗 / 游玩界面）

- 核心信息展示（血量、能量、技能、资源、计时等）：
- 信息优先级与布局原则（视线中线附近、边缘信息等）：
- 动态反馈（受击、暴击、回血、状态变化等）：

### 7.1.2 Menus（菜单）

- 主菜单结构（功能分组：背包、角色、任务、活动、商店等）：
- 子菜单信息架构与层级深度控制：
- 状态标记（红点提示、NEW 标记、时间限制标记等）：

### 7.1.3 Rendering System（渲染相关）

- 视角（第一人称 / 第三人称 / 俯视）与镜头原则：
- 特效优先级与性能预算（低端机 / 高端机不同表现）：
- 画面设置对 UI 的影响（宽高比、自适应布局）：

### 7.1.4 Camera（摄像机）

- 跟随规则（距离、平滑、碰撞处理）：
- 特殊镜头（锁定敌人、过场镜头、交互时镜头切换）：
- 防晕动症的考虑（视角摆动限制、FOV 设置等）：

### 7.1.5 Lighting Models（光照）

- 整体光照风格（写实 / 卡通 / 高对比等）：
- 动态光源与昼夜变化（如适用）：
- 可交互光源（提示、指引）：

## 7.2 Control System（操作系统）

- 支持的输入设备（触屏、键鼠、手柄、重力感应等）：
- 基础操作映射（移动、攻击、交互、跳跃、技能等）：
- 高阶操作（连击、取消、宏操作限制等）：
- 新手阶段的手势引导和容错（减轻新手学习成本）：

## 7.3 Audio（音频）

- 音频风格与混音原则（语音优先 / BGM 优先 / SFX 优先等）：
- 不同场景的音频层级（战斗、城镇、野外、主界面）：
- 动态混音规则（重要事件时压低环境音等）：

## 7.4 Music（音乐）

- 主题曲与主旋律定位：
- 各区域 / 场景配乐的风格与节奏（探索、战斗、BOSS、休息）：
- 音乐与版本活动的联动（新活动主题曲等）：

## 7.5 Sound Effects（音效）

- 关键交互音效（点击、滑动、确认、取消）：
- 战斗音效（攻击、命中、技能、爆炸等）：
- 反馈层级（成功、失败、警告、奖励）：

## 7.6 Help System（帮助与引导）

- 新手引导形式（强引导步骤 / 自由探索提示）：
- 内嵌帮助（? 按钮、长按提示、图文说明等）：
- 版本更新后的功能教育（新功能高亮、教程关卡等）：

## 7.7 Accessibility & Localization（无障碍与多语言）

- 字体大小、对比度、色弱模式等设置：
- 关键语音内容的文字替代（字幕、文本记录）：
- 多语言本地化注意事项（字符串长度、文本方向、符号习惯等）：

## 7.8 Screen Storyboard Method（界面分镜说明方法）

- 目标：融合 UI 界面描述与电影分镜方法，统一记录界面状态、过渡与交互。
- 使用步骤：
  - 为关键界面建立“界面状态”（初始、悬停、点击、动画中、加载中、结束）。
  - 以镜头为单位记录焦点、UI 组件、交互、反馈、音视频、无障碍、本地化、过渡、性能预算与埋点。
- 字段建议：
  - Screen/State、Shot/Time、Camera/Focus、UI Components、Interaction/Gesture、Feedback（Visual/Audio）、Accessibility/Localization、Transition/Sequence、Performance Budget、Analytics Events。
- 模板与指南：
  - 分镜说明指南：[interface_screen_storyboard_guide.md](GDDMarkdownTemplate/templates/interface_screen_storyboard_guide.md)
  - 分镜表模板：[interface_screen_storyboard_template.md](GDDMarkdownTemplate/templates/interface_screen_storyboard_template.md)

## 7.9 UX Design Philosophy（用户体验设计哲学）

> 超越功能性 UI，关注“为什么玩家要交互”的心理动机。

- **Curiosity-Driven Design（好奇心驱动设计）**：
    - 如何通过未知的 UI 元素引发探索欲？（例如：未解锁的黑色剪影）。
- **Self-Narrative（自我叙事）**：
    - 界面如何反映玩家的成长？（例如：主界面背景随剧情变化，头像框展示成就）。
- **Feedback Juiciness（反馈的“多汁感”）**：
    - 确保每一次点击都有视觉、听觉甚至触觉的悦动反馈。

## 7.10 Onboarding & Paywall Flows（新手流程与付费墙）

- **Onboarding Flow（新手上路流程）**：
    - FTUE (First Time User Experience) 流程图。
    - 关键“Aha Moment”的时刻安排。
- **Paywall Design（付费墙设计）**：
    - 触发时机（在用户产生需求的一瞬间弹出）。
    - 价值主张展示（清晰告知“为什么值得买”）。
    - 心理学应用（锚定效应、社会认同等）。
