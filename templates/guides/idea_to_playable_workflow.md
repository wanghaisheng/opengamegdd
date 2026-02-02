# 从创意到试玩广告的全流程指南 (End-to-End Workflow: Idea to Playable Ad)

本文档提供了一条**从零开始**的完整路径：如何将一个游戏点子（Idea）转化为标准的设计文档（GDD），通过资产生产管线，最终产出无需代码开发的**视频化试玩广告 (Video-based Playable Ad)**。

这条路径特别适合在**立项初期**或**MVP验证阶段**，通过低成本的视频素材来测试市场反馈，而无需等待程序开发完整的游戏包体。

---

## 阶段一：创意结构化 (Phase 1: Idea to GDD)
**目标**：将模糊的想法转化为可执行的文档结构。

1.  **定义核心概念**
    *   使用 `templates/3_Game Overview.md` 填写游戏的核心循环 (Core Loop) 和独特卖点 (USP)。
    *   **输出**：`docs/01_Overview.md`

2.  **构建交付物目录**
    *   按照 **[GDD交付物结构指南](GDDMarkdownTemplate/templates/guides/gdd_deliverable_structure.md)** 创建项目文件夹。
    *   建立 `docs/`, `production/`, `references/` 三层结构。

3.  **核心玩法可视化**
    *   使用 **[通用分镜方法论](GDDMarkdownTemplate/templates/guides/universal_storyboard_method.md)** 将玩法机制转化为“关键帧”。
    *   **关键动作**：不要只写文字规则，要画出“玩家按下按钮后屏幕发生了什么”。

---

## 阶段二：资产拆解与生产 (Phase 2: Asset Breakdown & Production)
**目标**：将 GDD 转化为美术和音频素材。

1.  **建立资产清单**
    *   使用 **[资产清单模板](GDDMarkdownTemplate/templates/asset_list_template.csv)**。
    *   由策划拆解出所有需要的 UI 图片、角色立绘、场景图、音效。
    *   **角色分工**：参考 **[角色职责矩阵](GDDMarkdownTemplate/templates/guides/role_responsibility_matrix.md)** 分配任务。

2.  **制定生产规范**
    *   根据 **[资产提取指南](GDDMarkdownTemplate/templates/guides/asset_extraction_guide.md)** 确定文件格式和命名规则。
    *   **美术生产**：参考各类生产指南（如 `ui_element_production_guide.md`, `image_asset_production_guide.md`）。

3.  **特效与动效设计**
    *   对于技能特效，参考 **[特效格式讨论](GDDMarkdownTemplate/templates/guides/vfx_discussion.md)**，决定是使用序列帧还是视频素材。

---

## 阶段三：MVP 视频模拟 (Phase 3: The MVP Gameplay Video)
**目标**：在不写代码的情况下，通过视频编辑软件模拟真实的游戏体验。

1.  **MVP 视频策划**
    *   阅读 **[MVP 游玩视频指南](GDDMarkdownTemplate/templates/guides/mvp_gameplay_video_guide.md)**。
    *   设计一段 15-30 秒的“伪实机演示”脚本。

2.  **素材组装**
    *   将阶段二生产的静态 UI、角色图放入视频剪辑软件 (AE/Premiere)。
    *   按照 GDD 中的逻辑制作简单的位移动画、弹窗动画。
    *   **重点**：模拟真实的点击反馈（如点击按钮时的缩放、音效）。

3.  **输出线性视频**
    *   导出一个包含完整核心循环（进入战斗 -> 战斗过程 -> 结算奖励）的 MP4 视频。

---

## 阶段四：交互式试玩广告 (Phase 4: Playable Ad Construction)
**目标**：将线性视频转化为可交互的 H5 或视频广告。

1.  **设计交互节点**
    *   参考 **[试玩广告视频指南](GDDMarkdownTemplate/templates/guides/playable_ad_video_guide.md)**。
    *   将 MVP 视频切分为多个片段（Intro, Idle, Action, Win/Fail）。

2.  **定义跳转逻辑**
    *   **Idle 片段**：循环播放，等待用户点击。
    *   **Action 片段**：用户点击后播放攻击/反馈动画。
    *   **End Card**：播放结束后显示的下载引导页。

3.  **批量化变体 (可选)**
    *   如果需要测试不同的美术风格或文案，使用 **[API 视频生成指南](GDDMarkdownTemplate/templates/guides/api_video_generation_guide.md)** 批量生成多个版本的视频片段。

---

## 总结：全流程概览图

```mermaid
graph TD
    A[创意 Idea] -->|结构化| B(GDD文档)
    B -->|分镜设计| C[通用分镜方法]
    B -->|需求拆解| D[资产清单 Asset List]
    
    D -->|美术生产| E[图片/模型/音频素材]
    C -->|视频脚本| F[MVP视频分镜]
    
    E + F -->|视频剪辑| G[MVP线性演示视频]
    
    G -->|切片与逻辑| H[交互式试玩广告 Playable Ad]
    
    H -->|投放测试| I{市场数据反馈}
    I -->|数据好| J[正式立项开发代码]
    I -->|数据差| K[修改GDD/素材重测]
```
