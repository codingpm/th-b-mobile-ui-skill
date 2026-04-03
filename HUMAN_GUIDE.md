# TH B Mobile UI Skill

`th-b-mobile-ui-skill` 是一个面向企业移动端原型生成的 skill。

它的目标是把移动端产品中常见的页面结构、组件语义、交互方式和界面风格提炼成一套可复用规则，让 AI 生成出来的移动端原型更像成熟的企业应用，而不是泛化的消费级界面。

## 适合做什么

- 生成移动端列表页原型
- 生成移动端详情页原型
- 生成移动端表单页和编辑页原型
- 生成带底部固定操作区的提交页
- 生成结果页、状态页、空态页
- 生成移动端 Figma 提示词
- 生成移动端 Vue、React、HTML 原型代码

## 这个 Skill 的核心价值

它会引导 AI 优先采用更像成熟移动端产品的设计语言，例如：

- 清晰的顶部导航和垂直信息流
- 卡片式信息区块和列表结构
- 分组表单、选择器、日期选择器等移动端友好控件
- 固定底部操作区
- 标签、徽标、状态块和结果反馈
- 更克制的移动端色彩和更实用的交互方式

它生成的结果会更像真实可落地的移动端产品页面，而不是活动页、营销页或泛化的 App 视觉。

## 不做什么

这个 skill 不追求复刻某一套具体技术实现，而是优先沉淀：

- 页面结构规则
- 命名和组件语义
- 移动端常见布局模式
- 表单、卡片、列表、底部操作区等移动端规范
- 更贴近企业移动端产品的界面风格

它更适合做“规范约束”和“原型生成”，而不是绑定某种具体实现。

## 推荐使用方式

最简单的调用方式：

```text
请用 $th-b-mobile-ui-skill 生成一个移动端页面原型，要求贴近企业移动端产品规范和标准化页面结构。
```

更推荐的调用方式：

```text
请用 $th-b-mobile-ui-skill 生成一个移动端资源列表页原型。

要求：
- 页面结构符合企业移动端产品风格
- 顶部有导航和筛选或 tabs
- 中间使用卡片列表或列表项结构
- 状态通过标签或状态块表达
- 底部操作区在需要时固定显示
- 不要做成营销页或装饰性很强的界面
```

## 适合补充给 AI 的信息

为了让结果更准，建议补充：

- 页面类型：列表页、详情页、表单页、结果页、状态页、仪表盘页
- 主要业务对象：资源、对象、记录、组织、地点、分类
- 关键字段
- 主要操作
- 是否需要 tabs、card、selector、popup、bottom action
- 是否需要生成代码
- 是否需要更偏卡片式、列表式、表单式或结果页式结构

## 目录说明

- [SKILL.md](/Users/mashaoguang/.codex/skills/th-b-mobile-ui-skill/SKILL.md)
  skill 的核心规则定义
- [openai.yaml](/Users/mashaoguang/.codex/skills/th-b-mobile-ui-skill/agents/openai.yaml)
  skills 平台展示信息和默认 prompt
- [mobile-page-patterns.md](/Users/mashaoguang/.codex/skills/th-b-mobile-ui-skill/references/mobile-page-patterns.md)
  常见移动端页面模板
- [mobile-ui-spec.md](/Users/mashaoguang/.codex/skills/th-b-mobile-ui-skill/references/mobile-ui-spec.md)
  移动端颜色、按钮、表单、卡片和交互规则

## 一句话总结

如果你的目标是“让 AI 生成出来的移动端原型更像成熟的企业移动端产品”，那就用 `th-b-mobile-ui-skill`。