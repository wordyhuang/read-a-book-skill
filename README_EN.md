> **[中文](README.md) | English**

# Read a Book Skill — Book Analysis Skill

> **Development Language**: This skill is developed and tested in Chinese. Chinese output is the first priority.
> Analysis reports and broadcast scripts are generated in Chinese by default. To request output in another language, specify the target language explicitly when invoking.

## About

A structured book analysis skill based on Mortimer J. Adler's *How to Read a Book*. It provides systematic deconstruction of non-fiction books across four categories: Practical/Tool, Cognitive/Science, Business/Management, and Philosophy/Thought.

**Core Capabilities**:
- Collects publicly available information via web search and automatically generates chapter-by-chapter analysis reports with type-specific branches
- Supports two output formats: structured report (Format A) and broadcast script (Format B)
- Applies anti-AI-flavor writing rules to make generated content sound more natural and human
- Designed to be agent-agnostic — not tied to any specific AI platform

## Agent Compatibility

This skill is decoupled from any specific Agent platform. Any AI Agent with **web search, web fetch, file read, and file write** capabilities can use it directly. See the "Agent Adaptation" section in `SKILL.md` for details.

## Directory Structure

```
read-a-book-skill/
├── SKILL.md              ← Skill source code (iteration entry point)
├── README.md              ← Chinese documentation
├── README_EN.md           ← This file (English)
└── document/              ← Planning docs, version archives (optional)
```

## System Load Path

The skill is loaded by the system from:

```
.trae/skills/read a book skill/SKILL.md
```

## Iteration Workflow

1. Edit `SKILL.md` in the project root
2. After testing, sync changes to `.trae/skills/read a book skill/SKILL.md`
3. Archive change history in `document/` if needed

## Output Formats

The skill supports two output formats:

- **Format A — Structured Report** (default): A Markdown document with chapters, headings, lists, and tables. Suitable for reading and reference.
- **Format B — Broadcast Script**: A continuous, paragraph-free script designed to be read aloud. Suitable for podcasts, audio programs, and video voiceovers.

Use keywords like "broadcast script", "audio", or "podcast" to trigger Format B; Format A is the default.

## Anti-AI Flavor

All generated content (excluding original book quotes) is processed according to the [remove-ai-flavor-writing-skill](https://github.com/B1lli/remove-ai-flavor-writing-skill) rules to remove template-like AI expressions. See Section 7 "Anti-AI-Flavor Quick Reference" in `SKILL.md`.

## Related Resources

- Planning doc: `.trae/documents/书籍拆解方法论技能创建计划.md`
- Practice case: `精进/文档/精进拆解报告_v3.0.md`
- Theoretical foundation: `.trae/skills/如何阅读一本书/SKILL.md`
