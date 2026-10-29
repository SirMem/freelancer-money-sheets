# REPLY-BIND · 回令绑定（强化 CLEAR-COST + GATE-IN-CHANNEL）

**One-liner:** 回令必须绑定聊天里那一块 verbatim 粘贴；并列「双主路径同等优先」/中英菜单/再开新门禁文档 = FAIL 降本——不算 CLEAR-COST。

**Parent of:** [CLEAR-COST](CLEAR-COST.md) + [GATE-IN-CHANNEL](GATE-IN-CHANNEL.md). Complements [PREVIEW-CONTRACT](PREVIEW-CONTRACT.md)（字段逐字）与 [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md) L10。

## Why（signals 2026-10-29 ~14:16 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| Paradox of choice / opinionated defaults — [yukaichou.com](https://yukaichou.com/behavioral-analysis/paradox-of-choice-schwartz-choice-overload/) | 默认 = 最强干预；首屏 ≥2 同等选项 = 决策税 |
| Why I Don't Ship Preferences — [jorviksoftware](https://jorviksoftware.cc/notes/2026/04/13/why-i-do-not-ship-preferences) | Opinion 取代 preference；别问「A 还是 C」 |
| One-paste agent onboarding — Traces / Bird | 激活 = 一块粘贴；菜单不是激活 |
| Founder decision bottleneck — [operationsupgrade](https://operationsupgrade.beehiiv.com/p/the-founder-decision-bottleneck) | 重复决策写成**一句规则**；别每次重选 |
| Local anti-pattern 同日 | `ONE-TAP-POST` 仍写「两条主路径同等优先」；`CHAT-REPLY` 并列 A/W/C；`OWNER-FAVOR` 仍指 clear-cost-card 为最低激活 → 与 CLEAR-COST「推荐动作=1」打架 |

## Complements（不替代）

| Gate | Job |
|------|-----|
| [CLEAR-COST](CLEAR-COST.md) | 度量：一张预览 + 一行回令；步骤/未决/秒 |
| [GATE-IN-CHANNEL](GATE-IN-CHANNEL.md) | 通道：预览在已打开聊天；站外 HTML = 镜像 |
| [PREVIEW-CONTRACT](PREVIEW-CONTRACT.md) | 同意语义：动词+对象；字段逐字 |
| **This reinforce** | **绑定**：回令 ↔ 唯一粘贴块；双主路径/中英菜单/新门禁文档 = FAIL |
| [chat-inline-clear.md](chat-inline-clear.md) | **唯一**绑定表面（PRIMARY） |

## Pass rule（Agent 自检）

在 OWNER-FAVOR B=FAIL 时，本轮清闸主交付必须同时满足：

1. **唯一推荐动作** = 朋友圈/同学群 · 故事脚注（不是 A∥C 同等优先）
2. **唯一粘贴块** 出现在聊天 / WakeParent（来自 [chat-inline-clear.md](chat-inline-clear.md)）
3. **唯一回令** 绑定该块：`人情帖已发：朋友圈/同学群·故事脚注 + HH:MM`
4. **零新门禁文档**冒充降本（再开 `*-GATE.md` 而不减少 Kevin 令牌 = L10 FAIL）
5. 备选路径（DM-R1 / C1 / W1/W2 / EN X）仅当 Kevin **明确拒绝** Moments 后才展开；**不得**与推荐动作并列首屏
6. 仍满足 CLEAR-COST / GATE-IN-CHANNEL / PREVIEW-CONTRACT

## Anti-patterns

- 「两条主路径同等优先（二选一即可）」写在 ONE-TAP 首屏
- 聊天正文同时贴中文朋友圈 + 英文 X + C1 让 Kevin 选
- 再写一篇新 `*-GATE.md` 当本轮主进度，而清闸令牌数不降
- 把 clear-cost-card / action-preview-card 标成「Lowest activation」（违反 GATE-IN-CHANNEL）
- 声称 A/W1/W2/C1 PASS（未收到绑定回令）

## Bound surface

Primary: [chat-inline-clear.md](chat-inline-clear.md)  
Optional mirror only: [reply-bind-scorecard.html](reply-bind-scorecard.html)
