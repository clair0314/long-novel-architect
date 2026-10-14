# Popwave × Long-Novel-Architect

### 给网文作者的 Codex，从找创意到写成一部小说

**[🌊 在 Popwave 体验「七种经典写作技法流」→](https://popwave.cn/work/)** · [看网文 Daily](https://popwave.cn/work/daily) · [下载开源 Skill](#本地安装与使用)

有了一个想法，接下来还要判断它适合什么赛道、怎样搭出能持续推进的结构、如何写正文，以及写完后到哪里找投稿机会。**Popwave 把这些环节放进同一个网文创作工作区**：它能查资料、调用专业 Skill 和写作专家、推进小说项目，也能帮助作者把作品做成封面与漫画。

[![Popwave 网页版创作工作区：找创意、理大纲、写正文、拆热书与制作视觉素材](docs/popwave-work.png)](https://popwave.cn/work/)

## Popwave 能陪你做什么

| 创作阶段 | 在 Popwave 里可以做的事 |
|---|---|
| **找方向** | 搜索平台新书榜单、赛道变化与新元素；在 [Daily 网文情报站](https://popwave.cn/work/daily)查看不同平台和赛道的热力与变化，再决定写什么。 |
| **搭故事** | 从脑洞出发理大纲、建立人物与设定。调用网文 Skill，或选择雪花流、涌现流等写作专家，让方法跟着项目一起工作。 |
| **写与改** | 在小说项目中继续排章节、写正文；拆解参考作品的结构、节奏与文风，整理可供自己创作使用的写法。 |
| **找素材、做视觉** | 在[网文 Wiki](https://popwave.cn/work/knowledge)查写作素材与方法；为作品制作封面、人物视觉素材和漫画。 |
| **检查与寻找机会** | 使用[朱雀 AI 检测](https://popwave.cn/work/detect)查看正文的 AI 写作特征；在 [Daily 征稿情报](https://popwave.cn/work/daily)查平台征稿要求、投稿渠道和编辑联系方式。 |

Popwave 的写作方法由专业编辑与作者团队在工作室创作中验证，再将可复用的部分整理为 Skill 与专家模式。作者可以按题材与创作阶段选择方法，让专家依据故事项目继续工作。

**[进入 Popwave 工作区 →](https://popwave.cn/work/)** · [浏览 Skill 与专家](https://popwave.cn/work/skills) · [查看今日网文情报](https://popwave.cn/work/daily)

## 先跑起来：网页版直接体验，源码也可自行安装

**推荐在 Popwave 体验。**网页版提供内置的「七种经典写作技法流」，打开 [Popwave 工作区](https://popwave.cn/work/)登录并新建小说项目，就可以用自己的脑洞或 [Daily 趋势](https://popwave.cn/work/daily)开始结构推演。得到骨架后，继续在同一项目里选择写作专家，推进设定、章纲与正文。使用网页版不需要下载本仓库。

```text
打开 Popwave → 新建小说项目 → 使用「七种经典写作技法流」
              → 得到长篇结构稿 → 写作专家继续推进
```

在项目对话中可以这样开始：

> 请用「七种经典写作技法流」分析这个长篇脑洞。逐一诊断七种方法，选出主方法和辅助方法，给出全书节点、分卷任务及前三章目标；保留我已经确定的情节，新增内容标为提案。［粘贴脑洞］

**想独立运行或查看完整方法？**下载本仓库，将 `long-novel-architect/` 安装到支持 Skills 的本地 Agent。运行后可得到 Markdown 结构稿，也可以把这份结构稿带入 Popwave 项目。[查看本地安装步骤 →](#本地安装与使用)

## 我们开放的 Skill：长篇小说架构师

**Long-Novel-Architect 把七种经典写作结构变成可执行的诊断与推演流程。**输入一句脑洞、一份设定或一段市场信号，它会检查故事的因果、人物变化与连载动力，选择主辅方法，交付全书节点、分卷任务和前三章目标。

长篇最难的部分，往往从精彩开局之后开始：事件如何一环扣一环，人物凭什么改变，每一卷又如何产生新的目标？这份开源 Skill 展示了我们怎样把写作理论变成具体工作步骤。Popwave 中的体验名称是「七种经典写作技法流」；本仓库保留可独立安装的 Skill 文件、方法手册和试跑报告。

[七大结构矩阵](#七大结构诊断矩阵) · [执行流程](#技能执行流) · [完整试跑报告](long-novel-architect/examples/yapo-dalisi-output.md) · [在 Popwave 继续创作](#在-popwave-继续创作)

![七种小说叙事方法的原创工作示意图](docs/seven-structures.png)

> 图解由本仓库制作，表示七种方法的工作重点；曲线和节点不代表固定的篇幅比例。

## 设计哲学：先给长篇做压力测试

**一个好开头，需要一套能持续运作的故事机制。**本 Skill 从三个层面检查它：

1. **因果链**：关键事件是否由人物选择推动？删去一个节点，后面的故事会不会照样发生？
2. **人物线**：外部胜负是否改变人物的做法、关系或处境？如果人物保持稳定，这种稳定有没有持续接受考验？
3. **连载线**：每卷结束时，目标、资源、关系或规则是否真的发生变化？下一卷的任务从哪里长出来？

输入可以是一句话脑洞、一份已有设定，或一段市场趋势。Skill 会先记录作者已确定的内容，再诊断结构缺口；新补的案件、规则与人物关系会标明为**创作提案**。

```text
脑洞 / 已有设定 / 市场信号
             ↓
       七种方法逐项诊断
             ↓
       选择 1 主 + 至多 2 辅
             ↓
    全书因果链 → 分卷任务 → 前三章
             ↓
     中段续航与结局兑现检查
```

## 七大结构诊断矩阵

### 01｜故事骨架：转折要互相咬合

| 方法 | 执行动作 | 主要产物 |
|---|---|---|
| **七点故事结构** | 从终局反推起点、中点、两次转折与两次压力，逐点检查“前一步如何迫使下一步发生”。 | 七节点因果表 |
| **起承转合** | 安排起势、发展、信息转向与重新理解，让「转」改变前文的意义。 | 四段信息变化表 |
| **金字塔结构** | 排出引发事件、逐级加压、不可回头的高点与其后果。 | 卷级压力链 |

### 02｜连载动力：每次行动都改变处境

| 方法 | 执行动作 | 主要产物 |
|---|---|---|
| **冲突曲线** | 追踪行动、得失、代价与新目标，检查中段事件能否互换顺序。 | 多轮得失与升级表 |
| **救猫咪节拍** | 检查开篇承诺、中点变化、重大失去与最终兑现；作为主方法时展开完整十五节拍。 | 节拍功能表 |

### 03｜人物与扩写：让设想变成可写材料

| 方法 | 执行动作 | 主要产物 |
|---|---|---|
| **英雄之旅** | 追踪角色的旧位置、跨越门槛、接受考验和变化后的行动。 | 人物变化线 |
| **雪花写作法** | 从一句话梗概，逐层扩展人物、阶段故事和场景清单，后层发现问题时回改前层。 | 逐层设计文档 |

这些方法处于不同层级。Skill 会为同一个故事逐项写出**适用问题、具体动作、产出物与边界**，再说明为什么选定某个主方法。[查看完整方法手册与诊断路由 →](long-novel-architect/references/structure-guide.md)

## 技能执行流

### Step 1｜输入脑洞或市场信号

给出你已有的人物关系、强情节和结局约束即可。没有故事时，也可以先提供来自 [Popwave 网文情报站 Daily](https://popwave.cn/work/daily)的趋势摘要。Skill 会区分**原案、资料与新提案**；用户提供的趋势不会被写成已经独立核验的事实。

### Step 2｜七法交叉诊断，自动选择主轴

Skill 逐一检查分段、因果、压力、连续得失、人物变化、读者节拍与资料完整度。选择规则很具体：**优先处理最会阻断下一阶段写作的缺口**，再从其他层级挑选辅助方法。作者指定主方法时，按指定方法完整展开。

### Step 3｜交付长篇架构与续航预警

输出包含主方法的完整结构表、人物线、全书主问题、分卷目标、前三章任务，以及中段可能重复的环节。每卷必须说明**目标、行动、代价和导致下一卷的变化**。如果当前材料支撑不了长篇，报告会指出缺口，并给出可替换的事件线提案。

### Step 4｜带着结构稿继续写

结构稿采用普通 Markdown。在 Popwave 中运行时，可以接着让写作专家推进设定、剧情编排和章节写作；在本地 Agent 中运行时，可将结构稿与接力指令复制到 [Popwave 创作工作区](https://popwave.cn/work/)继续使用。

## 诊断与输出示例

下面是[试跑报告](long-novel-architect/examples/yapo-dalisi-output.md)的摘要；案例只用于展示技法如何做出结构决策。

```text
输入：市井牙婆女 × 守律的大理寺评事
原案锚点：婚讯南逃 → 山洪假死 → 多年后街市重逢

七法诊断：
  七点故事结构  强转折已具备，适合锁定全书因果链
  英雄之旅      双主角的关系位置与做法需要各自变化
  雪花写作法    案件、时间线和分卷资料仍需逐层展开

结构选择：七点故事结构为主；英雄之旅与雪花写作法为辅
续航预警：重逢之后缺少已确定的持续事件线
可选提案：以“身契疑案”连接女主的牙行经验与男主的办案职责
```

**[查看七种方法的逐项判断、七节点结构与前三章任务 →](long-novel-architect/examples/yapo-dalisi-output.md)**  
案例中的“身契疑案”是本次推演的提案，并非原案已有情节。

## 理论溯源与核心参数

七种方法的源流不同。本仓库提供自己的长篇应用流程，并把可核对的方法来源与改编边界列在一起。

| 方法 | 本 Skill 使用的核心参数 | 方法来源或边界 |
|---|---|---|
| **七点故事结构** | Hook、Plot Turn 1、Pinch 1、Midpoint、Pinch 2、Plot Turn 2、Resolution | [Dan Wells 的公开讲座](https://www.youtube.com/watch?v=KcmiqQ9NpPE) |
| **雪花写作法** | 一句话 → 一段式 → 角色动机 → 阶段梗概 → 场景清单 | [Randy Ingermanson 的十步说明](https://www.advancedfictionwriting.com/articles/snowflake-method/)；本 Skill 用其中的开书设计层 |
| **英雄之旅** | 离开 → 考验／启蒙 → 带着变化归来 | [Joseph Campbell Foundation 的说明](https://www.jcf.org/learn/joseph-campbell-heros-journey)；不强制套齐流行的小步骤 |
| **救猫咪节拍** | 十五节拍；开场、中点、重大失去与终场的对应 | [Save the Cat! 官方节拍工具](https://savethecat.com/beat-mapper)；长篇应用为本仓库改编 |
| **金字塔结构** | 初始局面、加压、高点与后果 | [Freytag《戏剧的技巧》](https://www.gutenberg.org/ebooks/50616)；在此用于卷级压力检查 |
| **起承转合** | 起、承、转、合四段的信息变化 | 参照[相关的起承転結研究](https://textjournal.scholasticahq.com/article/146391-kishotenketsu-and-its-potential-applications-to-prose-writing)；不将两者完全等同 |
| **冲突曲线** | 行动 → 得失 → 处境变化 → 新目标 | 本仓库的工作定义，不声称存在唯一的原版曲线 |

完整操作表、验收项和来源说明见[方法手册](long-novel-architect/references/structure-guide.md)。

## 本地安装与使用

下载此仓库后，在仓库根目录将整个 Skill 文件夹放进支持 Skills 的 Agent 目录。以 Codex 为例：

```bash
cp -R long-novel-architect ~/.codex/skills/
```

然后输入：

> 用 long-novel-architect 分析我的长篇脑洞。让七种方法逐一诊断，选出主方法，交付全书节点、分卷推进和前三章任务。保留我已确定的情节，新增内容标为提案。［粘贴脑洞］

也可以指定“以起承转合作为主方法”，或只要求比较七种技法。Skill 的完整执行规则在 [SKILL.md](long-novel-architect/SKILL.md)。

## 在 Popwave 继续创作

**已经在 Popwave 使用「七种经典写作技法流」？**留在当前小说项目，接着选择适合的写作专家推进设定、剧情、章纲和正文。本案例可由「雪花流写作专家」继续处理。

**在本地运行了开源版？**打开 [Popwave 创作工作区](https://popwave.cn/work/)新建小说项目，把结构稿与[接力指令](long-novel-architect/examples/yapo-dalisi-output.md#交给-popwave-的下一步)粘贴进去，再让写作专家接力。

| 你现在需要 | Popwave 中的入口 |
|---|---|
| 还没有确定写什么 | [Daily 趋势与扫榜](https://popwave.cn/work/daily)看平台、赛道和元素的变化，再带着信号使用本 Skill。 |
| 已经有故事骨架 | [Work 小说项目](https://popwave.cn/work/)中继续理大纲、写正文，按需要选择[网文 Skill 与专家](https://popwave.cn/work/skills)。 |
| 写作时缺资料或参考 | 到[网文 Wiki](https://popwave.cn/work/knowledge)找设定、素材和技法，也可以在工作区拆解参考作品。 |
| 正文完成，准备呈现与投稿 | 制作封面或漫画，用[朱雀 AI 检测](https://popwave.cn/work/detect)查看文本特征，并在 [Daily 征稿情报](https://popwave.cn/work/daily)查可用渠道。 |

**[🌊 打开 Popwave 网页版，从一个脑洞开始写 →](https://popwave.cn/work/)**

## 仓库目录

```text
README.md
LICENSE                                      MIT 开源许可
docs/seven-structures.png                     七种方法总览图
docs/popwave-work.png                          Popwave 网页版工作区截图
long-novel-architect/
├── SKILL.md                                   执行流程与交付门槛
├── references/structure-guide.md              七种方法的操作、验收与来源
└── examples/
    ├── yapo-dalisi-input.md                   案例输入边界
    └── yapo-dalisi-output.md                  完整试跑报告
```

## 许可

本仓库以 [MIT 许可证](LICENSE)开放使用。
