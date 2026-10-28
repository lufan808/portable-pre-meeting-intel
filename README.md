# 会前人物情报

一个帮助你在会前快速研究某人的公开信息，并形成可直接使用的会前简报的 Skill。

它会把分散的公开信息整理成一条清晰的当前叙事：

- 研究最近 90 天的公开动态，而不是只复述旧简历；
- 先确认人物身份，避免把同名者混在一起；
- 分析本人表达、社群反应、第三方报道和官方身份四类信号；
- 对照“他如何描述自己”和“外界如何理解他”；
- 使用已经打开并验证过的来源；
- 生成可以直接在会面中使用的中英文问题；
- 输出一份结构清晰、带有可信度和搜索边界说明的 Markdown 简报。

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

## 信息边界

本 Skill 只整理公开信息；不会猜测社交媒体链接，不会访问私密数据，也会明确标注无法验证的内容。
