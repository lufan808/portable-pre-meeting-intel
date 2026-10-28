# Portable Pre-Meeting Intel

一个不依赖 Mira、sensight 或飞书内部服务的会前人物研究 Skill。

它保留原 `pre-meeting-intel` 的核心方法：

- 默认研究最近 90 天，而不是只复述旧简历；
- 先做人物身份消歧；
- 分为本人表达、社群反应、第三方报道、官方身份四路证据；
- 对照“他如何描述自己”和“别人如何描述他”；
- 强制使用已打开、可验证的来源；
- 生成可直接用于会面的 talking points；
- 在工具不可用时降级为本地 Markdown，而不是阻塞。

## 安装

### Codex

将 `portable-pre-meeting-intel` 目录复制到：

```text
~/.codex/skills/portable-pre-meeting-intel
```

### Claude Code

将同一个目录复制到：

```text
~/.claude/skills/portable-pre-meeting-intel
```

两种运行环境都读取目录中的 `SKILL.md`；`agents/openai.yaml` 只用于 Codex 的界面元数据，不影响 Claude Code。

## 使用示例

```text
准备我和 Rory Sutherland 的会面，重点了解他最近对行为营销和品牌增长的看法。
```

```text
研究 Sam Altman 最近 90 天的公开信号，并告诉我会面时应该问什么。
```

## 明确不包含的能力

本 Skill 不绑定任何内部社交媒体检索后端，不猜测社交媒体链接，不自动访问私密数据，也不把飞书文档写入作为完成条件。
