# AI Content Skills

一套为 AI Agent 设计的内容创作 Skill，覆盖公众号长文写作和小红书短图文生成。

基于 [Claude Code](https://github.com/anthropics/claude-code) 的 Skill 机制构建，可直接加载到支持 Skill 的 AI Agent 中使用。

## 包含的 Skill

### 1. Writer（公众号长文写作）

`writer/SKILL.md` — 一套完整的公众号长文写作方法论，从选题到成稿的全流程规范。

核心特点：
- **HKR 选题质检**：Happy + Knowledge + Resonance 三维度评估选题
- **口语化写作**：像聊天一样写文章，拒绝书面套话
- **严格事实核查**：所有可验证事实必须有来源
- **禁用词体系**：自动规避"说白了""本质上"等 AI 味词汇
- 附带 `references/content_methodology.md`（内容方法论）和 `references/style_examples.md`（风格示例）

### 2. XHS Content（小红书短图文）

`xhs-content/SKILL.md` — 小红书平台的短图文生成规范，继承 Writer 的风格底座并适配短内容场景。

核心特点：
- **选题优先级**：KOL 观点 > 开源项目破圈 > 产品发布 > 行业数据
- **四维评分体系**：钩子力 / 信息密度 / 传播性 / 互动潜力
- **标题必杀技**：数字冲击、信息差、争议性等公式化钩子模板
- **配图方案**：CDP 浏览器截取真实来源，支持降级策略
- **数据追踪**：预测评分 vs 实际数据的反馈迭代机制

## 使用方式

将 Skill 文件放到你的 AI Agent 的 skills 目录下，Agent 会在需要时自动加载。

```
your-agent/
├── skills/
│   ├── writer/
│   │   ├── SKILL.md
│   │   └── references/
│   │       ├── content_methodology.md
│   │       └── style_examples.md
│   └── xhs-content/
│       └── SKILL.md
```

## 背景

这套 Skill 是我在做 AI 产品内容运营时逐步沉淀的方法论。从手动写作到模板化生产，再到自动化管线，核心经验被结构化成了 AI Agent 可执行的规范。

- Writer Skill 用于生产深度技术长文（公众号）
- XHS Content Skill 用于日更短图文（小红书），配合 AI 日报管线实现半自动化产出

## 致谢

Writer Skill 的框架设计参考了开源社区的 Claude Skill 实践，在此基础上融入了个人的写作风格和运营方法论。

## License

MIT
