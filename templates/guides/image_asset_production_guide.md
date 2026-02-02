# 图片资产生产指南（纹理/贴图/UI静帧/背景）

## 能力与约束
- 载体：image（PNG/JPG/WebP/TGA），支持 Alpha（透明）。
- 用途：纹理贴图（PBR）、UI 图标/海报/插图、静态背景帧。

## 输入规范
- 色彩空间：sRGB（UI/贴图），线性空间按引擎规范。
- 分辨率：遵循平台与画面布局；尽量使用 2 的幂或满足引擎纹理要求。
- 命名：T_[subject]_[channel].tga（_D/_N/_R/_AO/_M 或 _RMA）、UI_[name].png。

## 制作要点（PBR）
- 通道：_D（BaseColor）、_N（Normal）、_R（Roughness）、_AO、_M（Metallic）；或 _RMA 打包。
- MIP 与滤波：启用 MIP；各级别无明显色偏与伪影。
- 压缩：平台友好格式（如 ASTC/ETC2/BCn），UI 避免过度压缩导致文字锯齿。

## UI 与背景
- DPI 与适配：按多分辨率切图；提供 1x/2x/3x。
- 9-Slice：按钮与面板使用九宫格以避免拉伸失真。
- 可访问性：高对比度、色弱模式适配；文字留白与最小字号。

## 校验与交付
- 校验：分辨率/色彩空间/Alpha 正常；通道命名正确。
- 交付：源文件（PSD/AI 可选）、导出图片、索引/切图说明、元数据（format=image）。
