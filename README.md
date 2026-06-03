# AI 项目开发模板

基于"本地文档驱动 + 分布式 Agent"的四阶段开发 SOP。

## 使用方法

### 1. 复制模板到新项目

```powershell
# 把这整个目录结构复制到你的新项目根目录
Copy-Item -Recurse "I:\AI\SOP\*" ".\my-new-project\" -Force
```

### 2. 启动 Claude Code 后发送第一句话

```
请首先读取 .claude/sop.md 文件。这是我们接下来开发这个项目必须严格遵守的生命周期 SOP，请按照里面的【阶段一：需求定义】开始向我提问。
```

## 目录结构

```
my-new-project/
├── .claude/
│   └── sop.md              # 完整 SOP 规范（AI 必读）
├── docs/
│   ├── proposal.md         # 阶段一输出：需求文档
│   ├── architecture.md     # 阶段二输出：架构设计
│   ├── progress.md         # 阶段三输出：任务看板
│   ├── prompt.md           # 阶段四输出：Master 运行总控
│   └── toolbox.md          # 已验证可复用的 skill/plugin 清单
├── tests/                  # 单元测试目录（严苛门禁）
└── README.md
```

## 四个阶段

| 阶段 | 名称 | 输出文件 |
|------|------|----------|
| 一 | 需求定义 | `docs/proposal.md` |
| 二 | 架构设计 | `docs/architecture.md` |
| 三 | 任务拆解 | `docs/progress.md` |
| 四 | 分布式编码 | `docs/prompt.md` + 源码 + 单测 |

详见 [.claude/sop.md](.claude/sop.md)。
