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
- **量化评估体系**: 为每个策划sub section提供科学的评分标准和检查清单
- **工业化生产模板**: 包含设计模板、公式定义、测试用例、迭代流程
- **中英文版本同步**: 更新docs/zh和docs/en文件夹中的实际GDD文档

### Changed
- **第4章 Gameplay and Mechanics**: 
  - 中文版添加4.1.2任务系统架构、4.2.5.1技能系统架构、4.2.6.4商业系统架构、4.2.7.1数值系统架构
  - 英文版同步添加相同的细化内容
- **第5章 Story, Setting and Character**:
  - 中文版添加5.1.3.1剧情连贯性评估体系，包含时间连贯性、角色连贯性、世界观连贯性
  - 英文版同步添加相同的剧情连贯性评估框架
- **第9章 Technical**:
  - 中文版添加9.1系统架构设计体系，包含架构分层、模块化设计、性能优化等
  - 英文版同步添加相同的系统架构评估框架
- **权重分配体系**: 实现游戏玩法逻辑性15%、剧情连贯性10%、系统架构合理性5%的科学分配

### Fixed
- **文档一致性**: 确保中英文版本内容完全对应，保持相同的评估标准和权重体系
- **结构完整性**: 将原本独立的框架文件实际应用到docs文件夹的GDD文档中

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
