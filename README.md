# shit-loop

> **Start from shit, then loop.**

一个给 AI 编码 Agent（如 Claude Code）用的 Skill：在用户完整授权后，自主把一个已经讨论过的方案端到端跑通，先做成一坨屎，再靠定期复盘一轮轮循环变好。

A skill for AI coding agents (e.g. Claude Code): once the user grants full autonomy, carry a previously discussed plan through end to end. Get a rough but complete version working first, then improve it loop by loop through periodic reviews.

## 核心思想 / Core ideas

- **先通后优**：第一目标是端到端跑通，不是一次做到最好。
- **不停下来问，选了就记**：决策点自己选一个推进，可能需要用户参与的写进决策日志。
- **问题不阻塞**：能绕就绕、能降级就降级，记下来继续跑。
- **定期复盘是核心引擎**：执行中约每小时一次，第一项检查目标是否跑偏；跑偏是正常的，关键是能拉回来。
- **在实践中长出错题本**：意外即候选教训，先标"待验证"，用"同类错误是否复发"衡量是否有效，验证、修订、淘汰、升级。
- **授权不改变门禁**：生产写入、不可逆操作、安全与凭据规则照旧。

- **Working first, polish later.** End-to-end first; perfection later.
- **Don't stop to ask; log what you chose.** Pick a default at every decision point and record the ones the user may want to weigh in on.
- **Problems don't block.** Work around or degrade, log it, keep going.
- **Periodic review is the engine.** Roughly hourly during execution; the first check is goal drift — drifting is normal, pulling back is what matters.
- **Grow a lessons notebook from practice.** Surprises become candidate lessons, validated by whether the same mistake recurs.
- **Autonomy does not override safety gates.**

## 安装 / Install

Claude Code：把 `skills/shit-loop` 目录复制到 `~/.claude/skills/`（全局）或项目的 `.claude/skills/`。

```bash
git clone https://github.com/zuozuo/shit-loop.git
cp -r shit-loop/skills/shit-loop ~/.claude/skills/
```

然后在对话里说"完全授权，先实现再优化，跑通整个方案"之类的话，或直接输入 `/shit-loop`。

Then grant full autonomy in chat (e.g. "full authorization, get it working first") or invoke `/shit-loop`.

Skill 正文为中文。The skill body is written in Chinese.

## License

MIT
