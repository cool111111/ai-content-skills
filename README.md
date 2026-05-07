<div align="center">

# 🎨 AI Content Skills

**一套让 AI Agent 真正能产出能用的内容的 Skill 全家桶**

不是 prompt 集合，是一整套可生产的内容方法论 — 覆盖**长文写作 + 短图文生成 + 达人发现**的完整内容运营链路。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skill: Claude Code](https://img.shields.io/badge/Skill-Claude%20Code-8A2BE2)](https://github.com/anthropics/claude-code)
[![Stars](https://img.shields.io/github/stars/cool111111/ai-content-skills?style=social)](https://github.com/cool111111/ai-content-skills/stargazers)

</div>

> 这是在 AI 内容运营实战中**沉淀**出来的方法论。
> 从手动写作 → 模板化生产 → 多 Agent 自动化管线，把每一步经验都结构化成 AI Agent 能直接执行的规范。

<!-- TODO 在此处插入一张管线架构图 / 工作流截图 / 真实产出截图 -->

## 这套 Skill 解决什么问题

普通 AI 写内容的三大病：**AI 味重 / 没钩子 / 没节奏**。

这套 Skill 不靠"prompt 越写越长"硬扛，而是用方法论 + 质检流水线 + 反 AI 味词库系统化解决：

| 病症 | 解决方案 |
|------|---------|
| AI 味重 | 60+ 高频套话黑名单 + 写完自动扫描重构 |
| 选题平庸 | HKR 三维度选题质检（公众号）+ 四维评分（小红书） |
| 没钩子没节奏 | 钩子模板库 + 平台节奏适配规则 |
| 找达人慢 | 跨平台自动搜索 + 深度内容评估 |

---

## 📚 包含的 Skill

### ✍️ [Writer Skill](https://github.com/cool111111/writer-skill) — 公众号长文

[![Stars](https://img.shields.io/github/stars/cool111111/writer-skill?style=social)](https://github.com/cool111111/writer-skill)

公众号长文写作方法论，从选题到成稿的全流程规范。

- HKR 选题质检 / 反 AI 味词库 / 三级质检流水线
- 完整的 `references/` 方法论文档库

### 📕 [XHS Content Skill](https://github.com/cool111111/xhs-content-skill) — 小红书短图文

[![Stars](https://img.shields.io/github/stars/cool111111/xhs-content-skill?style=social)](https://github.com/cool111111/xhs-content-skill)

继承 Writer 的风格底座，针对小红书平台做了深度适配。

- 选题优先级体系 / 标题钩子库 / 四维评分 / 反馈迭代闭环

### 🔍 [find-influencer Skill](https://github.com/cool111111/find-influencer-skill) — 跨平台达人发现

[![Stars](https://img.shields.io/github/stars/cool111111/find-influencer-skill?style=social)](https://github.com/cool111111/find-influencer-skill)

跨平台达人发现 + 深度评估自动化，覆盖小红书 / 抖音 / B 站 / YouTube。

- 实战验证过大量创作者筛选评估
- 把"找达人"从 3-5 小时压缩到 15-20 分钟

---

## 🚀 全家桶安装

如果你想**一次装齐所有 skill**：

```bash
# Clone 整个仓库
git clone https://github.com/cool111111/ai-content-skills.git

# 把每个 skill 软链到你 Agent 的 skills 目录
ln -s $(pwd)/ai-content-skills/writer ~/.your-agent/skills/writer
ln -s $(pwd)/ai-content-skills/xhs-content ~/.your-agent/skills/xhs-content

# find-influencer 在独立 repo（依赖较多，单独装）
git clone https://github.com/cool111111/find-influencer-skill.git \
  ~/.your-agent/skills/find-influencer
```

只想装某一个？直接去对应 repo 单独 clone，互不影响。

---

## 🔧 实战中我怎么用

这套 Skill 不是写出来"看着好"的，是真在跑的：

```
Twitter KOL × 3 ─────┐
GitHub Trending ─────┼──→ 日报汇总 ──→ 选题筛选 ──→ XHS Content Skill ──→ 推飞书审稿 ──→ 发布
AI 新闻聚合 ─────────┘                                         │
                                                              └──→ Writer Skill（深度长文）
```

**9 个 Agent 并行 / 每天 30 分钟跑完 / 稳定产出 3-5 条候选稿件。**

我只做最后一步：审稿 + 发布。

---

## 📁 目录结构

```
ai-content-skills/
├── writer/              # Writer Skill 完整内容（与独立 repo 同步）
│   ├── SKILL.md
│   └── references/
│       ├── content_methodology.md
│       └── style_examples.md
└── xhs-content/         # XHS Content Skill 完整内容（与独立 repo 同步）
    └── SKILL.md
```

> `find-influencer` 因为依赖较多（whisper / ffmpeg / opencli），保留为独立 repo，不打包进全家桶。

---

## 💡 适用场景

- 个人博主 / 自媒体 — 用 AI 提效，但拒绝 AI 味
- AI 产品的内容运营 — 把内容生产规模化、标准化
- 多 Agent 系统开发者 — 直接复用我的方法论，不用从零踩坑

---

## 致谢

Writer Skill 框架借鉴了开源社区的 Claude Skill 实践，在此基础上融入了我个人的写作方法论和实战运营经验。

## License

MIT — 觉得有用就 **star 一下** ⭐ 是最大的鼓励。
