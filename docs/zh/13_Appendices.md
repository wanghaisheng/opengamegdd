# 13. Appendices（附录）

> 作为「索引」存在，统一管理资产清单、术语表与 KPI 定义等。

## 13.1 Asset List（资产清单总览）

- 维护方式（表格 / 外部表格链接 / 资产管理系统）：
- 字段建议：ID、名称、类型、所属系统、资源路径、责任人、状态等。

### 13.1.1 Art（美术资产）

- Model and Texture List（模型与贴图清单）：
- Animation List（动画清单）：
- Effects List（特效清单）：
- Interface Art List（界面美术清单）：
- Cut Scene List（过场相关资源清单）：

### 13.1.2 Sound（音效）

- Environmental Sounds（环境音）：
- Weapon Sounds（武器音效）：
- Interface Sounds（界面音效）：

### 13.1.3 Music（音乐）

- Ambient（环境音乐）：
- Action（战斗音乐）：
- Victory / Defeat（胜利 / 失败音乐）：

### 13.1.4 Voice（配音）

- Actor #1 Lines（角色 #1 台词清单）：
- 按角色 / 章节 / 语言拆分的配音资产表：

## 13.2 Glossary（术语表）

- 游戏内关键概念统一定义：
- 内部通用的缩写（如 FTUE、ARPDAU、DAU 等）：
- 防止多团队、多地区理解不一致：

## 13.3 KPI Definitions（核心指标定义）

> 与 3.9、9.9、12.8 等章节中提到的指标做精确定义。

- 留存相关指标（D1 / D7 / D30 等）：
- 付费与收入指标（ARPU / ARPPU / ARPDAU / 付费率等）：
- 运营活动指标（参与率、完成率、活动期间 ARPDAU 提升幅度等）：

## 13.4 External References（外部参考资料）

- 竞品分析报告链接：
- 内部分享或复盘文档：
- 重要中台 / 平台文档链接（账号、支付、数据、反作弊等）：

## 13.5 Asset Roadmap（资产路线图）

- 定义：将资产清单转化为可执行生产时间表（阶段、时间线、依赖、里程碑）。
- 核心步骤：
  - 输入资产清单（角色、背景、道具、特效、声音、UI）。
  - 阶段划分：概念 → 建模 → 贴图 → 动作 → 测试 → 发布。
  - 时间计划：Gantt 图或看板，考虑 10–20% 缓冲与跨团队依赖。
  - 工具：Excel/Google Sheets 模板、GanttPRO、Miro 看板。
- 简版表头建议：
  - ID、类别、描述、数量、变体、规格（分辨率/多边形）、优先级、依赖、负责人、开始/结束日期、状态、来源（GDD页/分镜帧）。
- 益处：降低成本与延误、提升协作效率，适用于独立到中大型项目。

### 13.5.1 Templates（模板文件）

- CSV 模板：[asset_list_template.csv](GDDMarkdownTemplate/templates/asset_list_template.csv)
- Markdown 模板：[asset_list_template.md](GDDMarkdownTemplate/templates/asset_list_template.md)
- 元数据 JSON Schema：[asset_metadata_schema.json](GDDMarkdownTemplate/templates/asset_metadata_schema.json)

### 13.5.2 Specific Asset Templates（特定资产模板）

- 抽卡展示动画 – 设计规范（MD）：[gacha_animation_spec.md](GDDMarkdownTemplate/templates/gacha_animation_spec.md)
- 抽卡展示动画 – 分镜表（MD）：[gacha_animation_storyboard.md](GDDMarkdownTemplate/templates/gacha_animation_storyboard.md)
- 抽卡展示动画 – 元数据 Schema（JSON）：[gacha_animation_metadata_schema.json](GDDMarkdownTemplate/templates/gacha_animation_metadata_schema.json)

### 13.5.3 Video Asset Templates（视频资产模板）

- 通用视频制作指南（MD）：[video_asset_guide.md](GDDMarkdownTemplate/templates/guides/video_asset_guide.md)
- 通用视频分镜表（MD）：[video_storyboard_template.md](GDDMarkdownTemplate/templates/video_storyboard_template.md)
- 视频资产元数据 Schema（JSON）：[video_asset_metadata_schema.json](GDDMarkdownTemplate/templates/video_asset_metadata_schema.json)
- 视频编码档位（CSV）：[video_encoding_profiles.csv](GDDMarkdownTemplate/templates/video_encoding_profiles.csv)
- 视频镜头分解说明（MD）：[storyboard_for_video_assets.md](GDDMarkdownTemplate/templates/guides/storyboard_for_video_assets.md)
- API 驱动视频生产指南（MD）：[api_video_generation_guide.md](GDDMarkdownTemplate/templates/guides/api_video_generation_guide.md)
- MVP 游玩预渲染视频指南（MD）：[mvp_gameplay_video_guide.md](GDDMarkdownTemplate/templates/guides/mvp_gameplay_video_guide.md)

### 13.5.4 Image Sequence Guide（序列帧指南）

- 使用场景与制作说明（MD）：[image_sequence_guide.md](GDDMarkdownTemplate/templates/guides/image_sequence_guide.md)
- 序列帧镜头分解说明（MD）：[storyboard_for_image_sequence_assets.md](GDDMarkdownTemplate/templates/guides/storyboard_for_image_sequence_assets.md)

### 13.5.5 Asset Extraction Guide（资产清单分析）

- 从 GDD 提取资产并判定格式（MD）：[asset_extraction_guide.md](GDDMarkdownTemplate/templates/guides/asset_extraction_guide.md)

### 13.5.6 Universal Storyboard Method（通用分镜方法论）

- 抽象方法论与示例（MD）：[universal_storyboard_method.md](GDDMarkdownTemplate/templates/guides/universal_storyboard_method.md)
### 13.5.8 VFX Discussion（特效格式与选型）

- 特效格式讨论与资产映射（MD）：[vfx_discussion.md](GDDMarkdownTemplate/templates/guides/vfx_discussion.md)

### 13.5.9 Playable Ad Guide（试玩广告预渲染视频）

- 试玩广告（可点击串联分镜）指南（MD）：[playable_ad_video_guide.md](GDDMarkdownTemplate/templates/guides/playable_ad_video_guide.md)

## 13.6 Common-language Mapping（通俗术语映射）
### 13.5.7 Format Production Guides（格式生产指南）

- 图片（image）：[image_asset_production_guide.md](GDDMarkdownTemplate/templates/guides/image_asset_production_guide.md)
- 精灵表（sprite_sheet）：[sprite_sheet_production_guide.md](GDDMarkdownTemplate/templates/guides/sprite_sheet_production_guide.md)
- 3D 模型（3d_model）：[3d_model_production_guide.md](GDDMarkdownTemplate/templates/guides/3d_model_production_guide.md)
- 音频（audio）：[audio_asset_production_guide.md](GDDMarkdownTemplate/templates/guides/audio_asset_production_guide.md)
- 粒子/特效（fx_particle）：[fx_particle_production_guide.md](GDDMarkdownTemplate/templates/guides/fx_particle_production_guide.md)
- UI 元素（ui_element）：[ui_element_production_guide.md](GDDMarkdownTemplate/templates/guides/ui_element_production_guide.md)
## 13.6 Common-language Mapping（通俗术语映射）

- 角色（演员）：主角/敌人/NPC，能走、说话、战斗。
- 背景（布景）：森林、城市、房间等场景。
- 道具（物件）：武器、家具、树木等可交互物品。
- 灯光（光源）：火把、日光，用于突出重点或制造阴影。
- 特效（视觉效果）：爆炸、火光、烟雾等增强表现。
- 声音（配乐/音效）：BGM、脚步、喊叫等听觉反馈。
- 屏幕显示（字幕/HUD）：血条、菜单、提示等信息层。
- 用途：跨团队与非专业参与者沟通更顺畅；资产清单可同时保留专业与通俗两列，减少误解。

## 13.7 Advanced Templates & Checklists（进阶模板与检查单）

> 补充复杂系统所需的详细配置表与检查单。

### 13.7.1 Economy & Monetization（经济与商业化）

- **Economy CSV Configs（经济数值配置表）**：
    - 包含所有商品、定价、产出、消耗的数值表结构。
- **Monetization Checklist（商业化检查单）**：
    - 上线前必须核对的付费体验细节（价格锚点、二次确认、促销标识等）。
- **Subscription Growth Checklist（订阅增长检查单）**：
    - 针对订阅制游戏的 LTV 优化检查项。

### 13.7.2 VIP System Tables（VIP 系统表）

- **VIP Level & Privilege Table（VIP 等级权益表）**：
    - 详细列出每一级 VIP 需要的经验值及对应的特权差异。

