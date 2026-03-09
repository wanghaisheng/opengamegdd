# Game Design Document (GDD) Master Template（游戏设计文档总模板）

本目录包含一套**工业化游戏设计系统**，结合天美工作室群、原神（米哈游）、腾讯等大厂公开分享资料，以及"浓缩理论"等先进设计理念整理的GDD模板。

该模板启发自 https://github.com/LazyHatGuy/GDDMarkdownTemplate ，并结合我过往一年多的 vibe coding 探索与多年积累的游戏分析文章行业认知，形成面向AI agents的**工业化游戏设计系统**。

每个章节为一个独立 Markdown 文件，可单独放入 Wiki 或文档系统中使用，避免传统 PDF/Word 形式在协作与迭代上的限制。

## 🚀 重大升级亮点

### 🎯 工业化设计体系
- **策划细化框架**：技能、任务、数值、商业、剧情、系统架构6大细化模块
- **核心爽点循环设计**：基于"浓缩理论"的完整设计框架
- **世界观设计工具链**：基于天美工作室群工业化经验
- **AI辅助设计系统**：集成人工智能工具的设计决策支持

### 🎮 游戏类型专门化
- **8大游戏类型适配**：动作、RPG、策略、卡牌、模拟经营、消除、放置、恋爱养成
- **基于游戏分类数据**：覆盖市场95%以上游戏类型
- **混合类型支持**：灵活的模块选择和机制融合

### 📊 量化评估体系
- **权重分配系统**：游戏玩法逻辑性15%、剧情连贯性10%、系统架构合理性5%
- **科学评分标准**：每个模块都有具体的评估指标和检查清单
- **数据驱动设计**：基于真实市场数据的设计指导

### 🌍 国际化支持
- **中英文版本同步**：完全对应的双语版本
- **跨国团队协作**：适配不同地区的开发习惯
- **全球适用标准**：达到国际化大厂设计标准

## 作者与链接
- 网站：https://opengdd.borninsea.com/
- X：https://x.com/edwin_uestc
- GitHub：https://github.com/wanghaisheng
- LinkedIn：https://www.linkedin.com/in/wanghaisheng/

## 📚 文档结构（15章完整体系）

### 🎯 核心设计章节
- **3_Game Overview.md** —— 游戏概述与产品定义
  - 新增3.1.1核心爽点循环设计[权重8%]
- **4_Gameplay and Mechanics.md** —— 核心玩法与系统机制
  - 重构4.2.7.2基于游戏类型的系统架构设计
  - 完善商业化分层设计体系
- **5_Story, Setting and Character.md** —— 世界观与角色设定
  - 重构为5.1世界观设计工具链[权重6%]

### 🔧 技术与实现章节
- **9_Technical.md** —— 技术方案与架构
  - 添加9.1系统架构设计体系[权重5%]

### 🤖 AI与创新章节
- **14_AI-Assisted Design.md** —— AI辅助设计系统[新增]
  - 好玩浓度测试器集成
  - 世界观AI助手
  - 设计质量AI评估

### 🎮 类型适配章节
- **15_Game Type Adaptation.md** —— 游戏类型适配模块[新增]
  - 8大游戏类型专门化适配
  - 混合类型处理机制

### 📋 基础章节
- 1_Copyright Information.md —— 版权与法律信息
- 2_Version History.md —— 文档版本与审批记录
- 6_Levels.md —— 关卡与内容结构
- 7_Interface.md —— 界面与交互系统
- 8_Artificial Intelligence.md —— 人工智能设计
- 9_Technical.md —— 技术方案与架构
- 10_Game Art.md —— 美术风格与资源规划
- 11_Secondary Software.md —— 配套工具与二级软件
- 12_Management.md —— 项目管理与运营规划
- 13_Appendices.md —— 附录与资产清单
- 14_AI-Assisted Design.md —— AI辅助设计系统
- 15_Game Type Adaptation.md —— 游戏类型适配模块

## 🎯 使用建议

### 📋 最小可行版本(MVP)
建议在立项初期先完成以下章节的「最小可行版本」：
1. **3_Game Overview** - 包含核心爽点循环设计
2. **4_Gameplay and Mechanics** - 包含游戏类型适配
3. **9_Technical** - 包含系统架构设计

### 🔄 迭代流程
1. **第一阶段**：完成核心设计章节(3、4、9章)
2. **第二阶段**：补充世界观和AI设计(5、14章)
3. **第三阶段**：完善类型适配和评估(15章)
4. **第四阶段**：补全其他章节和附录

### 🎮 游戏类型选择
根据项目类型选择相应的适配模块：
- **动作游戏**：选择动作游戏适配模块
- **RPG游戏**：选择RPG游戏适配模块
- **卡牌游戏**：选择卡牌游戏适配模块
- **混合类型**：参考混合类型处理原则

## 📖 相关指南

### 🎯 设计指南
- [策划细化框架集成指南](templates/guides/enhanced_gdd_structure_integration.md)
- [游戏类型适配指南](docs/zh/15_Game%20Type%20Adaptation.md)
- [AI辅助设计使用指南](docs/zh/14_AI-Assisted%20Design.md)

## 🎯 特色功能

### 🤖 AI赋能设计
- **好玩浓度测试器**：基于浓缩理论的AI分析工具
- **世界观AI助手**：自动化世界观设计支持
- **设计质量评估**：AI驱动的质量检查和优化建议

### 📊 数据驱动
- **量化评估体系**：科学的评分标准和权重分配
- **类型专门化**：基于真实市场数据的设计指导
- **平衡验证**：系统性的数值平衡检查

### 🌍 工业化标准
- **模块化设计**：清晰的系统划分和关联
- **流程标准化**：从设计到实现的完整流程
- **质量保证**：多层次的评估和验证机制

## 🔄 更新历史

### 最新版本特性
- ✅ **核心爽点循环设计**：基于浓缩理论的完整设计框架
- ✅ **世界观设计工具链**：工业化世界观设计体系
- ✅ **AI辅助设计系统**：集成人工智能工具
- ✅ **游戏类型适配**：8大游戏类型专门化指导
- ✅ **商业化分层设计**：完整的用户分层策略
- ✅ **系统架构重构**：基于游戏类型的设计方法

### 技术升级
- 🔄 **WBS方法重构**：从项目管理方法改为游戏设计理论方法
- 🔄 **模块通用性**：解决特定模块的通用性问题
- 🔄 **评估体系**：建立科学的量化评估标准
- 🔄 **国际化同步**：中英文版本完全对应

## 📥 如何下载所有文档

  ![下载到本地](public/how-to-download.png)

## GDD 交付物结构指南
- [GDD_Deliverable_Structure.md](templates/guides/gdd_deliverable_structure.md) —— 游戏设计文档交付物标准目录结构说明
- [Idea_to_Playable_Workflow.md](templates/guides/idea_to_playable_workflow.md) —— 从创意到试玩广告的全流程指南

> 建议：在立项初期先完成 3、4、9 章的「最小可行版本」，随后逐步补全其它章节。

## 更新说明（资产规范增补）

- 新增「资产管线与命名规范」：见 [10_Game Art](docs/10_Game%20Art.md) 的 10.10 章节。
- 更新「格式维度与选型」说明：见 [10_Game Art](docs/10_Game%20Art.md) 的 Format 维度与选型要点。
- 新增「资产路线图与通俗术语映射」：见 [13_Appendices](docs/13_Appendices.md) 的 13.5、13.6 章节。
- 新增「资产元数据与自动化校验」：见 [9_Technical](docs/9_Technical.md) 的 9.12、9.13 章节。
- 资产清单模板文件位置：templates/  
  - [asset_list_template.csv](templates/asset_list_template.csv)  
  - [asset_list_template.md](templates/asset_list_template.md)  
  - [asset_metadata_schema.json](templates/asset_metadata_schema.json)
  - 特定资产模板（抽卡展示动画）：  
    - [gacha_animation_spec.md](templates/gacha_animation_spec.md)  
    - [gacha_animation_storyboard.md](templates/gacha_animation_storyboard.md)  
    - [gacha_animation_metadata_schema.json](templates/gacha_animation_metadata_schema.json)
  - 视频资产模板（通用）：  
    - [video_asset_guide.md](templates/guides/video_asset_guide.md)  
    - [video_storyboard_template.md](templates/video_storyboard_template.md)  
    - [video_asset_metadata_schema.json](templates/video_asset_metadata_schema.json)  
    - [video_encoding_profiles.csv](templates/video_encoding_profiles.csv)
  - 序列帧指南：  
    - [image_sequence_guide.md](templates/guides/image_sequence_guide.md)
  - 资产提取说明：  
    - [asset_extraction_guide.md](templates/guides/asset_extraction_guide.md)
  - 通用分镜方法论：  
    - [universal_storyboard_method.md](templates/guides/universal_storyboard_method.md)
  - 镜头分解说明（按载体）：  
    - 视频资产：[storyboard_for_video_assets.md](templates/guides/storyboard_for_video_assets.md)  
    - 序列帧资产：[storyboard_for_image_sequence_assets.md](templates/guides/storyboard_for_image_sequence_assets.md)
  - API 驱动视频生产：  
    - [api_video_generation_guide.md](templates/guides/api_video_generation_guide.md)
  - 格式生产指南：  
    - 图片（image）：[image_asset_production_guide.md](templates/guides/image_asset_production_guide.md)  
    - 精灵表（sprite_sheet）：[sprite_sheet_production_guide.md](templates/guides/sprite_sheet_production_guide.md)  
    - 3D 模型（3d_model）：[3d_model_production_guide.md](templates/guides/3d_model_production_guide.md)  
    - 音频（audio）：[audio_asset_production_guide.md](templates/guides/audio_asset_production_guide.md)  
    - 粒子/特效（fx_particle）：[fx_particle_production_guide.md](templates/guides/fx_particle_production_guide.md)  
    - UI 元素（ui_element）：[ui_element_production_guide.md](templates/guides/ui_element_production_guide.md)
  - 特效讨论：  
    - [vfx_discussion.md](templates/guides/vfx_discussion.md)
  - 试玩广告（Playable Ad）：  
    - [playable_ad_video_guide.md](templates/guides/playable_ad_video_guide.md)
  - MVP 游玩预渲染视频：  
    - [mvp_gameplay_video_guide.md](templates/guides/mvp_gameplay_video_guide.md)

## 支持方式
- PayPal：https://www.paypal.com/ncp/payment/BAGUNNTYE9R76
- 支付宝（中国）：
  
  ![支付宝（中国）](public/alipay-china.jpg)
- 支付宝（国际）：
  
  ![支付宝（国际）](public/alipay-international.jpg)
- 微信支付（中国）：
  
  ![微信支付（中国）](public/wechat-china.jpg)

---

**现在就开始使用这个工业化游戏设计系统，创建您的下一个成功游戏！**