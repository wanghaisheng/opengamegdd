# 10. Game Art（美术）

> 定义整体视觉方向、美术风格与资源规划，为长期版本更新提供统一视觉基线。

## 10.1 Art Direction Overview（美术总方向）

- 风格标签（写实 / 卡通 / 低多边形 / 像素等）：
- 参考作品与 Benchmark（包括原神、腾讯及 Voodoo 等相关产品）：
- 目标感受（轻松 / 压抑 / 史诗 / 可爱等）：

## 10.2 Concept Art（概念设计）

- 世界观概念图：
- 关键场景 / 城市 / 地标概念稿：
- 主要角色与敌人的概念稿：

## 10.3 Style Guides（风格规范）

- 线条、造型、比例、色彩、光影等统一规则：
- UI 与 3D / 2D 的风格统一性要求：
- 不允许出现的风格与元素（负面清单）：

## 10.4 Characters（角色美术）

- 角色分层（主角 / 重要 NPC / 敌人 / 村民等）：
- 每类角色的细节密度与标准（骨骼数量、多边形预算、贴图大小等）：
- 换装 / 皮肤系统的规则（作为长期商业化与 LiveOps 的重要部分）：

## 10.5 Environments（场景）

- 场景类型（城市、野外、地下城、特殊副本等）：
- 每种场景的色彩与光照基调：
- 模块化搭建策略（Tile、Module、Prefab 等）：

## 10.6 Equipment & Props（装备与道具）

- 装备层级（普通 / 稀有 / 传说等）在视觉上的区分：
- 功能性道具与装饰性道具的表现差异：

## 10.7 Cut Scenes（过场演出美术）

- 过场画面形式（实时 3D、2D 动画、漫画、立绘等）：
- 表现规范（分镜、字幕字号、logo 露出等）：

## 10.8 UI / UX Art（界面美术）

- UI 元素风格（扁平 / 拟物 / 卡通 / 高科技等）：
- 图标系统（主图标风格、尺寸、线面关系）：
- 动效与过渡（按钮反馈、界面切换、加载指示）：

## 10.9 Technical Art Considerations（技术美术）

- Shader 策略（通用 Shader / 特效 Shader / 角色 Shader 等）：
- 特效性能预算（粒子数量、透明度、后处理等）：
- 资源规范（命名、目录结构、引用规则）：

## 10.10 Asset Pipeline & Naming（资产管线与命名规范）

- 命名通用格式：前缀_主体_描述符/渠道_变体（避免空格与特殊符号，长度 < 50）。
- 推荐前缀示例（简版）：
  - 纹理：T_（如 T_hero_body_D / T_hero_body_N / T_hero_body_RMA）
  - 静态模型：SM_（如 SM_rifle_01）
  - 骨骼模型：SK_（如 SK_hero）
  - 材质 / 实例：M_ / MI_（如 M_hero_skin，MI_hero_skin_01）
  - 动画：ANM_（如 ANM_hero_run_01）
  - 音频 / 音效：MX_ / SX_（如 MX_theme_loop，SX_footstep_gravel_01）
  - 粒子 / 特效：PS_（如 PS_explosion）
  - UI 元素：UI_（如 UI_button_normal）
  - 灯光：Light_（如 Light_lamp_P_01）
- 贴图通道规范：_D（Diffuse）、_N（Normal）、_R（Roughness）、_AO、_M（Metallic），或 _RMA 打包。
- 变体与版本：_01 / _A / LOD0 / v001；保持两位数版本。
- 文件夹结构（结合功能分层 + 类型子分）：
  - Art/Characters/Hero/{Meshes, Textures, Materials, _wip}
  - Art/Weapons/Rifle/{Models, Textures}
  - Art/Environments/{Rocks, Trees}
  - Art/UI/{Sprites, Fonts}
  - Art/FX/Particles/
  - Audio/{SFX, Music, VO}
  - _Publish/（最终导出，无源文件）
- 元数据标签（JSON/XML）：LOD、Platform、Usage、Author、Version、Dependencies 等；用于搜索、打包与审计。
- 通俗术语映射（便于跨团队沟通）：
  - 角色（演员）、背景（布景）、道具（物件）、灯光（光源）、特效（视觉效果）、声音（配乐/音效）、屏幕显示（字幕/HUD）。
- 实施建议：项目立项即文档化规范；脚本批量重命名；CI/CD 校验命名与元数据完整性。

### Format 维度（资产格式分类）

- 3D 模型（3d_model）：SM/SK 等模型文件与骨骼数据。
- 图片（image）：单帧纹理/贴图/UI 图像。
- 序列帧（image_sequence）：按帧组织的图片序列（PNG/JPG/TGA），用于动画或特效；不属于视频容器，但可渲染为视频或打包为精灵表。
- 精灵表（sprite_sheet）：合并后的序列帧（单张大图 + 索引），用于 UI/2D 动画。
- 视频（video）：有容器与编码（MP4/H.264/H.265/WEBM），适合过场或展示。
- 音频（audio）：BGM/SFX/VO 等。
- 其它：shader/material/font/prefab/level/fx_particle/ui_element。

- 序列帧制作与使用指南：[image_sequence_guide.md](GDDMarkdownTemplate/templates/image_sequence_guide.md)

### 格式选型与命名要点

- 视频（video）：用于统一高质展示或过场，命名示例：VID_Cutscene_Chapter1_v001.mp4；提供多档码率与分辨率。
- 序列帧（image_sequence）：用于可控动画/特效，命名示例：SEQ_GachaReveal_0001.png；帧序统一位数（如 4 位）。
- 精灵表（sprite_sheet）：用于 UI/2D 动画，命名示例：SPR_UI_ButtonPress_atlas_v001.png；需配套索引文件。
- 图片（image）：纹理与贴图，命名示例：T_hero_body_RMA.tga；遵循通道后缀规则。
- 粒子 / 特效（fx_particle）：命名示例：PS_fire_small_loop、PS_explosion_heavy；区分规模与循环属性。
- 音频（audio）：BGM/SFX/VO，命名示例：MX_theme_loop.ogg、SX_footstep_gravel_01.wav、VO_hero_intro_zh.mp3。

### 选型建议

- 需要交互与镜头可控：优先 3d_model + image + fx_particle 实时渲染。
- 需要统一表现、高质但弱交互：选择 video，并提供多平台适配。
- 大量 2D/UI 动画：优先 sprite_sheet；复杂镜头或特效可用 image_sequence。
