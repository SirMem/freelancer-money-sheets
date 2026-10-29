# DISCOVERY-REWARD · 发现=对已有 traction 的奖励（核心 · 非 *-GATE）

**One-liner（CN）：** 目录/市场「发现」是对已有 traction 的奖励，不是冷流量来源；在人情/首单/联盟未破前只堆 LIVE 上架 = 库存上架，不算分发。

**English short:** Marketplace/directory discovery is a **reward for traction you already have** (first sale, warm owner favor, affiliate held link, owned list), not a cold-traffic source. Listing before traction is inventory shelving, not distribution.

## Why（signals 2026-10-29 ~21:22 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [Otto Automaton DEV · 11 cycles · $0](https://dev.to/ottoautomaton/im-an-autonomous-ai-agent-running-a-real-business-11-cycles-in-ive-made-0-heres-the-wall-i-4agg) | Marketplace "discovery" is a **reward for traction you already have**, not a source of it; **30 days** marketplace = **1 view**, **$0** |
| [Saucekit · marketplace or own page](https://saucekit.so/blog/ai-skill-marketplace-or-your-own-page) | Marketplace is a **channel**; listing does **not** create demand |
| X [@krishav_kr9125](https://x.com/krishav_kr9125/status/2111681462626091246) (2026-10-18) | Directory visits ≠ sales (**$0**) |
| X [@zentricod](https://x.com/zentricod/status/2092658351733670290) | Discover fee economics vs direct — platform cut ≠ free cold traffic |
| Local same-day money loops | Many Friday Invoice Chase Ranker directory LIVEs (Agent Control / AgentLaunch / Directory Index / AI Product Index / …) while **OWNER-FAVOR A/W1/W2 + WeChat C1 + Affiliates R0** still **FAIL**; Gumroad sales **Δ≈0** |

## Relation to existing cores

| Core | Job | This core adds |
|------|-----|----------------|
| [PROGRESS-MIRAGE](PROGRESS-MIRAGE.md) | Harness PASS ≠ World Δ; self-grade gates create mirage | Mirage is **channel type** (self-score vs world); DISCOVERY-REWARD names the **platform causal arrow** traction→discovery |
| [AUDIENCE-RENT](AUDIENCE-RENT-GATE.md) | Rent someone else's audience on commission | Rent still needs a held link / partner; empty LIVE shelves do not substitute |
| [CHECKPOINT-LADDER](CHECKPOINT-LADDER.md) | Dense mid-run ladder; LIVE ≠ rung | Ladder forbids LIVE as rung; this core forbids LIVE as **discovery credit** until traction predicates true |
| [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md) | Shelf/LIVE ≠ first-sale while B=FAIL | Formalizes why more LIVE is inventory bias, not distribution progress |
| [WARM-FIRST](WARM-FIRST.md) | Discover needs ≥1 counted paid sale | Aligns: Discover/directory reward after counted traction |

**Harder / distinct from PROGRESS-MIRAGE：** PROGRESS-MIRAGE says 「LIVE/自评分 ≠ 店进度」；DISCOVERY-REWARD 钉平台因果：**先有 traction → 才有 discovery**。把 Agent Control / AgentLaunch LIVE 写成「分发进度」= 把因果箭头反过来。

**≠ new *-GATE：** 本核是分发/发现因果纪律，不是第二道 Kevin 批准类（L11）。禁止另开 `DISCOVERY-REWARD-GATE.md`。

## Rules（本店）

1. **Traction before discovery credit：** 只有当至少一条 traction 谓词为真时，目录/市场 LIVE 才可记为 **discovery_eligible**：OWNER-FAVOR A **或** W1 **或** W2 **或** WeChat C1 已发 **或** Affiliates R0 有持链回复 **或** 付费首单。当前全 FAIL → `discovery_eligible=false`。
2. **LIVE = inventory when ineligible：** `discovery_eligible=false` 时，任何目录 LIVE 计数 = **库存上架**，不得写入「分发进度 / World Δ / discovery」。
3. **Causal arrow：** 平台发现流量奖励已有 traction；不得假设「上架越多 → 冷流量越多 → 首单」。
4. **Directory LIVE ≠ distribution：** Agent Control / AgentLaunch / Directory Index / AI Product Index / SarnAI 等 LIVE **≠** 分发进度，直到 traction 破。
5. **Prices / spend：** Invoice $6 · Expense $5 · Client $5 · Bundle $12 · Aging/ADHD free $0；本核实践 **$0 spend**；不代发 X/微信。
6. **L11：** 不新开 `DISCOVERY-REWARD-GATE.md`；不抢 Kevin 回令。

## Pass rules（Agent 自检 · DR1–DR5）

| # | Check | PASS | FAIL |
|---|-------|------|------|
| DR1 | Traction predicates listed | RESULT 列出 A/W1/W2/C1/R0/首单；全 FAIL → `discovery_eligible=false` | 省略谓词或自称 eligible |
| DR2 | LIVE count = inventory when ineligible | 目录 LIVE 标库存，不给 discovery credit | 「又 LIVE = 分发+1」 |
| DR3 | No new *-GATE | 核心名 DISCOVERY-REWARD；L11 | 新开 DISCOVERY-REWARD-GATE.md |
| DR4 | Prices / $0 spend | $6/$5/$5/$12 · free $0 · no spend | 改价或花钱未确认 |
| DR5 | World Δ≈0 until traction | 显式 Δ≈0；人情/首单仍 FAIL | 把 LIVE 写成 World Δ+ |

## Anti-patterns

- 把 Agent Control / AgentLaunch / Directory Index LIVE 写成「分发进度」而 traction 仍 FAIL
- 「今天又上了 N 个目录所以发现流量会来」
- 另开 `DISCOVERY-REWARD-GATE.md`
- 用目录 visits 当销量代理（@krishav_kr9125：$0）
- 在 OWNER-FAVOR 未清前继续堆 LIVE 当主工作



## Hook · WRONG-AXIS（reinforce · 2026-10-29 ~21:45）

目录面板 **impressions / LIVE 计数** 是错误刻度（IH OpenMyPro 1534/2/0；Favors.dev；X @OperatorOpt 337/0）。判 listing 只看 **intent** 或 **equity**；equity ≠ `discovery_eligible`。见 [WRONG-AXIS.md](WRONG-AXIS.md) · [wrong-axis-scorecard.html](wrong-axis-scorecard.html)。

## Complements

见 [PROGRESS-MIRAGE.md](PROGRESS-MIRAGE.md) · [CHECKPOINT-LADDER.md](CHECKPOINT-LADDER.md) · [ACTIVITY-BIAS-LOCK.md](ACTIVITY-BIAS-LOCK.md) · [AUDIENCE-RENT-GATE.md](AUDIENCE-RENT-GATE.md) · [WARM-FIRST.md](WARM-FIRST.md) · [discovery-reward-scorecard.html](discovery-reward-scorecard.html) · [chat-inline-clear.md](chat-inline-clear.md)。


## Hook · CHANNEL-RANK（reinforce · 2026-10-29 ~22:18 Asia/Shanghai）

**One-liner add-on：** 首单渠道有分母排序——别人已建好的社区/线程（borrowed demand）≈34%，自有受众≈20%，1:1 冷触≈15%，**PH/市场/目录≈10%**；在 traction FAIL 时继续堆 LIVE = 把最低分母渠道当主路径。≠新核名；≠新 *-GATE（L11）。

| Signal | Point |
|--------|-------|
| [Lead Scorer · 70 first-customer cases 2024–2026](https://lead-scorer.com/blog/how-founders-get-first-customers-2026) | Named channels n=59: borrowed communities **34%** (Reddit 15) · owned audience **20%** · 1:1 cold **15%** · **PH/marketplaces/directories 10%** · SEO 8% · personal network 7% · **paid ads 0/66**. Launch ≠ distribution plan. |
| X [@YoannaJuille](https://x.com/YoannaJuille/status/2109939921808933180) (2026-10-13) | Launch day: **4,000+** X impressions · **35** site visits · **0** sales — vanity≠demand (WRONG-AXIS sibling). |
| [IH Rareș · $176 first month](https://www.indiehackers.com/post/i-made-176-in-my-first-month-heres-what-worked-and-what-didn-t-330cc528a7) (2026-03) | Every sale from **direct person engagement** (IH / cold DM / Reddit thread); X BIP **72K views → $0**; SEO 6mo → $0. Already cited in OWNER-FAVOR; here as channel-rank corroboration. |
| Local | Friday Invoice Chase Ranker: many directory LIVEs (Ignlab / UniLink / Agent Control / …) while **OWNER-FAVOR A/W1/W2 + WeChat C1 + Affiliates R0** FAIL → activity mass sits in the **10% bucket**, not the 34% borrowed-demand bucket. |

**Rules add-on：**
1. When ranking next hour of work, prefer a **borrowed-demand place** (thread where invoice/late-pay pain is already written) or **owner favor** over another Instant shelf.
2. Channel-rank does **not** unlock `discovery_eligible`; traction predicates unchanged.
3. Do not invent `CHANNEL-RANK-GATE.md`.

See [discovery-reward-channel-rank-scorecard.html](discovery-reward-channel-rank-scorecard.html) · [WRONG-AXIS.md](WRONG-AXIS.md) · [OWNER-FAVOR-GATE.md](OWNER-FAVOR-GATE.md) · [AUDIENCE-RENT-GATE.md](AUDIENCE-RENT-GATE.md).


## Sibling · OUTREACH-BIMODAL（NEW · 2026-10-29 ~22:53 Asia/Shanghai）

**Within cold outreach** (not a discovery/listing axis): reply rates are **bimodal** — ≤50 hand-qualified → 14–58% & ≥1 paying in all 6 Lead Scorer cases; ≥300 scrape → ~1% & first sales≈0. Variable = list + known facts, not copy volume. Prefer [ICP-ROSTER.md](ICP-ROSTER.md) warm; cold hand-qual ≤15 pending. ≠ CHANNEL-RANK / WRONG-AXIS / *-GATE（L11）。

See [OUTREACH-BIMODAL.md](OUTREACH-BIMODAL.md) · [outreach-bimodal-scorecard.html](outreach-bimodal-scorecard.html) · [HAND-QUAL-CHECKLIST.md](HAND-QUAL-CHECKLIST.md) · [QUALIFIED-COLD-ROSTER.md](QUALIFIED-COLD-ROSTER.md).
