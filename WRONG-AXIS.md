# WRONG-AXIS · 强化 DISCOVERY-REWARD（impressions ≠ intent · 非 *-GATE）

**One-liner（CN）：** 目录 owner 面板的 impressions / LIVE 计数是错误刻度；判 listing 只看 **intent**（outbound click、陌生人回复、付费/试用）或 **equity**（dofollow + 页面可索引），且 equity ≠ discovery_eligible。

**English short:** Directory impressions and LIVE shelf-count are the **wrong axis**. Score a listing on **intent** (outbound click, stranger reply, trial/paid) or **equity** (followed anchor + indexed page). Equity still does **not** unlock `discovery_eligible` while traction predicates FAIL ([DISCOVERY-REWARD](DISCOVERY-REWARD.md)).

## Why（signals 2026-10-29 ~21:45 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [Indie Hackers · OpenMyPro · 1,534 / 2 / 0](https://www.indiehackers.com/post/1-534-impressions-2-opens-0-clicks-i-was-judging-a-launch-directory-on-the-wrong-axis-54cf2e5fb4) | 1,534 impressions · 2 opens · **0 clicks**; tagline rewrite +18 impressions +0 clicks. Visitors axis would delete it; **followed + indexed** is the other axis. Free tiers often emit **plain-text domain** = badge not equity. |
| [Favors.dev · Launch metrics](https://favors.dev/blog/launch-metrics-to-track) | Impressions = platform rendered your name near someone's thumb. Track qualified visitors / day-7 / permanent assets / named replies — not applause. |
| X [@OperatorOpt](https://x.com/OperatorOpt/status/2113644154484150561) (2026-10-23) | Live Scan: **337 impressions · 0 clicks**; paused engagement. |
| Local audit (this round) | Agent Control / AgentLaunch / Directory Index / AI Product Index LIVE HTTP 200; tool anchors mostly present (dofollow-default or noreferrer≠nofollow). **No** owner-panel impressions; **0** known inbound replies from these shelves → intent FAIL; traction FAIL → `discovery_eligible=false`. |

## Relation to existing cores

| Core | Job | This reinforce adds |
|------|-----|---------------------|
| [DISCOVERY-REWARD](DISCOVERY-REWARD.md) | Causal: traction → discovery; LIVE before traction = inventory | **Measurement axis** once you open a listing panel: which columns count |
| [PROGRESS-MIRAGE](PROGRESS-MIRAGE.md) | Harness PASS ≠ World Δ | Vanity impressions are a mirage column, same family |
| [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md) | More LIVE ≠ first sale | LIVE count itself is vanity when used as progress |
| [CHECKPOINT-LADDER](CHECKPOINT-LADDER.md) | LIVE ≠ rung | Wrong-axis forbids impressions as rung credit |

**≠ new *-GATE / ≠ new core name competing with DISCOVERY-REWARD：** 本文件是 DISCOVERY-REWARD 的刻度强化，禁止另开 `WRONG-AXIS-GATE.md`（L11）。

## Three axes（60s check）

1. **Vanity（ignore as progress）：** impressions, reach, LIVE shelf-count, tagline Δ-impressions, badges.
2. **Intent（primary for demand）：** listing opens → outbound clicks → stranger email/reply → trial/paid. Zero known intent = channel not yet demand.
3. **Equity（secondary durable asset）：** HTML `<a href>` to your domain with **no** `nofollow`/`sponsored`/`ugc`; listing URL `site:`-indexed. `noreferrer noopener` ≠ nofollow. Plain-text domain = badge.

## Rules（本店）

1. Never write「impressions↑ = 分发进度」or「又 LIVE +1 = discovery」。
2. Intent column empty + traction FAIL → channel = inventory (DISCOVERY-REWARD).
3. Equity PASS alone does **not** set `discovery_eligible=true`.
4. Prices Invoice $6 · Expense $5 · Client $5 · Bundle $12 · free $0; practice **$0 spend**; no auto WeChat/X for Kevin clear.
5. L11: no `WRONG-AXIS-GATE.md`.

## Pass rules（WA1–WA5）

| # | Check | PASS | FAIL |
|---|-------|------|------|
| WA1 | Axes named | RESULT separates vanity / intent / equity | Collapses into one LIVE score |
| WA2 | Local LIVE audit | ≥1 LIVE page HTTP 200 + anchor/rel note | Claim without HTML check |
| WA3 | Intent honesty | Explicit 0 known inbound from shelves | Impressions as proxy for demand |
| WA4 | Ties to DISCOVERY-REWARD | equity ≠ discovery_eligible while traction FAIL | Equity→eligible shortcut |
| WA5 | No new *-GATE · $0 · prices | L11 · $6/$5/$5/$12 · 0 spend | New GATE or spend |

## Anti-patterns

- Celebrating directory impressions / tagline rewrite Δ-impressions
- Deleting a dofollow+indexed listing solely because clicks=0 (OpenMyPro caveat) — **and** keeping a nofollow/plain-text badge because impressions look busy
- Treating `noreferrer` as nofollow
- Using equity PASS to claim discovery progress while OWNER-FAVOR still FAIL

## Complements

[DISCOVERY-REWARD.md](DISCOVERY-REWARD.md) · [discovery-reward-scorecard.html](discovery-reward-scorecard.html) · [wrong-axis-scorecard.html](wrong-axis-scorecard.html) · [PROGRESS-MIRAGE.md](PROGRESS-MIRAGE.md) · [ACTIVITY-BIAS-LOCK.md](ACTIVITY-BIAS-LOCK.md).
