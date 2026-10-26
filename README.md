# Visual Design Reasoning

**语言 / Language：** [简体中文](README.md) | [English](README_EN.md)

Visual Design Reasoning 是一个面向 Codex 的通用视觉设计推理 Skill，用于分析视觉参考、探索与深化设计方向、发现设计冲突，并将需求组织成可执行的图像或视频创作指令。

**[下载 V1.0.0](https://github.com/muxinMX/visual-design-reasoning/releases/tag/v1.0.0)**

## 它解决什么问题

视觉任务常常混合了观察、判断、创意探索、方案深化、提示词编写和媒体执行。这个 Skill 会先识别用户当前真正需要的阶段，再调用最小必要的方法模块，避免在“只分析”时提前出方案，也避免在用户只要提示词时强制走完一套流程。

它尤其适合以下情况：

- 从一张或多张参考图中提取结构、风格、色彩、材质、构图、光影和可迁移规律；
- 生成一个方案或多个有实质差异的视觉方向，并比较取舍；
- 在不破坏已确认设定的前提下继续深化方案；
- 规划角色保真、局部修改、风格转换和多图合成；
- 直接生成、压缩或优化图像与视频提示词；
- 识别互相冲突、物理上不合理或难以执行的设计要求，并给出最小可行调整。

## 适用人群与领域

适合角色、插画、概念、场景、平面、品牌、包装、产品、建筑与空间设计师，3D 艺术家、动画创作者，以及使用 AI 辅助视觉创作的普通用户。

可处理的视觉领域包括角色与主体、产品与系列、品牌和图形系统、世界观与场景、建筑与空间、构图与镜头、姿势与动作、灯光与氛围、图像编辑、多图合成，以及静态图转动画的动作规划。

本 Skill 不绑定固定画风、媒介或生成工具，也不会默认添加卡通角色、电影感 3D、高饱和、固定画幅、特定工作室风格或 Midjourney 语法。

## 主要功能与 20 种方法体系

20 种方法被整理为五个维护模块；公开使用时通常按目标自动路由，无须记忆方法编号。

| 方法 | 能力 | 主要模块 |
|---:|---|---|
| 01 | 图像逆向分析 | Visual Analysis |
| 02 | 风格 DNA 提取 | Visual Analysis |
| 03 | 多参考风格融合 | Visual Analysis |
| 04 | 角色或主体视觉结构分析 | Visual Analysis |
| 05 | 概念到角色设计 | Design Reasoning |
| 06 | 基础形态 IP 延展 | Design Reasoning |
| 07 | 角色变体设计 | Design Reasoning |
| 08 | 世界观设计 | Design Reasoning |
| 09 | 多角色关系设计 | Design Reasoning |
| 10 | 从主体推导场景创意 | Design Reasoning |
| 11 | 构图与镜头分析 | Composition and Motion |
| 12 | 多主体构图 | Composition and Motion |
| 13 | 姿势与动作设计 | Composition and Motion |
| 14 | 灯光与氛围设计 | Composition and Motion |
| 15 | 身份保真延展 | Image Editing and Synthesis |
| 16 | 局部修改 | Image Editing and Synthesis |
| 17 | 风格转换 | Image Editing and Synthesis |
| 18 | 多图提取与合成 | Image Editing and Synthesis |
| 19 | 静态图转动画规划 | Composition and Motion |
| 20 | 提示词优化 | Prompt Generation |

质量检查作为跨模块能力，负责核对阶段、证据与推断、设计一致性、空间和物理逻辑、原创性、工具边界及可执行性。完整映射见 [`references/method-map.md`](references/method-map.md)。

## 五阶段工作流程

| 阶段 | 作用 | 关键边界 |
|---|---|---|
| **Analyze** | 观察、拆解和讨论视觉问题 | 可指出必要的风险与最小调整，但不擅自进入完整方案探索或提示词输出 |
| **Explore** | 发展一个或多个尚未确认的方向 | 用户要单方案时只发展一个；只有用户要求多个方向或比较时，才必须提供实质不同的方案 |
| **Refine** | 深化已经选定的方向 | 保留已确认的身份、关系、构图与约束，不静默替换核心概念 |
| **Prompt** | 将现有需求或已确认方案转换为提示词 | 可由用户直接进入，不要求先完成 Analyze、Explore 或 Refine |
| **Execute** | 实际生成或编辑媒体 | 仅在用户明确授权且当前环境有合适媒体工具时进入 |

五个阶段是工作模式，不是必须依次完成的流水线。混合任务按主要交付物判断阶段；例如，“分析冲突并给出最小修正”仍可属于 Analyze。

## 版本、下载与安装

### V1.0.0 Release

[V1.0.0 Release](https://github.com/muxinMX/visual-design-reasoning/releases/tag/v1.0.0) 是正式稳定发布包，用户可以直接下载其中的 Skill ZIP 进行安装。该发布包是发布时的历史快照，不应理解为已经包含此后在 `main` 分支新增的英文文档或元数据调整。

### main 分支

[`main` 分支](https://github.com/muxinMX/visual-design-reasoning) 是目前持续维护的仓库源码，包含 V1.0.0 发布后新增的国际化文档与元数据修改，可用于查看最新文档或手动安装。`main` 分支不是一个新的 Release，也不代表其中每次文档更新都经过了完整的重新测试。

无论使用发布包还是从 `main` 分支手动安装，都应得到名为 `visual-design-reasoning` 的文件夹，并确保 `SKILL.md` 位于该文件夹根目录。如果下载的 `main` 源码目录带有分支后缀，请在安装前将目录重命名为 `visual-design-reasoning`。

### Windows（用户级）

1. 下载并解压 ZIP，得到 `visual-design-reasoning` 文件夹。
2. 打开 Windows 文件资源管理器，在地址栏输入：

   `%USERPROFILE%\.codex\skills\`

3. 如果目录不存在，请先创建。
4. 将整个 `visual-design-reasoning` 文件夹复制到 `skills` 目录内。

最终确保：

`%USERPROFILE%\.codex\skills\visual-design-reasoning\SKILL.md`

### macOS（用户级）

1. 下载并解压 ZIP，得到 `visual-design-reasoning` 文件夹。
2. 打开用户级 Skills 目录：

   `~/.codex/skills/`

3. 如果目录不存在，可在终端执行：

   `mkdir -p ~/.codex/skills`

4. 将整个 `visual-design-reasoning` 文件夹放入 `skills` 目录。

最终确保：

`~/.codex/skills/visual-design-reasoning/SKILL.md`

安装完成后，重新启动 Codex。

**注意：** 不要重复嵌套同名文件夹，`SKILL.md` 必须直接位于 `visual-design-reasoning` 文件夹内。

## 调用方式

### 自动调用

在允许隐式调用的 Codex 环境中，直接描述视觉设计任务即可。例如：

```text
分析这张参考图的构图、材质和视觉风格，先不要写提示词。
```

自动调用由环境根据 Skill 名称、description 与任务内容决定，并不保证每个媒体请求都必须经过本 Skill。纯粹的裁切、格式转换、压缩等不需要设计判断的技术操作不属于本 Skill。

### 手动调用

显式输入 Skill 名称：

```text
$visual-design-reasoning 帮我分析这个视觉 brief，并发展一个适合的设计方向。
```

## 案例展示：2 头身角色的造型与动作可行性分析

以下是用于说明阶段控制与分析能力的**示例工作流**，不是对某次模型调用、测试输出或通过率的陈述。

| 项目 | 内容 |
|---|---|
| 输入需求 | 一个风格化 3D 角色只有两头身、四肢很短，但需要完成奔跑、攀爬和持握等复杂动作；先分析结构冲突，暂不生成图片和提示词。 |
| Skill 识别的阶段 | **Analyze** |
| 主要分析维度 | 轮廓识别、动作范围、关节空间、3D 制作可行性 |
| 输出类型 | 设计冲突分析、风险说明和最小可行调整建议 |
| 阶段控制 | 保持在 Analyze，不擅自进入 Prompt 或 Execute |

## 典型使用示例

### 角色分析

```text
$visual-design-reasoning 分析这张角色参考的轮廓、比例、服装层级和识别点。区分可见事实与推测，只分析，不生成方案或提示词。
```

### 产品探索（单方案）

```text
$visual-design-reasoning 为这款桌面音箱发展一个低视觉噪声、适合小户型的单一设计方向。说明形态、交互、材料与量产取舍，不要补充其他备选方案。
```

### 场景设计（多方案）

```text
$visual-design-reasoning 基于这个故事设定提出三个结构上明显不同的车站场景方向，比较空间组织、叙事焦点、光线和制作成本。
```

### 局部编辑提示词

```text
$visual-design-reasoning 为这张图写局部编辑提示词：只把角色的红色外套改为深蓝色防水面料，保持脸、体型、姿势、构图、背景、光向和其他服装不变。只输出提示词，不执行编辑。
```

### 设计冲突分析

```text
$visual-design-reasoning 分析“极薄悬挑结构、完全无支撑、真实重型石材、可长期户外使用”之间的冲突，说明视觉与工程影响，并提出最小可行调整。保持在分析阶段。
```

### 直接图像或视频提示词

```text
$visual-design-reasoning 直接写一段工具中立的产品主视觉提示词，主题是可折叠旅行灯；不需要先做方案探索。
```

```text
$visual-design-reasoning 把已确认的角色动作整理成 6 秒图生视频提示词，包含预备、发力、主动作、跟随和结束定格，并保持身份、服装和背景连续。
```

## 功能边界与媒体工具依赖

已验证的核心能力包括：视觉参考分析；单方案与多方案探索；已确认方案深化；图像及视频创作指令组织；直接图像提示词；局部编辑提示词；设计冲突分析与批判性建议；以及对非视觉设计任务和纯技术图像操作的隔离。

需要特别区分“创作指令”与“实际媒体执行”：

- 本 Skill 可以独立完成分析、设计推导、编辑规划和提示词编写；
- 实际生成或编辑图像、视频，依赖 Codex 当前环境中可用的专用媒体工具及用户授权；
- Imagegen 已被独立验证可完成真实图片生成和局部编辑；
- Visual Design Reasoning 与 Imagegen 的联合调用链尚未完成完整端到端验证，因此不能将 Imagegen 单独执行成功视为本 Skill 的 Execute 全链路已通过；
- 用户直接请求媒体生成时，系统可以选择当时最合适的专用工具，不要求每次都先调用本 Skill；
- 未明确授权生成或编辑媒体时，本 Skill 不进入 Execute；即使用户明确授权，缺少合适工具时也只应说明限制，不假称已执行；
- 提示词提升的是约束表达与可执行性，不能保证生成结果完全确定。

本版本不保存个人风格、工具偏好或项目资料，不提供个性化记忆、固定个人工作流或 V1.1 规划中的个性化功能。

## 项目结构

```text
visual-design-reasoning/
├── SKILL.md
├── README.md
├── README_EN.md
├── LICENSE
├── agents/
│   └── openai.yaml
├── references/
│   ├── visual-analysis.md
│   ├── design-reasoning.md
│   ├── composition-motion.md
│   ├── image-editing.md
│   ├── prompt-generation.md
│   ├── quality-check.md
│   └── method-map.md
└── templates/
    ├── visual-analysis.md
    ├── image-prompt.md
    └── video-prompt.md
```

## 许可证

本项目采用 MIT License，详见 [`LICENSE`](LICENSE)。

## 反馈与建议

如果遇到安装问题、Skill 调用失败、阶段控制问题，或希望提出改进建议，请通过 [GitHub Issues](https://github.com/muxinMX/visual-design-reasoning/issues) 反馈。建议尽可能附上 Codex 环境、可复现任务、预期行为和实际观察结果。

## V1.0 版本说明

V1.0 是首个公开版本，固定了 20 种方法体系、五阶段工作模式、按需模块路由、单方案与多方案边界、直接提示词入口、媒体执行授权边界、设计冲突检查，以及工具与风格中立原则。

本版本的目标是稳定、通用和可解释，不包含个人 IP、固定艺术风格、个人工作流程或 V1.1 个性化能力。
