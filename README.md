# 长安都柏林车辆工程.skill

一个面向 **本科传统车辆工程 / 机械车辆工程方向** 的 Codex Agent Skill 项目。

这个项目用于沉淀本科四年车辆工程课程体系、课程复习方法、课件索引、题库、公式库、考试复习包，以及求职简历、面试、PPT 中的专业基础表达。

> 内部调用名：`$undergraduate-vehicle-engineering-learning`  
> 显示名称：`长安都柏林车辆工程.skill`

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

## 上传 GitHub 前的建议

如果这个仓库会公开，请先检查 `大学课程/` 目录中是否包含：

- 受版权保护的教材 PDF
- 教师课件
- 答案手册
- 个人实验报告
- 个人学号、姓名、邮箱等隐私信息

如果包含上述内容，建议不要公开上传，或者将 `大学课程/` 从公开仓库中移除，只保留 skill 本体和教程。

推荐公开上传的内容：

- `.agents/skills/undergraduate-vehicle-engineering-learning/`
- `README.md`
- `undergraduate-vehicle-engineering-learning-usage-guide.md`

谨慎上传的内容：

- `大学课程/`
- 教材 PDF
- solution manual
- 试卷答案
- 个人报告

## License

当前项目尚未指定开源协议。公开发布前建议补充 `LICENSE` 文件。
