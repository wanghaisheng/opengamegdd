# GDD 交付物目录结构说明 (GDD Deliverable Structure)

当一个全新的游戏创意（Game Idea）经过策划与设计，最终形成的**游戏设计文档（GDD）交付物**通常是一个包含结构化文档、资源列表和参考素材的完整文件夹。

本文档定义了标准的 GDD 交付物目录结构，以及每个文件应包含的核心内容。

---

## 1. 推荐目录结构 (Directory Structure)

我们建议采用 **"主文档 + 附件资源 + 生产清单"** 的三层结构。

```text
[GameName]_Project_GDD/
├── README.md                       # 项目导航页（入口文件）
├── 00_ChangeLog.md                 # 变更日志 (对应模板 2_Version History)
├── docs/                           # 核心设计文档 (Markdown)
│   ├── 01_Overview.md              # 游戏概述 (对应模板 3_Game Overview)
│   ├── 02_Gameplay.md              # 核心玩法 (对应模板 4_Gameplay...)
│   ├── 03_Story_Characters.md      # 剧情与角色 (对应模板 5_Story...)
│   ├── 04_Levels.md                # 关卡设计 (对应模板 6_Levels)
│   ├── 05_UI_Interaction.md        # 界面交互 (对应模板 7_Interface)
│   ├── 06_AI_Systems.md            # AI设计 (对应模板 8_Artificial Intelligence)
│   ├── 07_Art_Style.md             # 美术风格 (对应模板 10_Game Art)
│   ├── 08_Technical.md             # 技术架构 (对应模板 9_Technical)
│   ├── 09_Audio.md                 # 音频设计 (集成在 10_Game Art 或独立)
│   └── 10_Business_Ops.md          # 商业与运营 (对应模板 12_Management)
├── production/                     # 生产与执行文档
│   ├── asset_lists/                # 资产需求清单
│   │   ├── asset_list_master.csv   # 总资产表
│   │   ├── character_assets.csv    # 角色资产拆分表
│   │   └── ui_assets.csv           # UI资产拆分表
│   ├── storyboards/                # 分镜与脚本
│   │   ├── intro_cutscene.md       # 开场动画分镜
│   │   ├── gacha_animation.md      # 抽卡演出分镜
│   │   └── mvp_gameplay.md         # MVP视频分镜
│   └── schedules/                  # 排期与进度
├── references/                     # 参考资料
│   ├── images/                     # 嵌入文档的图片/图表
│   ├── moodboard/                  # 情绪板/参考图
│   └── literature/                 # 参考文献/IP原始资料
└── legal/                          # 法律与版权
    └── copyright_info.md           # (对应模板 1_Copyright Information)
```

---

## 2. 核心文档内容详解 (File Contents)

### `README.md` (项目导航)
*   **内容**: 项目代号、一句话介绍、最新版本号、核心文档的快速链接索引。
*   **作用**: 让新加入成员快速找到入口。

### `docs/01_Overview.md` (游戏概述)
*   **对应模板**: `3_Game Overview.md`
*   **核心内容**:
    *   游戏概念 (High Concept)
    *   独特卖点 (USP)
    *   目标受众 (Target Audience)
    *   平台与控制方式
    *   核心循环图 (Core Loop Diagram)

### `docs/02_Gameplay.md` (核心玩法)
*   **对应模板**: `4_Gameplay and Mechanics.md`
*   **核心内容**:
    *   玩家视角的流程 (Game Flow)
    *   角色控制与摄像机 (3C)
    *   核心机制 (战斗/解谜/建造等具体规则)
    *   系统循环 (经济/成长/社交)

### `docs/03_Story_Characters.md` (剧情与角色)
*   **对应模板**: `5_Story, Setting and Character.md`
*   **核心内容**:
    *   世界观背景 (World Building)
    *   故事大纲 (Story Synopsis)
    *   角色小传 (Character Bios)
    *   叙事传递方式 (Dialogue/Cutscenes)

### `docs/04_Levels.md` (关卡设计)
*   **对应模板**: `6_Levels.md`
*   **核心内容**:
    *   关卡流程图
    *   关卡编辑器需求
    *   典型关卡平面图 (Paper Prototyping)
    *   刷怪/事件机制

### `docs/05_UI_Interaction.md` (界面交互)
*   **对应模板**: `7_Interface.md`
*   **核心内容**:
    *   UI 流程图 (Screen Flow)
    *   HUD 布局说明
    *   菜单层级与交互逻辑
    *   控制映射表 (Key Mapping)

### `docs/07_Art_Style.md` (美术风格)
*   **对应模板**: `10_Game Art.md`
*   **核心内容**:
    *   美术风格定义 (Art Pillars)
    *   色彩规范 (Color Palette)
    *   角色/场景/UI 风格指南
    *   资产规格标准 (Asset Specs)

### `docs/08_Technical.md` (技术架构)
*   **对应模板**: `9_Technical.md`
*   **核心内容**:
    *   引擎选型与版本
    *   目标平台性能指标 (Performance Budget)
    *   代码架构规范
    *   数据存储方案

### `docs/10_Business_Ops.md` (商业与运营)
*   **对应模板**: `12_Management.md`
*   **核心内容**:
    *   变现策略 (Monetization)
    *   分析埋点需求 (Analytics)
    *   本地化计划 (Localization)

---

## 3. 生产目录内容 (Production Folder)

此文件夹包含直接指导生产的“可执行文件”。

### `production/asset_lists/`
*   **asset_list_master.csv**:
    *   基于 `docs/templates/asset_list_template.csv`。
    *   包含所有需要制作的资产 ID、类型、状态、优先级。
*   **用途**: 导入项目管理软件 (Jira/Trello) 生成任务单。

### `production/storyboards/`
*   **xxx_storyboard.md**:
    *   基于 `docs/templates/video_storyboard_template.md` 或 `universal_storyboard_method.md`。
    *   包含用于指导视频制作、过场动画或复杂交互的镜头表。

---

## 4. 交付物检查清单 (Deliverable Checklist)

在提交 GDD 交付物前，请确认：

- [ ] **完整性**: 所有核心章节（特别是玩法和概述）已由占位符替换为实际设计。
- [ ] **一致性**: 玩法文档中的机制与 UI 文档中的界面描述不冲突。
- [ ] **可执行性**: 资产清单已列出，且有明确的技术规格（面数/尺寸）。
- [ ] **视觉化**: 关键逻辑配有流程图，关键视觉配有参考图或草图。
- [ ] **版本号**: `00_ChangeLog.md` 已更新当前交付的版本信息。
