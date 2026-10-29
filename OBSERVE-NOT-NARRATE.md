# OBSERVE-NOT-NARRATE · 独立证据先于 Agent 叙事（核心 · 非 *-GATE）

**One-liner（CN）：** Exception-only / 人在环上（HOTL）在证据只靠 Agent 自述时是不安全的；主张必须有独立于叙事、且能在执行后存活的出处（URL / HTTP / commit / 工具原始结果）；生成≠评判；一次违约就要降阶——否则「自治」只是信任剧场。

**English short:** You cannot safely raise work to exception-only / human-on-the-loop if the only evidence is the agent's own narrative. Claims need independent provenance that survives the run (URL/HTTP/commit/raw tool result). Generation ≠ judgement. Demotion is hair-triggered on one breach. Without that, autonomy is trust theater.

## Why（signals 2026-10-29 ~17:15 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [harten.io · Human cannot be the bottleneck](https://harten.io/papers/01-2-human-cannot-be-the-bottleneck/) | HITL→HOTL；证据须独立于 Agent 叙事；Agent 不可批改自己的作业；证据须在执行后仍存活 |
| [Govenant · Autonomy and resilience](https://govenantstandard.org/standard/07-autonomy-and-resilience/) | Earned autonomy；**一次违约即降阶**；NEVER_AUTO 钉死；监视器独立于被监视的失败模式 |
| X [@GuyGotThis](https://x.com/GuyGotThis/status/2115129913573593358) | 真测是拒绝率；99% 批准 = 自动化橡皮图章 |
| X [@weipanux](https://x.com/weipanux/status/2115718260092002555) | Human in the loop ≠ human judging |
| Local same-day money | CurlShip / DevElif / AI Startup Hub LIVE 常有 RESULT 复述 Agent 主张；OWNER-FAVOR 仍 FAIL — 目录 LIVE 不是清闸证据 |

## Relation to existing cores

| Core | Job | This core adds |
|------|-----|----------------|
| [EXCEPTION-ONLY](EXCEPTION-ONLY.md) | Raise reversible/low-blast to rung3+；keep OWNER-FAVOR at approve-before；L11 | **Raise is invalid** without independent surviving evidence + demotion path |
| [CLEAR-COST](CLEAR-COST.md) / [TOKEN-LATENCY](TOKEN-LATENCY.md) | Lower cost of the one Kevin clear；chat-inline | Score whether the **log** is evidence or narrative (not just whether clear is cheap) |
| [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md) | Shelf/LIVE ≠ first-sale progress while B=FAIL | LIVE claim must cite URL/HTTP/raw；narrative-only RESULT = FAIL evidence |
| [OWNER-FAVOR-GATE](OWNER-FAVOR-GATE.md) | Irreversible warm unit stays rung2 | OWNER-FAVOR ∈ NEVER_AUTO；Agent 不可自标 PASS |

**Harder than EXCEPTION-ONLY alone：** EXCEPTION-ONLY 说「升阶」；OBSERVE-NOT-NARRATE 说「没有独立存活证据就不得升阶」。

## Rules

1. **Independent provenance：** 每个可核对主张须引用独立于 Agent 叙事的出处 — URL · HTTP status · git commit SHA · 工具原始 JSON/HTML（落盘路径）。「我觉得 LIVE 了」= FAIL。
2. **Survives the run：** 证据必须在本轮结束后仍可复核（公开页 / 原始响应文件 / commit），不能只活在聊天摘要里。
3. **Generation ≠ judgement：** 生成 RESULT / 分数卡的 Agent **不得**给自己判 PASS。评判字段须可被独立复核或留给主人/事后审。
4. **Demotion hair-trigger：** 一次证据违约（假 LIVE、无出处、自批改作业）→ 该类决策立刻降阶（rung4→3 或 3→2），直到重新赢得证据。
5. **NEVER_AUTO pinned：** OWNER-FAVOR · Spend / 付费投放 · 代发人情 · 代说「是」— 永不静默升阶；见 EXCEPTION-QUEUE packet + SAY-YES LOCK。
6. **Reject/defer rate：** 对开着的 Kevin 闸，若长期 100%「建议批」而无 defer/reject 路径记录 = 橡皮图章风险（cite @GuyGotThis）。本店：OWNER-FAVOR 仍 FAIL = 正确 defer，不是卡死。

## Pass rules（Agent 自检 · E1–E6）

| # | Check | PASS | FAIL |
|---|-------|------|------|
| E1 | Claim cites independent URL/HTTP/commit/raw | 主张旁有可点出处或落盘原始结果 | 仅 Agent 复述 |
| E2 | Generation ≠ judgement | 分数卡/RESULT 不自封不可逆 PASS | Agent 自标 OWNER-FAVOR PASS |
| E3 | Demotion path named | 文档写明一次违约如何降阶 | 只有升阶叙事 |
| E4 | RESULT fails if only self-narrative | 无出处的 LIVE/进度主张 → RESULT FAIL 或降级措辞 | 叙事当进度 |
| E5 | NEVER_AUTO includes OWNER-FAVOR / Spend | 钉在清单且本轮未静默升阶 | 暗示「可代发/代花」 |
| E6 | Reject/defer rate tracked for open gate | 开闸状态显式 FAIL/待 Kevin；非假 PASS | 开闸却记清闸进度 |

## Anti-patterns

- RESULT.md 只写「已 LIVE」而无 URL / HTTP / 原始 JSON 路径
- 用分数卡 HTML 自己给自己打 PASS（生成=评判）
- 把目录 LIVE 写成 OWNER-FAVOR / CLEAR-COST 进度
- 升 rung3+ 却无 demotion / NEVER_AUTO 条款
- 另开并列 `*-GATE.md` 抢注意力（违反 L11）
- 空喊「请批准」而无独立证据字段（违反 EXCEPTION-QUEUE）

## Complements（不替代 · 不发明并列 GATE）

见 [EXCEPTION-ONLY.md](EXCEPTION-ONLY.md) · [JOB-CONTRACT.md](JOB-CONTRACT.md)（验收测试先于动手） · [SLICE-LOCK.md](SLICE-LOCK.md)（per-slice 基线；mean PASS 仍可藏局部 FAIL） · [CLEAR-COST.md](CLEAR-COST.md) · [ACTIVITY-BIAS-LOCK.md](ACTIVITY-BIAS-LOCK.md) · [chat-inline-clear.md](chat-inline-clear.md) · [observe-not-narrate-scorecard.html](observe-not-narrate-scorecard.html)。

## Audit note · money-loop ~17:13

`/workspace/sidehustle/money-loop-2026-10-29-1710/RESULT.md`：AI Startup Hub LIVE 主张旁有 `POST → 201`、`GET → 200`、公开 URL，且同目录有 `submit-response.json` / `get-product.json` — **本轮该主张偏证据（E1 PASS）**。风险仍在：历史多轮 RESULT 常复述 Agent 叙事；本核钉死「无独立存活出处 = 不得当进度」。
