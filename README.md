# 长安都柏林车辆工程.skill

一个面向 **本科传统车辆工程 / 机械车辆工程方向** 的 Codex Agent Skill 项目。

这个项目用于沉淀本科四年车辆工程课程体系、课程复习方法、课件索引、题库、公式库、考试复习包，以及求职简历、面试、PPT 中的专业基础表达。

> 内部调用名：`$undergraduate-vehicle-engineering-learning`  
> 显示名称：`长安都柏林车辆工程.skill`
>
> 各位都柏林车辆的学弟学妹们大家好。
这是一个个人兴趣探索类项目，本科四年的生活让我印象深刻，同时四年的课程也让我痛不欲生。按照我自己的感受，课程是离散的，考试是连续的，听课是如懂的，自习是不会的。我的四年很忙，但是我真正学到了什么，不知道。而且在我与其他同学交流的过程中，我发现有同感的同学很多很多。

人们常说科学技术是第一生产力，那么，我不禁思考，我们是否可以利用当前的AI技术，将我们从这种重复的、低价值的劳动中解放出来，从而有更多的时间去深耕兴趣技能，用心感受生活。

为此，我整理了我四年的全部资料，把过去四年的自己 蒸馏了出来，做成了如你们所见的skill。
它已经内嵌了课程大纲、知识点等；配合各科课件，能够直接生成复习重点、抓取课上习题，自动生成详细的中英解题过程，寻找教材中的类似习题，甚至模拟考试问答——所有功能都基于我真实的学习轨迹训练而成。

我始终认为这并非投机取巧，而是合理精简无用内耗。很多课程考完试便再无用处，实在没必要耗费大把时间反复老旧课件。依照学习边际效应，我们往往要耗费八成精力，才能吃透最后两成细碎知识点，这类无意义的过度复盘本就大可不必。

但是，那么受限于本人在同年级本专业路边一条的学习能力和工程能力，我不认为使用该skill可以让你的成绩在一夜之间突飞猛进，他的作用更多像是能保证你在从零开始时快速上手，辅助你在打好整个课程基础后查漏补缺锦上添花，和自动化处理工作不同，学习新知还是要我们自身的理解与思考。

当前的skill还是一个残血版，只针对春季的考试科目如热力学系列课程，流体力学系列课程、Anton系列课程、电子电工、程序设计、大学物理等进行了部分针对性优化。

由于本人的经历、脑洞、学习能力都十分有限，这个skill肯定有若干不尽如人意的地方，后续我将持续优化，也欢迎各位志同道合、学有余力、脑洞大开的同学们私信我提供想法和建议等，让我不断丰富该skill，我在项目文件中也增加了一份问卷，希望大家能够扫码填写，给予我最真实的反馈。同时也欢迎道桥、交运的同学参与进来，针对性编写其他两个专业的skill。最后，感谢大家的点赞与关注！

## 项目目标

本项目希望把传统车辆工程本科阶段的学习内容整理成一个可持续扩展的 Codex skill，使它能够：

- 梳理本科传统车辆工程课程体系
- 根据课程表构建知识地图
- 读取课件、教材、作业、试卷、答案等素材
- 建立课程索引
- 抽取重点习题
- 分步解答习题
- 构建题库
- 构建公式库
- 生成考试复习包
- 将本科课程、课程设计和工程训练转化为简历、面试、求职 PPT 表达
- 用更基础、更细致的方式解释公式、概念、工程问题和学习方法

## 适用范围

本 skill 只面向本科阶段的传统车辆工程 / 机械车辆工程课程体系。

适合处理的内容包括：

- 数学与自然科学基础
- 程序设计
- 大学物理
- 工程力学
- 应用动力学
- 热力学
- 流体力学
- 机械控制工程
- 电工电子技术
- 液压与气动传动
- 材料与制造
- 汽车构造
- 汽车设计
- 发动机
- 车辆动力学
- 新能源汽车基础
- 本科课程设计与工程训练

## 明确边界

本项目不会、也不应该用于虚构经历。

使用时必须遵守：

- 不添加研究生阶段内容
- 不添加自动驾驶研究内容
- 不添加强化学习、SUMO、PPO、DQN、LLM 相关内容
- 不虚构课程、项目、竞赛、奖项、成绩、实习或科研经历
- 没有素材时，不假装读取过课件
- 没有证据时，用 `TODO` 标注
- 课件题目、页码、老师重点、考试高频点必须基于用户上传材料

## 当前项目结构

```text
.
├── .agents/
│   └── skills/
│       └── undergraduate-vehicle-engineering-learning/
│           ├── SKILL.md
│           ├── agents/
│           │   └── openai.yaml
│           ├── assets/
│           │   ├── course-review-template.md
│           │   ├── courseware-index-template.md
│           │   ├── exam-qa-template.md
│           │   ├── exam-review-package-template.md
│           │   ├── exercise-bank-template.md
│           │   ├── formula-bank-template.md
│           │   ├── formula-summary-template.md
│           │   ├── interview-answer-template.md
│           │   ├── knowledge-map-template.md
│           │   ├── material-upload-checklist-template.md
│           │   └── resume-course-expression-template.md
│           └── references/
│               ├── 00-user-background.md
│               ├── 01-undergraduate-course-map.md
│               ├── 02-study-methods.md
│               ├── 03-core-vehicle-engineering-knowledge.md
│               ├── 04-course-review-rules.md
│               ├── 05-projects-and-experience-template.md
│               ├── 06-weaknesses-and-learning-needs.md
│               ├── 07-online-search-rules.md
│               ├── 08-courseware-index-and-ingestion.md
│               ├── 08-material-library-rules.md
│               ├── 09-exam-review-package-rules.md
│               ├── 10-course-type-processing-rules.md
│               ├── 11-autumn-core-course-index.md
│               └── 12-autumn-core-course-builtins.md
├── 大学课程/
└── undergraduate-vehicle-engineering-learning-usage-guide.md
```

## 当前内置课程骨架

本项目已经内置了一批秋季/核心课程的轻量知识骨架。即使不重新读取原始 PDF，也可以用于基础复习、大纲整理、公式候选、问答题方向和常见题型整理。

当前内置课程包括：

- 程序设计
- 大学物理（一）
- 电工与电子技术基础
- 工程力学1 / Mechanics for Engineers
- 工程力学2 / Applied Dynamics
- 机械控制工程
- 流体力学1 / Mechanics of Fluids 1
- 流体力学2 / Mechanics of Fluids 2
- 热力学1 / Thermodynamics 1
- 热力学2 / Thermodynamics 2
- 液压传动 / Hydraulic and Pneumatic Transmission

注意：内置课程骨架不是逐页课件复刻。若需要精确引用课件原题、页码、答案或老师强调内容，仍需要读取原始素材。

## 三种使用模式

### 1. 无素材模式

没有课件、试卷、答案时，可以生成：

- 通用课程框架
- 通用学习路线
- 通用复习方法
- 通用题库模板
- 通用公式库模板
- 通用考试复习包模板

不能生成：

- 真实课件原题
- 真实页码
- 教师重点
- 真实高频考点

### 2. 内置课程骨架模式

可以基于 `references/12-autumn-core-course-builtins.md` 做基础复习。

适合：

- 先快速了解课程结构
- 生成基础复习大纲
- 生成公式候选
- 生成记忆性问答方向
- 生成常见题型方向

但不能把这些内容声称为“来自某页课件”。

### 3. 素材库增强模式

当用户上传课件、教材、作业、试卷、答案后，可以做更具体的工作：

- 建立课程索引
- 抓取课件重点习题
- 构建题库
- 构建公式库
- 分步解题
- 基于试卷和答案推断高频题型
- 生成更贴近课程材料的考试复习包

## 安装方式

### 当前仓库使用

本项目已经使用 repository-level skill 结构：

```text
.agents/skills/undergraduate-vehicle-engineering-learning/
```

在当前仓库中使用 Codex 时，可以直接调用：

```text
请使用 $undergraduate-vehicle-engineering-learning，帮我整理《工程力学1》的复习大纲。
```

### 安装为全局 Skill

如果希望在任意工作区使用，可以复制到 Codex 用户级 skills 目录：

```powershell
Copy-Item `
  -Path "G:\Desktop\skill_try\.agents\skills\undergraduate-vehicle-engineering-learning" `
  -Destination "C:\Users\29086\.codex\skills\" `
  -Recurse
```

复制后建议重启 Codex。

## 常用提示词

### 梳理课程体系

```text
请使用 $undergraduate-vehicle-engineering-learning，帮我梳理本科传统车辆工程课程体系。
```

### 使用内置骨架复习

```text
请使用 $undergraduate-vehicle-engineering-learning，基于内置秋季核心课程骨架，帮我整理《热力学1》的知识框架。
```

### 建立课程索引

```text
请使用 $undergraduate-vehicle-engineering-learning，读取 大学课程/流体力学1 的课件、习题和答案，只建立课程索引，不要生成详细复习资料。
```

### 抓取课件习题

```text
请使用 $undergraduate-vehicle-engineering-learning，从《电工与电子技术基础》的课件和试题中抓取重点习题，保留来源文件和页码。
```

### 建立公式库

```text
请使用 $undergraduate-vehicle-engineering-learning，基于《大学物理（一）》课件建立公式库，包含公式含义、变量解释、单位、推导逻辑、物理意义、典型题型、记忆方法和易错点。
```

### 生成考试复习包

```text
请使用 $undergraduate-vehicle-engineering-learning，基于《工程力学1》的课件、作业和答案，生成考试复习包。
```

考试复习包包含：

1. 知识点排列
2. 知识点重要性排序
3. 知识框架
4. 核心概念解释
5. 公式总结
6. 高频题型
7. 易错点
8. 记忆性问答
9. 自测题

### 转化为求职表达

```text
请使用 $undergraduate-vehicle-engineering-learning，根据我提供的本科课程表和课程设计材料，帮我写一版简历里的“专业基础”表达。不要夸大，不要虚构项目，没有证据的地方用 TODO。
```

## 推荐素材库结构

```text
materials/
  course-table/
    undergraduate-course-table.md
  courses/
    工程力学1/
      slides/
      homework/
      exams/
      answers/
    热力学1/
      slides/
      homework/
      exams/
      answers/
    流体力学1/
      slides/
      homework/
      exams/
      answers/
  career/
    resume.md
    target-roles.md
    project-evidence/
```

当前仓库中的 `大学课程/` 目录是已有课程素材示例。

## 详细教程

更完整的新手教程见：

[undergraduate-vehicle-engineering-learning-usage-guide.md](./undergraduate-vehicle-engineering-learning-usage-guide.md)
