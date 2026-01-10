# auto_write_v2

> 基于 Claude Code Skills 的"反AI味"写作系统

一个工作流驱动的写作系统，通过强制性的需求澄清、风格建模、素材调研和主编审稿，帮助你写出**不像AI生成**的高质量文章。

## 核心特点

- **反AI味道**：自动去除小标题病、排比上瘾、格式洁癖等AI典型特征
- **风格建模**：12维度深度解构，提取任何文章的写作风格并复用
- **素材调研**：自动搜集真实数据、案例和观点，让文章有据可依
- **字数精准控制**：误差控制在±20%以内

## 项目结构

```
auto_write_v2/
├── writing-agent/              # 核心写作系统
│   ├── .claude/
│   │   ├── skills/            # 写作流程 Skills（5个）
│   │   │   ├── 澄清写作需求/  # 需求澄清
│   │   │   ├── 调研资料/      # 素材调研
│   │   │   ├── 风格建模/      # 风格提取
│   │   │   ├── 写作执行/      # 分步写作
│   │   │   └── 主编审稿/      # 审稿诊断
│   │   └── styles/            # 风格库（12维度风格配方）
│   │       ├── 参考文章/       # 样本文档
│   │       ├── 蝈蝈的写作风格1.md
│   │       └── 墨水怪风.md
│   ├── articles/              # 生成的文章
│   │   └── images/            # 文章配图
│   ├── docs/                  # 详细文档
│   │   ├── FAQ.md             # 常见问题
│   │   └── PROJECT_STRUCTURE.md
│   ├── CLAUDE.MD              # 工作流主文档
│   ├── CHANGELOG.md           # 版本记录
│   └── README.md              # 写作系统说明
├── .claude/                   # Claude Code 配置
├── static/                    # 静态资源
├── .gitignore
├── CLAUDE.md                  # 项目级配置说明
└── README.md                  # 本文件
```

## 快速开始

1. 在 Claude Code 中打开 `writing-agent` 目录
2. 对 Claude 说："帮我写一篇关于XXX的文章"
3. 系统会自动引导你完成整个写作流程

## 详细文档

完整的使用指南请查看 [writing-agent/README.md](writing-agent/README.md)

## 许可证

MIT License
