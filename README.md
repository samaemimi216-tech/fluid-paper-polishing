# Fluid Paper Polishing

面向流体力学、计算流体力学与传热传质论文的 Codex 学术写作技能。它借鉴 [nature-skills](https://github.com/Yuan1z0825/nature-skills) 的动态路由和渐进加载设计，并根据 69 份本地论文 PDF 归纳物理条件、数值证据、论证结构、术语与期刊表达规范。

## 适用范围

- 计算流体力学、动理学方法、稀薄气体与多尺度流动
- UGKS、DUGKS、LBM、DSMC 等数值方法
- 传热传质、声子输运、辐射输运与共轭传热
- 多相流、颗粒流、燃烧与反应流
- 湍流、孔隙尺度输运、浸入边界与界面流
- 数据驱动流体建模、稀疏闭合与流体机器学习
- 数值、实验、理论和综述论文
- 中文草稿英译、英文润色、章节重构和术语统一

支持标题与摘要、引言、控制方程、数值或实验方法、验证与确认、结果与讨论、结论以及图表说明。

## 核心特点

- 按 `贡献类型 × 研究类型 × 章节 × 语言 × 期刊 × 物理领域` 自动选择规则。
- 区分方法开发、物理发现、公平比较、综述综合和数据驱动建模的论证结构。
- 区分连续模型、离散方法、验证、确认和物理解释。
- 检查守恒性、精度阶、稳定性、正性、渐近保持、网格无关性及计算效率等声明是否具有对应证据。
- 检查强/弱扩展、平衡保持、数据泄漏、跨工况泛化及物理约束等新型声明。
- 统一变量、缩写、无量纲数、流动区域和方法名称。
- 保留公式、数据、引文、图表编号和 LaTeX 命令。
- 缺少必要信息时生成作者问询，不虚构参数、结论、机制或参考文献。

## 安装

Codex 会从个人目录 `$HOME/.agents/skills` 或项目目录 `.agents/skills` 发现技能。详见 OpenAI 的 [Agent Skills 文档](https://developers.openai.com/codex/skills)。

### 方法一：让 Codex 安装

在 Codex 中输入：

```text
Use $skill-installer to install the skill from https://github.com/samaemimi216-tech/fluid-paper-polishing.git
```

### 方法二：Windows 全局安装

该方式会让技能对当前用户的所有项目生效：

```powershell
New-Item -ItemType Directory -Force "$HOME\.agents\skills"
git clone https://github.com/samaemimi216-tech/fluid-paper-polishing.git "$HOME\.agents\skills\fluid-paper-polishing"
```

### 方法三：项目内安装

在目标项目根目录执行：

```powershell
New-Item -ItemType Directory -Force ".agents\skills"
git clone https://github.com/samaemimi216-tech/fluid-paper-polishing.git ".agents\skills\fluid-paper-polishing"
```

Codex 通常会自动检测新增技能。如果技能没有出现，请重启 Codex。

## 使用

显式调用最稳定。在提示词中写出 `$fluid-paper-polishing`，然后提供章节类型、目标期刊和原文。

### 润色英文摘要

```text
Use $fluid-paper-polishing to polish the following abstract for Journal of Computational Physics.
Preserve all technical claims and check whether the accuracy and efficiency statements are adequately bounded.

[粘贴摘要]
```

### 中文引言翻译与重构

```text
使用 $fluid-paper-polishing 将下面的中文引言改写为适合 International Journal of Heat and Mass Transfer 的英文。
保留引文编号，突出物理问题、现有方法的限制和本文贡献，不要虚构结果。

[粘贴引言]
```

### 检查数值验证部分

```text
使用 $fluid-paper-polishing 审查下面的 verification and validation 部分。
检查网格无关性、精度阶、守恒误差、比较基准和计算效率是否足以支持文中的声明。

[粘贴正文]
```

### 润色结果与讨论

```text
Use $fluid-paper-polishing to revise this Results and Discussion section.
Separate observations from mechanisms, retain all numerical values, and flag unsupported causal explanations.

[粘贴正文]
```

### JFM 物理问题导向润色

```text
Use $fluid-paper-polishing to revise this manuscript for Journal of Fluid Mechanics.
Lead with the fluid-mechanical question, retain all nondimensional ranges, and separate the observed structure from the proposed mechanism.

[粘贴正文]
```

### 数据驱动流体论文

```text
使用 $fluid-paper-polishing 润色下面的数据驱动湍流建模摘要。
检查数据来源、训练/验证/测试划分、跨雷诺数泛化、物理约束和不确定性声明。

[粘贴摘要]
```

### 全文统一

```text
使用 $fluid-paper-polishing 对这篇流体论文进行全文一致性检查。
先建立术语与符号账本，再按章节润色，并列出需要作者补充的信息。

[提供论文文件或正文]
```

## 建议提供的信息

为了得到更准确的结果，建议同时提供：

- 章节类型和目标期刊
- 研究类型：数值、实验、理论或综述
- 主要物理问题与适用流动区域
- 核心贡献、主要证据和适用边界
- 需要保留的术语、符号、缩写和 LaTeX 格式
- 期刊字数或格式限制

## 默认输出

技能通常返回：

1. `Polished text`：润色后的正文；
2. `Revision notes`：结构、术语、证据与期刊适配说明；
3. `Author queries`：影响科学正确性或可复现性的缺失信息；
4. 对较大修改附加简短的声明—证据对应关系。

## 支持的路由

| 维度 | 当前选项 |
|---|---|
| 贡献类型 | method-development、physical-investigation、comparative-assessment、review-synthesis、data-driven-modeling |
| 研究类型 | numerical、experimental、theoretical、review |
| 章节 | title、abstract、introduction、formulation-methods、verification-validation、results、discussion、results-discussion、conclusion、captions |
| 语言 | en、zh-to-en |
| 期刊 | JCP、JFM、Physics of Fluids、Physical Review Fluids、IJHMT、PRE、PECS、generic |
| 物理领域 | general-fluids、kinetic-rarefied、heat-radiation、multiphase-reacting、interfacial-porous、turbulence-data-driven |

## 项目结构

```text
fluid-paper-polishing/
├── SKILL.md                 # 技能入口与执行协议
├── manifest.yaml            # 动态路由配置
├── agents/openai.yaml       # Codex UI 元数据
├── static/                  # 始终加载或按路由加载的规则
│   ├── core/
│   ├── contribution-types/
│   ├── study-types/
│   ├── sections/
│   ├── language/
│   └── journals/
└── references/              # 按需加载的流体领域参考规则
```

## 更新

如果通过 Git 克隆安装，可执行：

```powershell
git -C "$HOME\.agents\skills\fluid-paper-polishing" pull
```

## 语料基础与边界

本技能参考了开发目录中的 69 份流体、传热和辐射输运论文 PDF，其中新增 40 份语料。代表性期刊包括 *Journal of Computational Physics*、*Journal of Fluid Mechanics*、*Physics of Fluids*、*Physical Review Fluids/E*、*International Journal of Heat and Mass Transfer* 与 *Progress in Energy and Combustion Science*。语料仅用于总结论证结构、术语、证据边界和领域表达习惯，不复制论文原句或作者特有措辞。

本技能负责写作与科学表述检查，不替代作者对方程、代码、实验、数据、统计结果和参考文献的最终核验。
