# 团队角色与文档职责矩阵 (Role Responsibility Matrix)

本文档旨在梳理 `docs/templates` 及其子目录下的文档体系与游戏开发团队各角色的对应关系。通过明确每个角色的输入、输出及职责，确保文档被正确使用，提升团队协作效率。

---

## 1. 核心策划团队 (Core Design Team)

### 1.1 系统策划 / 玩法策划 (System / Gameplay Designer)
*   **职责**: 定义游戏规则、系统逻辑、产出资产需求列表。
*   **涉及文档**:
    *   `asset_list_template.md` / `asset_list_template.csv`
    *   `universal_storyboard_method.md`
    *   `mvp_gameplay_video_guide.md`
*   **输入**: 游戏核心机制文档 (GDD)、功能需求。
*   **输出**: 
    *   **资产需求列表**：包含ID、格式、用途的详细清单。
    *   **玩法分镜草图**：用于指导MVP视频或实际开发。
*   **关键任务**: 
    *   使用 `asset_list_template` 将策划案转化为美术/程序可执行的资产清单。
    *   利用 `universal_storyboard_method` 描述核心玩法的视觉流程。

### 1.2 文案策划 / 剧情策划 (Narrative Designer)
*   **职责**: 编写剧本、台词、设计演出桥段和情感体验。
*   **涉及文档**:
    *   `storyboard_structured_prompt.md`
    *   `video_storyboard_template.md`
    *   `gacha_animation_storyboard.md`
*   **输入**: 世界观设定、角色设定、关卡流程。
*   **输出**:
    *   **结构化分镜脚本**：将纯文本剧本转化为包含镜头、动作、音频信息的结构化表格。
    *   **演出需求文档**：针对抽卡、过场动画的具体演出说明。
*   **关键任务**:
    *   使用 `storyboard_structured_prompt` 将自然语言剧本快速转化为标准分镜表，供美术团队使用。

### 1.3 关卡/交互策划 (Level / Interaction Designer)
*   **职责**: 设计界面流转、关卡结构、交互逻辑。
*   **涉及文档**:
    *   `interface_screen_storyboard_template.md`
    *   `interface_screen_storyboard_guide.md`
    *   `playable_ad_video_guide.md`
*   **输入**: 系统功能图、UIUX规范。
*   **输出**:
    *   **界面分镜**：清晰的UI流转图和状态变化说明。
    *   **试玩广告流程**：定义Playable Ad的交互热区和跳转逻辑。

### 1.4 数值策划 (Numerical / Balance Designer)
*   **职责**: 设计数值公式、平衡战斗参数、产出资产性能预算建议。
*   **涉及文档**:
    *   `asset_extraction_guide.md`
    *   `video_encoding_profiles.csv`
*   **输入**: 战斗机制、角色属性、经济模型。
*   **输出**:
    *   **性能预算建议**：基于数值模拟得出的资产复杂度限制（如特效时长、模型面数）。
    *   **战斗参数表**：用于程序和美术配置的数值数据。
*   **关键任务**:
    *   协助 **TA** 确定 `asset_extraction_guide.md` 中的性能边界，确保资产表现不影响战斗平衡。

### 1.5 商业化策划 / 经济系统设计师 (Monetization / Economy Designer)
*   **职责**: 设计游戏经济循环、定价策略、抽卡（Gacha）体系。
*   **涉及文档**:
    *   `gacha_animation_spec.md`
    *   `gacha_animation_metadata_schema.json`
    *   `asset_list_template.csv`
*   **输入**: 商业化目标、数值模型。
*   **输出**:
    *   **商品需求列表**：付费点相关的资产需求（如礼包图、抽卡动画）。
    *   **抽卡演出规范**：定义不同稀有度的视觉表现差异。
*   **关键任务**:
    *   利用 `gacha_animation_spec` 制定能够刺激付费的抽卡演出流程。

### 1.6 IP 架构师 / 世界观总监 (IP Architect / World Director)
*   **职责**: 确保所有资产和叙事符合 IP 核心设定，维护品牌一致性。
*   **涉及文档**:
    *   `storyboard_structured_prompt.md`
    *   `video_asset_guide.md`
*   **输入**: IP 圣经 (IP Bible)、原始版权方要求。
*   **输出**:
    *   **IP 监修意见**：对角色、场景、剧情的审核反馈。
    *   **世界观设定集**：指导美术和文案的顶层设计。

---

## 2. 美术设计团队 (Art Design Team)

### 2.1 美术总监 / 概念艺术家 (Art Director / Concept Artist)
*   **职责**: 确立视觉风格、审核资产质量。
*   **涉及文档**:
    *   `image_asset_production_guide.md`
    *   `ui_element_production_guide.md`
*   **输入**: 艺术风格指南 (Art Bible)、Moodboard。
*   **输出**:
    *   **概念设计稿**：角色、场景、UI的概念图。
    *   **资产生产标准**：针对不同图片资产的具体的视觉规范。

### 2.2 3D美术 / 动画师 (3D Artist / Animator)
*   **职责**: 制作3D模型、绑定、动画数据。
*   **涉及文档**:
    *   `3d_model_production_guide.md`
    *   `gacha_animation_spec.md`
*   **输入**: 角色/场景原画、分镜脚本。
*   **输出**:
    *   **3D资产模型**：符合规范的.fbx/.obj等文件。
    *   **动画片段**：符合镜头需求的动画数据。

### 2.3 特效美术 (VFX Artist)
*   **职责**: 设计和制作游戏内的视觉特效（粒子、Shader动画等）。
*   **涉及文档**:
    *   `vfx_discussion.md`
    *   `fx_particle_production_guide.md`
    *   `image_sequence_guide.md`
    *   `storyboard_for_image_sequence_assets.md`
*   **输入**: 技能设计文档、动作资源、分镜需求。
*   **输出**:
    *   **特效预制体**：Particle Systems, Shaders。
    *   **序列帧资源**：用于UI或特定性能限制场景的序列帧图集。

### 2.4 UI/UX设计师 (UI/UX Designer)
*   **职责**: 制作最终UI界面资源、图标、HUD元素，设计交互流程。
*   **涉及文档**:
    *   `ui_element_production_guide.md`
    *   `sprite_sheet_production_guide.md`
    *   `interface_screen_storyboard_guide.md`
*   **输入**: 界面分镜、交互原型、探索体验架构文档。
*   **输出**:
    *   **UI切图**：Sprite Sheets, PNGs。
    *   **UI动效资源**。
    *   **交互规范**：点击反馈、转场逻辑。

---

## 3. 技术与工具团队 (Tech & Tools Team)

### 3.1 技术美术 (Technical Artist - TA)
*   **职责**: 制定资产规范、性能优化、搭建管线、Shader编写。
*   **涉及文档**:
    *   `asset_extraction_guide.md`
    *   `asset_metadata_schema.json` (及相关JSON Schema)
    *   `video_encoding_profiles.csv`
    *   `image_sequence_guide.md`
*   **输入**: 引擎性能指标、美术资产。
*   **输出**:
    *   **技术规范文档**：模型面数限制、贴图尺寸、编码格式。
    *   **验证工具**：用于自动化检查资产是否符合Schema的脚本。
*   **关键任务**:
    *   维护 `asset_metadata_schema.json`，确保资产导入引擎时的元数据正确性。
    *   制定视频和序列帧的性能权衡标准 (`image_sequence_guide.md`)。

### 3.2 解决方案架构师 (Solution Architect / Lead Programmer)
*   **职责**: 设计游戏技术架构、选择技术栈、评估技术可行性。
*   **涉及文档**:
    *   `asset_metadata_schema.json`
    *   `asset_extraction_guide.md`
*   **输入**: GDD、资产需求列表。
*   **输出**:
    *   **技术架构文档**：客户端/服务端架构、数据流向。
    *   **技术风险评估**：针对特定玩法或资产规模的性能预警。
*   **关键任务**:
    *   审核 `asset_extraction_guide` 确保提取流程符合引擎管线。

---

## 4. 市场与视频团队 (Marketing & Video Team)

### 4.1 视频剪辑师 / 动效设计师 (Video Editor / Motion Designer)
*   **职责**: 制作PV、过场视频、买量素材、MVP演示视频。
*   **涉及文档**:
    *   `video_asset_guide.md`
    *   `storyboard_for_video_assets.md`
    *   `mvp_gameplay_video_guide.md`
    *   `api_video_generation_guide.md`
    *   `playable_ad_video_guide.md`
*   **输入**: 游戏实机画面、美术素材、分镜脚本、音频。
*   **输出**:
    *   **成品视频文件**：mp4/webm等格式。
    *   **试玩广告素材**：交互式视频片段。
*   **关键任务**:
    *   利用 `mvp_gameplay_video_guide` 在无代码阶段模拟核心玩法视频。
    *   使用 `api_video_generation_guide` 批量生产素材。

### 4.2 音频设计师 (Audio Designer)
*   **职责**: 制作BGM、SFX、语音。
*   **涉及文档**:
    *   `audio_asset_production_guide.md`
*   **输入**: 视频分镜（时间轴）、功能需求列表。
*   **输出**:
    *   **音频文件**：wav/mp3/ogg。
    *   **音频中间件工程** (如Wwise/FMOD)。

### 4.3 技术营销经理 (Technical Marketing Manager)
*   **职责**: 搭建自动化营销素材生产管线，利用 API 批量生成视频。
*   **涉及文档**:
    *   `api_video_generation_guide.md`
    *   `video_asset_metadata_schema.json`
*   **输入**: 营销日历、基础美术素材库。
*   **输出**:
    *   **自动化脚本/工具**：对接视频生成 API 的工程。
    *   **批量素材库**：用于 A/B 测试的大量视频变体。
*   **关键任务**:
    *   实施 `api_video_generation_guide` 中的流程，实现“千人千面”的广告素材投放。

---

## 5. 项目管理 (Project Management)

### 5.1 制作人 / 项目经理 (Producer / PM)
*   **职责**: 进度管理、资源协调、外包管理。
*   **涉及文档**:
    *   `asset_list_template.csv`
    *   `asset_extraction_guide.md`
*   **输入**: 各部门排期、里程碑目标。
*   **输出**:
    *   **资产进度表**：追踪每个Asset ID的制作状态（草稿/完成/审核/入库）。
    *   **外包需求包**：基于规范文档打包的明确需求。

### 5.2 敏捷教练 / Scrum Master
*   **职责**: 维护开发流程、管理待办事项 (Backlog)、消除团队阻碍。
*   **涉及文档**:
    *   `asset_list_template.csv`
*   **输入**: 冲刺目标 (Sprint Goal)、GDD。
*   **输出**:
    *   **用户故事 (User Stories)**：将设计文档拆解为可开发的任务卡片。
    *   **燃尽图 (Burndown Chart)**：可视化项目进度。
*   **关键任务**:
    *   确保 `asset_list_template` 中的资产被正确拆分为Sprint任务。

### 5.3 设计验证师 / QA总监 (Design Validator / QA Director)
*   **职责**: 验证设计一致性、风险评估、验收测试。
*   **涉及文档**:
    *   `universal_storyboard_method.md`
    *   `asset_metadata_schema.json`
*   **输入**: 所有设计文档、已产出资产。
*   **输出**:
    *   **风险评估报告**：指出设计文档中的逻辑漏洞或资源冲突。
    *   **测试用例**：针对玩法逻辑的测试步骤。

### 5.4 外包管理经理 (Outsourcing Manager)
*   **职责**: 管理外部供应商、分发需求、审核交付质量。
*   **涉及文档**:
    *   `asset_extraction_guide.md`
    *   `asset_list_template.csv`
    *   `3d_model_production_guide.md`
*   **输入**: 资产需求列表、预算计划。
*   **输出**:
    *   **外包工作单 (Work Orders)**：包含详细规格说明的合同附件。
    *   **反馈记录**：对供应商提交物的修改意见。
*   **关键任务**:
    *   将 `asset_extraction_guide.md` 作为外包合同的标准附件，确保交付物格式统一。

---

## 6. 战略与运营团队 (Strategy & Operations Team)

### 6.1 市场分析师 (Market Analyst)
*   **职责**: 提供市场定位、用户画像、竞品分析。
*   **涉及文档**:
    *   `playable_ad_video_guide.md`
    *   `video_asset_guide.md`
*   **输入**: 市场数据、趋势报告。
*   **输出**:
    *   **市场定位文档**：指导美术风格和核心玩法方向。
    *   **素材方向建议**：针对买量市场的视频素材建议。

### 6.2 社区与长线运营 (Community & LiveOps Manager)
*   **职责**: 规划长线活动、管理玩家社区、收集反馈。
*   **涉及文档**:
    *   `gacha_animation_spec.md`
    *   `mvp_gameplay_video_guide.md`
*   **输入**: 玩家反馈、运营数据。
*   **输出**:
    *   **活动策划案**：节日活动、新角色推广计划。
    *   **社区内容日历**：规划PV、演示视频的发布节奏。

### 6.3 本地化经理 (Localization Manager)
*   **职责**: 管理多语言翻译流程、文化适应性检查。
*   **涉及文档**:
    *   `ui_element_production_guide.md`
    *   `audio_asset_production_guide.md`
    *   `asset_list_template.csv`
*   **输入**: 原始文本 (Source Text)、音频脚本。
*   **输出**:
    *   **本地化资源包**：各语言的文本表和配音文件。
    *   **UI适配建议**：针对德语/俄语等长文本语言的界面调整需求。
*   **关键任务**:
    *   检查 `ui_element_production_guide` 中的文本框预留空间是否足够。

### 6.4 用户研究员 (User Researcher)
*   **职责**: 组织玩家测试、分析行为数据、验证设计假设。
*   **涉及文档**:
    *   `mvp_gameplay_video_guide.md`
    *   `playable_ad_video_guide.md`
*   **输入**: MVP视频、试玩广告Demo。
*   **输出**:
    *   **用户体验报告**：基于测试视频的玩家反馈分析。
    *   **A/B测试建议**：针对 Playable Ad 的优化方向。

---

## 总结：协作工作流示例

1. **需求阶段**：
    *   **系统策划**使用 `asset_list_template` 列出新角色的资产需求。
    *   **文案策划**使用 `storyboard_structured_prompt` 生成该角色的登场动画分镜。

2. **规范阶段**：
    *   **TA** 根据 `3d_model_production_guide` 和 `gacha_animation_spec` 确认模型面数和骨骼标准。

3. **生产阶段**：
    *   **美术/动画** 开始制作，参考 `image_asset_production_guide`。
    *   **视频团队** 同步制作预告PV，参考 `video_asset_guide`。

4. **验收与集成**：
    *   **TA/程序** 对照 `asset_metadata_schema` 检查提交的资源。
    *   **策划** 验收MVP视频 (`mvp_gameplay_video_guide`) 确认设计意图是否达成。
