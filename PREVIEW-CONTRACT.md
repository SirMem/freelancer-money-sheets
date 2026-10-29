# PREVIEW-CONTRACT · 预览即契约（REINFORCE CLEAR-COST）

**One-liner:** 清闸确认不能只问「允许发吗」——**预览即契约**：卡上逐字段原文 = 将要发生的唯一动作；类目确认是反模式；批准后改文案必须重开一张卡。

父核：[CLEAR-COST.md](CLEAR-COST.md)（一张卡 + 一行回令）。本轮把「预览」从口号钉成**同意机制**。

## Why（signals 2026-10-29 ~13:23 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [Action Preview · Agent Consent](https://agentconsent.dev/patterns/action-preview/) | 类目确认（"Allow send?"）与具体动作之间有类型错误；同意需要可辨识实例 |
| 预览=契约 | 卡上参数 ↔ 执行路径必须双射；批准后改文 = 毁约，须新卡 |
| Friction budget | 可逆低风险动作不要预览（训练盲目点是）；高后果外部可见才花确认预算 |
| 按钮动词 | 批准钮写动作（「复制并去发」），不是「OK / 确定」 |
| X / indie | 「Distribution is infrastructure」≠ 再开 PR；降激活能的卡才是基建 |
| Local | clear-cost-card 已有粘贴正文，但标题/按钮仍偏「说明页」→ 本轮改成 Action Preview 解剖 |

## Complements（不替代）

| Gate | Job |
|------|-----|
| [CLEAR-COST](CLEAR-COST.md) | 合法进度度量：1 动作 + 预览 + 回令 |
| **This reinforce** | 预览的**同意语义**：类目≠令牌；双射；按钮动词 |
| [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md) | 什么不算进度 |
| [OWNER-FAVOR-GATE](OWNER-FAVOR-GATE.md) | 仍须清的暖单元 |

## Pass rule（卡自检 · 叠在 CLEAR-COST 上）

1. **标题 = 动词 + 对象**（例：「发朋友圈故事脚注」），禁止「确认操作 / 请审阅」
2. **字段逐字**：渠道 / 正文 / 配图 / 回令 — 不摘要成「Dana 等 2 人」式糊弄
3. **批准钮写动作**；拒绝钮便宜且不恐吓
4. **批准后禁止静默改文**；改了 = 新卡 + 新回令
5. **不预览可逆草稿**（写 md / 搜 X）浪费摩擦预算

违规：再开「也可以发连接者 / 也可以 Affiliates」并列菜单当主进度；或把类目确认（「是否允许 Agent 发帖？」）当清闸。

## Artifact

- 契约卡：[action-preview-card.html](action-preview-card.html)（可分发）
- 分数卡：[preview-contract-scorecard.html](preview-contract-scorecard.html)
- 旧卡仍可用：[clear-cost-card.html](clear-cost-card.html) — 本轮推荐契约卡

## Anti-patterns

- 用 PREVIEW-CONTRACT 再拆 5 个新门禁文件
- 声称 A/W1/W2/C1 PASS（未收到 Kevin 回令）
- 把 Intent-watch / 冷回复冒充「已清闸」
