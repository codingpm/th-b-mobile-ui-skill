# TH B Mobile UI Skill

TH B Mobile UI Skill 是一个用于生成企业移动端原型界面的可复用 skill。

它通过沉淀页面结构、界面语义和 UI 规范，帮助 AI 生成更规整、更克制、更符合企业移动端场景的界面，而不是泛化的消费级页面。它关注的是设计语言和页面结构，而不是某一种具体技术实现。

## 特性

- 支持企业移动端常见的列表页、详情页、表单页、结果页、状态页模式
- 内置颜色、按钮、表单、卡片、状态和交互规则
- 适合生成原型描述、Figma 提示词、前端页面代码
- 兼容 skill 平台常见结构，包含 `SKILL.md` 和 `agents/openai.yaml`
- 适合通过 GitHub 仓库进行分享、维护和发布

## 快速开始

在提示词中直接引用这个 skill：

```text
请用 $th-b-mobile-ui-skill 生成一个企业移动端原型，要求界面紧凑、配色克制、按钮层级清晰、卡片结构稳定。
```

为了获得更好的结果，建议同时补充：

- 页面类型
- 关键模块
- 主要字段
- 主要操作
- 是否有 tabs、popup、bottom action
- 你希望输出的是原型描述、Figma 提示词，还是前端代码

## 示例提示词

```text
请用 $th-b-mobile-ui-skill 生成一个移动端资源列表页原型，页面包含顶部导航、筛选区、卡片列表、状态标签和底部操作区。
```

```text
请用 $th-b-mobile-ui-skill 生成一个移动端审批表单原型，要求分组清晰、控件紧凑、校验明确，并带固定底部操作区。
```

```text
请用 $th-b-mobile-ui-skill 生成一个详情页的 Figma 提示词，页面包含状态头部、摘要卡片、关联 tabs 和操作记录区。
```

```text
请用 $th-b-mobile-ui-skill 生成企业移动端风格的前端页面代码，要求中性色表面、卡片式结构、清晰按钮层级，并显式包含加载态、空态和错误态。
```

## 这个 Skill 能做什么

这个 skill 主要用于指导 AI 生成：

- 带导航、筛选、卡片列表的移动端列表页
- 带状态头部、摘要信息、关联区块的详情页
- 带分组和明确操作层级的创建/编辑表单
- 带固定底部操作区的提交页
- 结果页、状态页、空态页
- 可直接用于设计生成的 Figma 提示词
- 企业移动端风格的 HTML、Vue、React 原型代码

## 设计原则

这个 skill 偏好的界面风格：

- 中性、低噪音的界面表面
- 单一强调色
- 紧凑型移动端信息密度
- 清晰的按钮层级
- 稳定的卡片、列表、表单结构
- 明确的加载态、空态和错误态

这个 skill 会避免的界面风格：

- 营销页式布局
- 炫目的渐变
- 过于装饰化的移动端界面
- 过大的视觉头图
- 过于活泼的消费级风格

## 仓库结构

```text
th-b-mobile-ui-skill/
├── SKILL.md
├── README.md
├── HUMAN_GUIDE.md
├── agents/
│   └── openai.yaml
└── references/
    ├── mobile-page-patterns.md
    ├── mobile-ui-spec.md
    └── publishing-kit.md
```

### 主要文件

- `SKILL.md`
  skill 的核心定义和主规则集。

- `agents/openai.yaml`
  skill 平台展示信息和默认提示词配置。

- `HUMAN_GUIDE.md`
  面向同事或协作者的人类可读说明文档。

### 参考文件

- `references/mobile-page-patterns.md`
  页面模板，包括列表页、详情页、表单页、结果页等常见移动端结构。

- `references/mobile-ui-spec.md`
  更细的颜色、按钮、表单、卡片和交互规则。

- `references/publishing-kit.md`
  用于发布到 skill 平台时的简介、卖点和示例提示词。

## 这个仓库怎么用

这个仓库有几种常见用法：

1. 作为本地 skill 目录，放入兼容 Codex 的 skills 目录中使用
2. 作为 GitHub 仓库，被 skill 平台从仓库导入
3. 作为团队共享的企业移动端界面规范和提示词规范

## 适合的使用场景

- 生成管理类移动端列表页
- 设计带状态和分组区块的详情页
- 生成配置页或审批页
- 设计带底部操作区的移动端表单
- 生成结果页和状态页
- 生成企业移动端风格的前端原型

## 发布说明

这个仓库已经按 skill 平台和 GitHub 分发的方向组织好了结构。它被设计成一层可复用的企业移动端界面规范，而不是某个具体产品实现的技术依赖。

如果平台支持读取 skill 元数据，主要入口文件是：

- `SKILL.md`
- `agents/openai.yaml`
