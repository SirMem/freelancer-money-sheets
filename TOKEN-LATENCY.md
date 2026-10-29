# TOKEN-LATENCY · 强化 CLEAR-COST（非新门禁）

**One-liner:** 清闸只计 **first action**（绑定回令收到）；开分数卡 / 货架 LIVE / 多开预览 = **0** 激活完成分。聊天内路径 token=1、≈60–90s；任何「先开页」路径多 ≥1 次打开 + 更高延迟 = 相对 chat-inline **FAIL**。

**Parent of:** [CLEAR-COST](CLEAR-COST.md)（计量）。Complements [REPLY-BIND](REPLY-BIND.md) / [GATE-IN-CHANNEL](GATE-IN-CHANNEL.md) / [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md)。**不是**新的 `*-GATE.md`。

## Why（signals 2026-10-29 ~15:22 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| Waitlist→Activation one ping — [thefirstusers.com](https://thefirstusers.com/waitlist-to-signup-activation-ping) | 转化事件 = 一条消息 + 一次 tap + **first action**；庆祝的是完成动作，不是点击/开页 |
| TikTok in-feed one-tap checkout (X · Oct 2026) | 客户**不离开**当前面；多跳 = 激活税 |
| IH · empty dashboard / choice overload | 「太多选项不知先做啥」→ 激活=0；并列路径拖死 first action |
| Local same-day leak | `clear-cost-scorecard.html` 仍写「打开 clear-cost-card」为第 1 步 → 违反 GATE-IN-CHANNEL / REPLY-BIND |

## Metric（Agent 自检）

| Path | Kevin tokens | Page opens | Est. seconds | Clear-complete? |
|------|--------------|------------|--------------|-----------------|
| **★ chat-inline**（PRIMARY） | **1**（绑定回令） | **0** | **60–90** | 仅当收到 `人情帖已发：…+ HH:MM` |
| Open HTML scorecard → copy → post → reply | 1 | ≥1 | 120–180+ | 多打开 = 更高延迟；**不得**标 Lowest |
| Dual A∥C / EN·CN menu | ≥2 决策 | 0–1 | 不定 | **FAIL**（REPLY-BIND） |
| Shelf PR / directory LIVE while B=FAIL | 0 from Kevin | n/a | n/a | **0** CLEAR-COST 完成分（ACTIVITY-BIAS） |

## Pass rule

1. 本轮主交付若声称「降清闸成本」，必须给出 **token / page-opens / est-seconds** 对照表（见 scorecard）。
2. chat-inline 路径必须在表上 **严格更优**（token≤、opens=0、seconds≤）。
3. 任何分数卡「下一步」**禁止**写「先打开 HTML」；唯一下一步 = 复制聊天块 → 发 → 回绑定令牌。
4. 零新并列 `*-GATE.md` 冒充降本（继承 REPLY-BIND L10）。

## Bound surface

Primary: [chat-inline-clear.md](chat-inline-clear.md)  
Optional mirror: [token-latency-scorecard.html](token-latency-scorecard.html)
