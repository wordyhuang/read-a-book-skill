> **[English](README_EN.md) | 中文**

# Read a Book Skill — 书籍拆解技能

> **开发语言**：本技能基于中文开发与测试，中文内容为第一优先级输出语言。
> 拆解报告和口播稿默认以中文生成；如需其他语言输出，请在调用时明确指定目标语言。

## 项目简介

基于 Mortimer J. Adler《如何阅读一本书》(How to Read a Book) 的分析阅读理论，对实用/工具、认知/科普、商业/管理、哲学/思想四类非虚构书籍进行结构化拆解。

**核心能力**：
- 通过网络搜索采集公开资料，自动生成分类型（四分支）的逐章拆解报告
- 支持两种输出格式：结构化报告（格式 A）和口播稿（格式 B）
- 引入去 AI 味写作规则，确保生成内容贴近真人表达
- 设计为跨 Agent 平台通用，不绑定任何特定 AI 系统

## Agent 兼容性

本技能与 Agent 平台解耦，任何具备**网络搜索 + 网页获取 + 文件读写**能力的 AI Agent 均可使用。详见根目录 `SKILL.md` 的「Agent 适配说明」章节。

## 目录结构

```
read-a-book-skill/
├── SKILL.md              ← 技能源代码（迭代入口）
├── README.md              ← 本文件（中文）
├── README_EN.md           ← 英文版说明
└── document/              ← 规划文档、版本记录（可选）
```

## 系统加载位置

技能实际被系统加载的路径是：

```
.trae/skills/read a book skill/SKILL.md
```

## 迭代工作流

1. 修改根目录 `SKILL.md` 中的内容
2. 测试验证后，将修改同步到 `.trae/skills/read a book skill/SKILL.md`
3. 修改历史可在 `document/` 中归档

## 输出格式

技能支持两种输出格式，可根据场景选择：

- **格式 A — 结构化报告**（默认）：Markdown 格式的分章节、含标题/列表/表格的完整拆解报告。适合阅读和查阅。
- **格式 B — 口播稿**：类新闻播报的连续稿件，无分段、无旁白，可直接朗读。适合播客、音频节目、视频口播。

用户指定"口播稿/播报稿/朗读版/音频"时自动使用格式 B；默认为格式 A。

## 去 AI 味

所有生成内容（原文引用除外）均按 [remove-ai-flavor-writing-skill](https://github.com/B1lli/remove-ai-flavor-writing-skill) 的规则去除 AI 写作痕迹。详见 `SKILL.md` 第 7 节「去AI味速查表」。

## 相关资源

- 规划文档：`.trae/documents/书籍拆解方法论技能创建计划.md`
- 实践案例：`精进/文档/精进拆解报告_v3.0.md`
- 理论支撑：`.trae/skills/如何阅读一本书/SKILL.md`
