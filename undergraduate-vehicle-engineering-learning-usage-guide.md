# undergraduate-vehicle-engineering-learning 使用教程

这是一份给新手看的使用说明。你只需要记住一句话：

> 这个 skill 是一个“本科传统车辆工程学习助手”。它现在有两种能力：一是内置了一批你当前项目里的秋季核心课程骨架，可以脱离原始课件做基础复习；二是仍然支持你继续上传课件、作业、试卷、答案，用真实素材做更精细的抓题、解题、题库、公式库和考试复习包。

## 1. 项目 Skill 清单

当前项目里的 repository-level skill 有：

| Skill 名称 | 路径 | 作用 |
|---|---|---|
| `长安都柏林车辆工程.skill` | `.agents/skills/undergraduate-vehicle-engineering-learning/` | 本科传统车辆工程课程体系、课件索引、课程复习、题库、公式库、考试复习包、简历/面试/PPT 表达 |

调用时写：

```text
请使用 $undergraduate-vehicle-engineering-learning，……
```

注意：`长安都柏林车辆工程.skill` 是人类可读显示名；实际调用名仍然是 `$undergraduate-vehicle-engineering-learning`。

## 2. 这个 Skill 能做什么

它可以帮你做：

- 梳理本科传统车辆工程课程体系
- 建立课程知识框架
- 根据课件建立课程索引
- 根据内置课程骨架做基础复习
- 从课件、作业、试卷中抓取重点习题
- 对习题进行分步解答
- 建立题库
- 建立公式库
- 生成考试复习包
- 把本科课程、课程设计、工程训练转化成简历、面试、求职 PPT 表达
- 用更基础、更细致的方式解释课程概念、公式和工程问题

它不会做：

- 不会编造你没有学过的课程
- 不会编造成绩、奖项、项目、实习、竞赛
- 不会把研究生内容混进本科课程
- 不会把自动驾驶研究、强化学习、SUMO、PPO、DQN、LLM 内容混进传统车辆工程本科课程
- 没有素材时，不会假装“我从课件里看到了某个重点”
- 没有项目证据时，不会编造简历项目

## 3. 当前安装方式

当前 `长安都柏林车辆工程.skill` 已经放在本仓库的 repository-level skill 目录：

```text
G:\Desktop\skill_try\.agents\skills\undergraduate-vehicle-engineering-learning\
```

只要你在 `G:\Desktop\skill_try` 这个工作区里使用 Codex，就可以调用它。

## 4. 如果想安装成全局 Skill

如果你以后希望在任何工作区都能使用它，可以把整个 skill 文件夹复制到 Codex 用户级 skills 目录：

```text
C:\Users\29086\.codex\skills\undergraduate-vehicle-engineering-learning\
```

PowerShell 示例：

```powershell
Copy-Item `
  -Path "G:\Desktop\skill_try\.agents\skills\undergraduate-vehicle-engineering-learning" `
  -Destination "C:\Users\29086\.codex\skills\" `
  -Recurse
```

复制后建议重启 Codex，让 Codex 重新加载 skills。

如果只是当前项目使用，不需要复制到 C 盘。

## 5. 最简单的调用方式

```text
请使用 $undergraduate-vehicle-engineering-learning，帮我梳理本科传统车辆工程课程体系。
```

或者：

```text
请使用 $undergraduate-vehicle-engineering-learning，帮我整理《工程力学1》的复习大纲。
```

关键是写上：

```text
$undergraduate-vehicle-engineering-learning
```

## 6. 三种使用模式

## 模式 A：没有任何素材

适合你只是想先搭框架。

可以做：

- 通用课程框架
- 通用学习路线
- 通用复习方法
- 通用考试复习包模板
- 通用公式总结模板
- 通用题库模板
- 告诉你应该上传哪些材料

不能做：

- 从课件中抓题
- 判断老师重点
- 生成真实高频考点
- 引用具体页码
- 说某道题来自某份课件

示例：

```text
请使用 $undergraduate-vehicle-engineering-learning，在我还没有上传课件的情况下，先给我一个《汽车构造》的通用复习框架。
```

## 模式 B：使用内置秋季核心课程骨架

这个项目已经把当前上传过的一批秋季/核心课程做成了内置骨架。即使不重新读取 PDF，也可以做基础复习。

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

可以做：

- 基于内置骨架生成复习大纲
- 基于内置骨架整理知识点
- 基于内置骨架列公式候选
- 基于内置骨架生成问答题方向
- 基于内置骨架生成常见题型
- 基于内置骨架生成基础考试复习包

限制：

- 不能声称某个知识点来自具体第几页，除非重新读取原始 PDF
- 不能引用课件原题的精确文字，除非已经从素材中抽取
- 不能把内置骨架当成老师真实考试重点

示例：

```text
请使用 $undergraduate-vehicle-engineering-learning，基于内置秋季核心课程骨架，帮我整理《工程力学2》的考试复习包。
```

## 模式 C：使用你上传的素材库

如果你上传了课件、试卷、作业、答案，skill 可以做最具体的工作。

可以做：

- 识别课程
- 建立课程索引
- 建立课件目录
- 抓取重点习题
- 解题
- 建立题库
- 建立公式库
- 生成考试复习包
- 引用来源文件和页码

示例：

```text
请使用 $undergraduate-vehicle-engineering-learning，读取 大学课程/流体力学1 的课件、习题和答案，先建立课程索引，不要生成详细复习资料。
```

## 7. 推荐素材库怎么放

推荐结构：

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

不一定非要这样放。你也可以直接告诉 Codex：

```text
我的课件在 G:\Desktop\skill_try\大学课程\流体力学1，请先读取这些 PDF。
```

## 8. 素材越多，能做得越具体

| 你提供的材料 | Skill 能做什么 |
|---|---|
| 什么都没有 | 通用框架、通用方法、模板 |
| 只有课程表 | 课程体系、课程关系、学习路线 |
| 使用内置课程骨架 | 大纲、知识点、公式候选、问答题方向、题型方向 |
| 有课件 | 课程索引、大纲、知识点、公式、课件习题 |
| 有课件 + 作业 | 题库、题型、解题方法 |
| 有课件 + 试卷 + 答案 | 高频题型、考试复习包、易错点 |
| 有项目材料 | 简历、面试、PPT 中的真实项目表达 |

## 9. 常用命令清单

### 9.1 建课程索引

```text
请使用 $undergraduate-vehicle-engineering-learning，读取 [文件夹路径]，只建立课程索引，不要生成详细复习资料。
```

### 9.2 使用内置骨架复习

```text
请使用 $undergraduate-vehicle-engineering-learning，基于内置秋季核心课程骨架，帮我整理《热力学1》的知识框架。
```

### 9.3 建课程大纲

```text
请使用 $undergraduate-vehicle-engineering-learning，基于 [课程名/文件夹路径] 的课件，帮我构建课程大纲。
```

### 9.4 抓取课件重点习题

```text
请使用 $undergraduate-vehicle-engineering-learning，从 [课程名/文件夹路径] 的课件中抓取重点习题，保留来源文件和页码。
```

### 9.5 解答习题

```text
请使用 $undergraduate-vehicle-engineering-learning，解答 [课程名] 中抓取到的重点习题，要求分步骤讲清楚。
```

### 9.6 建题库

```text
请使用 $undergraduate-vehicle-engineering-learning，基于 [课程名/文件夹路径] 的课件、作业和试卷，构建题库。
```

### 9.7 建公式库

```text
请使用 $undergraduate-vehicle-engineering-learning，基于 [课程名/文件夹路径] 的课件，构建公式库，包含公式含义、变量解释、推导逻辑、物理意义、典型题型和易错点。
```

### 9.8 生成考试复习包

```text
请使用 $undergraduate-vehicle-engineering-learning，基于 [课程名/文件夹路径] 的课件和习题，生成考试复习包。
```

考试复习包会包括：

1. 知识点排列
2. 知识点重要性排序
3. 知识框架
4. 核心概念解释
5. 公式总结
6. 高频题型
7. 易错点
8. 记忆性问答
9. 自测题

### 9.9 生成简历表达

```text
请使用 $undergraduate-vehicle-engineering-learning，基于我的本科课程和课程设计材料，把它们转化成简历中的专业基础和项目经历表达。
```

### 9.10 生成面试回答

```text
请使用 $undergraduate-vehicle-engineering-learning，帮我把本科车辆工程课程背景转化成面试中“你有哪些专业基础”的回答。
```

## 10. 常用提示词范例

### 10.1 课程体系

```text
请使用 $undergraduate-vehicle-engineering-learning，帮我梳理本科传统车辆工程课程体系，按数学基础、力学、热流体、材料制造、车辆结构、发动机、车辆动力学、电控与新能源进行分类。
```

### 10.2 课程关系

```text
请使用 $undergraduate-vehicle-engineering-learning，帮我讲清楚 Mechanics、Solid Mechanics、Applied Dynamics 和 Automotive Vehicle Dynamics 之间的关系，要适合基础薄弱的人理解。
```

### 10.3 课件索引

```text
请使用 $undergraduate-vehicle-engineering-learning，读取 G:\Desktop\skill_try\大学课程 下的资料，只建立课程索引。请输出识别到哪些课程、每门课有哪些文件、对应本科课程表哪一门、哪些文件需要我确认。
```

### 10.4 内置骨架复习

```text
请使用 $undergraduate-vehicle-engineering-learning，基于内置秋季核心课程骨架，帮我整理《液压传动》的知识点、公式候选、问答题方向和常见题型。不要声称这些来自具体页码。
```

### 10.5 抓题但不解题

```text
请使用 $undergraduate-vehicle-engineering-learning，从《电工与电子技术基础》的课件和试题中抓取重点习题，先不要解答，只建立题库索引。
```

### 10.6 抓题并解题

```text
请使用 $undergraduate-vehicle-engineering-learning，从《流体力学1》的题库中选择核心题型进行分步解答。每道题都要说明用到的知识点、公式、解题流程和易错点。
```

### 10.7 建公式库

```text
请使用 $undergraduate-vehicle-engineering-learning，基于《大学物理（一）》课件建立公式库。每个公式都要包含公式含义、变量解释、单位、推导逻辑、物理意义、典型题型、记忆方法和易错点。
```

### 10.8 生成考试复习包

```text
请使用 $undergraduate-vehicle-engineering-learning，基于《工程力学1》的课件、作业和答案，生成考试复习包。必须包括知识点排列、重要性排序、知识框架、核心概念解释、公式总结、高频题型、易错点、记忆性问答和自测题。
```

### 10.9 简历表达

```text
请使用 $undergraduate-vehicle-engineering-learning，根据我提供的本科课程表和课程设计材料，帮我写一版简历里的“专业基础”表达。不要夸大，不要虚构项目，没有证据的地方用 TODO。
```

### 10.10 面试表达

```text
请使用 $undergraduate-vehicle-engineering-learning，帮我准备一个面试回答：请介绍你的车辆工程专业基础。要求基于本科课程，不要加入研究生或自动驾驶研究内容。
```

## 11. 最推荐的使用顺序

如果你刚开始整理，建议按这个顺序来：

1. 先用内置课程骨架搭建总体复习框架
2. 上传或整理本科课程表
3. 让 skill 建课程体系图
4. 上传某一门课的课件
5. 让 skill 建课程索引
6. 让 skill 建课程大纲
7. 让 skill 抓取重点习题
8. 让 skill 建题库
9. 让 skill 建公式库
10. 让 skill 生成考试复习包
11. 最后再转化成简历、面试、求职 PPT 表达

## 12. 新手最容易犯的错误

### 错误 1：没上传课件，却要求“从课件抓题”

错误提示词：

```text
帮我从汽车构造课件里抓重点题。
```

如果没有课件，skill 不能抓题。

更好的提示词：

```text
我还没上传课件。请使用 $undergraduate-vehicle-engineering-learning，先告诉我需要上传哪些材料，才能为《汽车构造》建立题库。
```

### 错误 2：要求生成“真实高频考点”，但没有试卷或作业

没有试卷、作业、答案时，只能生成通用重点或内置骨架重点，不能说是真实高频考点。

更好的提示词：

```text
请使用 $undergraduate-vehicle-engineering-learning，在没有试卷的情况下，先基于内置课程骨架生成复习重点，并标注哪些地方需要试卷验证。
```

### 错误 3：让它编简历项目

skill 不会编造项目。

更好的提示词：

```text
请使用 $undergraduate-vehicle-engineering-learning，根据我提供的课程设计报告，帮我改写成简历项目经历。没有数据的地方用 TODO。
```

## 13. 一句话记忆

没有素材时，它是“本科车辆工程学习方法助手”。

使用内置骨架时，它是“秋季核心课程基础复习助手”。

有素材时，它是“课件索引 + 抓题 + 解题 + 题库 + 公式库 + 考试复习包助手”。

任何具体结论，都应该来自真实材料或明确标注为内置骨架/通用框架。
