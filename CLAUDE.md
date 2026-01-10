# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with this repository.

## 项目概述

这是一个基于 Claude Code Skills 的"反AI味"写作系统。核心目标是通过强制性工作流，让AI写出的文章像人类一样自然。

**工作模式：** Skill-first、Workflow-gated、禁止直接起草

**优先级：** 去AI味 > 清晰度 > 可控性 > 质量 > 速度

## 用户交互模式

### 开始写作
```
你："帮我写一篇关于XXX的文章"
```
系统自动引导：澄清需求 → 选择是否调研 → 风格选择 → 分步写作 → 主编审稿

### 风格建模
```
你："帮我分析 @sample_article.md 的风格，以后按这个风格写"
```
系统进行12维度解构，保存风格文件到 `.claude/styles/`

### 仅审稿
```
你："帮我审一下这篇文章" + 粘贴内容或 @文件
```
系统调用主编审稿，输出AI味道检测和修改建议

## 核心架构（高层概念）

项目通过5个强制性Skill实现工作流准入：

```
用户请求 → writing-clarifier (必须) → research-expert (可选) → style-modeler (可选)
    → writing-executor (必须) → editor-review (必须) → 最终稿
```

**数据流：**
- 需求澄清 → 结构化确认信息
- 调研资料 → 数据/案例/观点
- 风格建模 → 12维配方文件
- 写作执行 → 分步草稿 + 版本文件
- 主编审稿 → 诊断报告

**关键约束：**
1. 严禁跳过 `writing-clarifier` 直接写作
2. 严禁一次性输出全文（必须分步）
3. 字数误差必须控制在±20%以内
4. 反AI格式默认启用（小标题/排比/加粗禁用）

## 重要文件位置

| 文件 | 用途 |
|------|------|
| `writing-agent/CLAUDE.MD` | 完整工作流定义（优先阅读） |
| `writing-agent/.claude/skills/*/SKILL.md` | 各Skill详细指令 |
| `writing-agent/.claude/styles/*.md` | 风格库 |
| `writing-agent/articles/*.md` | 生成的文章 |
| `.vscode/settings.json` | VSCode配置（已启用跳过权限检查） |

## API配置（DeepSeek）

推荐使用 DeepSeek API 降低成本：
```
API Base URL: https://api.deepseek.com/v1
Model: deepseek-chat
```

详见 `writing-agent/docs/DEEPSEEK_SETUP.md`

## 扩展项目

### 添加新Skill
在 `writing-agent/.claude/skills/` 创建目录，参考现有Skill的格式编写 `SKILL.md`

### 添加新风格
对 Claude 说："帮我分析 @article.md 的风格"，系统自动保存到 `writing-agent/.claude/styles/`

### 修改反AI规则
编辑 `writing-agent/.claude/skills/写作执行/SKILL.md` 的"反AI写作技巧"部分

## 版本管理

每个Skill都有独立版本号（如v1.3.0），修改时需更新SKILL.md中的版本记录。

详见 `writing-agent/CHANGELOG.md`

## 参考文档

- [完整工作流](writing-agent/CLAUDE.MD) - 必读
- [项目结构](writing-agent/docs/PROJECT_STRUCTURE.md)
- [常见问题](writing-agent/docs/FAQ.md) - 24个Q&A
- [贡献指南](writing-agent/CONTRIBUTING.md)
