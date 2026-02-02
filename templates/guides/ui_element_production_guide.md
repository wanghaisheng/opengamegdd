# UI 元素资产生产指南（按钮/面板/图标/叠加层）

## 能力与约束
- 载体：ui_element（静帧 image、sprite_sheet、image_sequence）。
- 目标：一致的视觉风格与交互反馈，良好适配与可访问性。

## 输入规范
- 尺寸与布局：以网格与基线系统规范化；留白与对齐统一。
- DPI 与多分辨率：1x/2x/3x 切图；竖屏/横屏适配。
- 命名：UI_[component]_[state].png、SPR_UI_[group]_atlas.png。

## 状态与动效
- 状态集：normal/hover/pressed/disabled；可选 active/success/error。
- 动效载体：sprite_sheet（轻量）或 image_sequence（复杂叠加）。
- 反馈：点击/确认/错误的视觉与音频反馈。

## 可访问性与本地化
- 对比度与色弱模式；最小字号与换行策略。
- 文本长度与语言方向（LTR/RTL）；图标语义一致。

## 校验与交付
- 校验：尺寸/切图/索引正确；动效无穿帮；可访问性检查。
- 交付：静帧/atlas/index、动效素材、音频反馈（可选）、元数据（format=ui_element）。
