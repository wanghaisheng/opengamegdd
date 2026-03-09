# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- **策划细化框架系统**: 创建完整的策划部分细化评估体系
  - `templates/guides/skill_planning_framework.md` - 技能策划框架 [权重4%]
  - `templates/guides/mission_planning_framework.md` - 任务策划框架 [权重4%]
  - `templates/guides/numerical_planning_framework.md` - 数值策划框架 [权重4%]
  - `templates/guides/monetization_planning_framework.md` - 商业系统策划框架 [权重3%]
  - `templates/guides/narrative_coherence_framework.md` - 剧情连贯性评估框架 [权重10%]
  - `templates/guides/system_architecture_framework.md` - 系统架构合理性评估框架 [权重5%]
  - `templates/guides/enhanced_gdd_structure_integration.md` - 整合指南
- **核心爽点循环设计**: 基于浓缩理论的核心体验设计框架 [权重8%]
  - 第3章Game Overview添加3.1.1核心爽点循环设计
  - 包含核心爽点识别、浓缩策略、质变突破、双循环结构设计
- **世界观设计工具链**: 基于天美工作室群工业化经验的世界观设计体系 [权重6%]
  - 第5章添加5.1世界观设计工具链
  - 包含体验目标设计、世界设定工具、叙事设计框架、叙事载体层级
- **AI辅助设计系统**: 集成人工智能工具的设计决策支持系统 [权重10%]
  - 新增第14章AI-Assisted Design
  - 包含好玩浓度测试器集成、世界观AI助手、设计质量AI评估
- **游戏类型适配模块**: 针对不同游戏类型的专门化设计指导 [权重20%]
  - 新增第15章Game Type Adaptation
  - 包含快节奏动作、策略、叙事、多人在线、卡牌、模拟经营、消除、放置、恋爱养成等类型适配
- **商业化分层设计**: 完善的用户分层商业化体系
  - 第4章添加用户分层设计体系、分层体验设计、分层付费策略
  - 包含非R、小R、中R、大R四类用户的完整策略
- **游戏类型核心模块设计**: 基于游戏类型的系统架构设计框架
  - 第4章添加基于游戏类型的模块化架构
  - 包含8大游戏类型的核心模块定义和关键指标
- **量化评估体系**: 为每个策划sub section提供科学的评分标准和检查清单
- **工业化生产模板**: 包含设计模板、公式定义、测试用例、迭代流程
- **中英文版本同步**: 更新docs/zh和docs/en文件夹中的实际GDD文档

### Changed
- **第3章 Game Overview**: 
  - 中英文版添加3.1.1核心爽点循环设计，基于浓缩理论的完整设计框架
- **第4章 Gameplay and Mechanics**: 
  - 中文版添加4.1.2任务系统架构、4.2.5.1技能系统架构、4.2.6.4商业系统架构、4.2.7.1数值系统架构
  - 英文版同步添加相同的细化内容
  - 重构4.2.7.2为基于游戏类型的系统架构设计，摒弃WBS方法
  - 添加完整的商业化分层设计体系和用户分层策略
- **第5章 Story, Setting and Character**:
  - 中文版重构为5.1世界观设计工具链，包含完整的工业化设计体系
  - 英文版同步添加相同的世界观设计工具链
  - 原有5.1.3.1剧情连贯性评估体系整合到新框架中
- **第9章 Technical**:
  - 中文版添加9.1系统架构设计体系，包含架构分层、模块化设计、性能优化等
  - 英文版同步添加相同的系统架构评估框架
- **新增第14章 AI-Assisted Design**: 
  - 中英文版添加完整的AI辅助设计系统
  - 包含好玩浓度测试器、世界观AI助手、设计质量AI评估等模块
- **新增第15章 Game Type Adaptation**: 
  - 中英文版添加完整的游戏类型适配模块
  - 包含8大游戏类型的专门化适配和混合类型处理
- **权重分配体系**: 实现游戏玩法逻辑性15%、剧情连贯性10%、系统架构合理性5%的科学分配
- **系统架构设计方法**: 从WBS工作分解结构改为基于游戏类型的设计方法

### Fixed
- **文档一致性**: 确保中英文版本内容完全对应，保持相同的评估标准和权重体系
- **结构完整性**: 将原本独立的框架文件实际应用到docs文件夹的GDD文档中
- **框架通用性**: 解决重生系统等特定模块的通用性问题，改为基于游戏类型的灵活选择
- **设计方法**: 修正WBS项目管理方法为游戏设计理论方法，提高框架的专业性和针对性

## [1.2.0] - 2026-01-28

### Added
- **Role Responsibility Matrix**: Created `templates/guides/role_responsibility_matrix.md` to map GDD templates to specific team roles (Design, Art, Tech, Marketing, PM, etc.).
- **GDD Deliverable Structure**: Created `templates/guides/gdd_deliverable_structure.md` to define the standard directory structure for game design deliverables.
- **Workflow Guide**: Created `templates/guides/idea_to_playable_workflow.md` providing a step-by-step guide from initial idea to MVP video and playable ad.

### Changed
- **Documentation Index**: Updated `docs/README.md` to include references to the newly created guides.
- **Role Matrix Expansion**: Expanded `role_responsibility_matrix.md` to include specialized roles:
    - Numerical / Balance Designer
    - Monetization / Economy Designer
    - IP Architect / World Director
    - Technical Marketing Manager
    - Outsourcing Manager
    - Localization Manager
    - User Researcher
    - Solutions Architect
    - Scrum Master
    - Design Validator / QA Director

### Fixed
- N/A
