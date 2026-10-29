# CHECKPOINT-LADDER · 密检查点梯子（核心 · 非 *-GATE）

**One-liner（CN）：** 长目标不能只靠终点二元 PASS/FAIL；要用有序密梯子 + 周期性外环检查点——否则既丢掉中间进度，也掩盖中途覆盖/回退（终局分数低于更早检查点）。≠ PROGRESS-MIRAGE（闸门信道/自评分），≠ SLICE-LOCK（跨切片均值掩盖），本核钉「单次长跑时间轴上的密检查点」。

**English short:** For long-horizon goals, binary end-of-run verdicts discard partial progress and hide mid-run regressions (final reward below an earlier checkpoint). Use an ordered dense progress ladder + periodic out-of-band checkpoints; keep the official binary beside the dense score, not instead of it.

## Why（signals 2026-10-29 ~19:45 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [LHTB 2.0 · arXiv/html 2610.14146](https://arxiv.org/html/2610.14146) | Verifier every **30 min**; **65** trajectories final reward **below** earlier checkpoint (**55** continuing declines); reconstruction binary mean **0.221** vs dense ladder **0.653** |
| [Checklist Partial-Credit Scoring](https://agentpatternscatalog.github.io/patterns/patterns/checklist-partial-credit-scoring.html) | Ordered checkpoints; **no credit for later without earlier**; claim≠trace; report **graded score beside binary** |
| [Scale Labs · verifier design for CUA](https://labs.scale.com/blog/verifier-design-for-cua) | Hard gates **+** dense rewards — not either alone |
| X [@Kizuno18](https://x.com/Kizuno18/status/2115014885218148458) | Regulator cannot live inside the system; need **out-of-band** circuit breakers |
| Local same-day money loops | Directory LIVE / SCORE PASS 堆叠，而 OWNER-FAVOR ladder rung 仍 **0** — 日终二元「目录很多」掩盖 Clear-Cost / warm 零进度 |

## Relation to existing cores

| Core | Job | This core adds |
|------|-----|----------------|
| [PROGRESS-MIRAGE](PROGRESS-MIRAGE.md) | Harness PASS ≠ World Δ; self-grade gates create mirage | Mirage is about **channel type**; ladder is about **time-axis density** on one long run |
| [SLICE-LOCK](SLICE-LOCK.md) | Per-slice baselines; mean masks regressions | Slice-lock is **cross-slice**; ladder is **ordered rungs on one timeline** |
| [OBSERVE-NOT-NARRATE](OBSERVE-NOT-NARRATE.md) | Claims need independent surviving provenance | Provenance of a late claim ≠ earlier rung held; need mid-run checks |
| [EDIT-TRIGGERED](EDIT-TRIGGERED.md) | Target↑ + protect + edit-path trigger | Trigger at T≠ proves ladder rung at T0..Tn still green |
| [JOB-CONTRACT](JOB-CONTRACT.md) | Six-field job before run | Acceptance should name ladder rungs + checkpoint cadence, not only end binary |
| [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md) | Shelf/LIVE ≠ first-sale while B=FAIL | LIVE stack ≠ climbing OWNER-FAVOR rungs |
| [CLEAR-COST](CLEAR-COST.md) | One chat paste ↔ one bound reply | Clear-Cost packet ready = rung 0; send/reply climb later rungs |

**Orthogonal to PROGRESS-MIRAGE：** 信道类型 vs 时间轴密检查点——两者可同时踩雷（自评分 + 只看终点）。

**Orthogonal to SLICE-LOCK：** 跨切片均值掩盖 vs 单次长跑中途回退——目录 LIVE 切片 PASS 不推进人情梯子。

**≠ new *-GATE：** 本核是进度/验收形状纪律，不是第二道 Kevin 批准类（L11）。

## Rules（本店）

1. **Ordered ladder：** 首单路径用有序梯档，例如 (0) Clear packet ready → (1) Kevin sent warm/story → (2) reply/token → (3) first paid。后档不得跳过前档计分。
2. **Dense + binary side-by-side：** RESULT 报告 **当前 rung** + **graded ladder score**，并保留官方二元（首单有/无）。禁止只用日终「PASS/FAIL」或「目录很多」。
3. **Mid-run checkpoints：** 长跑至少 morning / noon / evening（或等价周期）记 **World Δ + harness**；若终局低于更早检查点 → 标 **REGRESSION-ON-LADDER**，不得装「整轮成功」。
4. **Directory LIVE ≠ rung advance：** 目录提交 / SCORE PASS / hub 核心落地 **不** 推进 OWNER-FAVOR 梯子。那是 harness / boundary 切片。
5. **Out-of-band verifier：** 检查点读外环证据（人情是否发出、回令、销量），不得只读本轮 RESULT 自述（配合 PROGRESS-MIRAGE + @Kizuno18）。
6. **L11：** 不新开 `CHECKPOINT-LADDER-GATE.md`；不抢 Kevin 回令。

## Pass rules（Agent 自检 · L1–L6）

| # | Check | PASS | FAIL |
|---|-------|------|------|
| L1 | Ordered rungs named | RESULT 有 0..n 梯子定义 | 只有终点二元 |
| L2 | Current rung + regression | 写明当前档；若回退显式 | 省略中途回退 |
| L3 | Graded beside binary | 密分数与官方二元并列 | 只用 PASS/FAIL 或只密不二元 |
| L4 | Mid-run checkpoints | ≥2 时点 WorldΔ+harness | 只日终一刀 |
| L5 | LIVE ≠ rung | 目录 LIVE 不标成梯子前进 | 「又 LIVE 了所以进度+1」 |
| L6 | No new *-GATE | 核心名 CHECKPOINT-LADDER；L11 | 新 GATE / 第二回令 |

## Anti-patterns

- 日终「今天目录很多 = 赚钱循环成功」
- 把 SCORE PASS / hub commit 计为 OWNER-FAVOR rung+1
- 跳过 rung0（Clear packet）直接自称 warm 进度
- 终局低于 noon 检查点却仍写 Overall PASS
- 另开 `CHECKPOINT-LADDER-GATE.md`

## Complements

见 [PROGRESS-MIRAGE.md](PROGRESS-MIRAGE.md) · [SLICE-LOCK.md](SLICE-LOCK.md) · [OBSERVE-NOT-NARRATE.md](OBSERVE-NOT-NARRATE.md) · [EDIT-TRIGGERED.md](EDIT-TRIGGERED.md) · [JOB-CONTRACT.md](JOB-CONTRACT.md) · [ACTIVITY-BIAS-LOCK.md](ACTIVITY-BIAS-LOCK.md) · [CLEAR-COST.md](CLEAR-COST.md) · [checkpoint-ladder-scorecard.html](checkpoint-ladder-scorecard.html) · [chat-inline-clear.md](chat-inline-clear.md)。

## Reinforce · CURRENT-STATE（2026-10-29 ~20:54 · 非新门禁）

**One-liner add-on:** 梯子计分必须用 **当前仍成立的谓词**（current-state），不能用「曾经摸到过的峰值」当 credit。历史峰值 / 曾 LIVE / 曾 PASS 在回退后仍挂在分数上 = **HISTORICAL-PEAK 幻觉**；PartHackBench 里 historical credit 均膨胀 **0.252**、严格回退检出 **0/14**，而 current-state 规则膨胀 **0**、检出 **14/14**。

| Signal | Point |
|--------|-------|
| [PartHackBench · arXiv/html 2609.29578](https://arxiv.org/html/2609.29578) | Historical/max 峰值 credit 对 matched 终局膨胀 mean **.252**（ASR 10/15）；rollback 检出 **0/14**；CSPS/current-state **Δhack=0** · rollback **14/14** |
| [LHTB 2.0 · 2610.14146](https://arxiv.org/html/2610.14146)（父核已引） | 30min verifier 暴露终局低于更早检查点——密检查点须读**当下**状态，不是历史高水位 |
| X [@brendenvonhouse](https://x.com/brendenvonhouse/status/2108760682435162224) | 「draft in a folder = partial credit；我只在它 live on the site 时计分」→ 当前可观察态 |
| X [@baboonAI4S](https://x.com/baboonAI4S/status/2114246198609776735) | 长跑 ~step 12 静默改需求 = drift；峰值叙事掩盖当前不合格 |
| X [@ashwinsuriya](https://x.com/ashwinsuriya/status/2115777815329325184) / Thruline | 测试「看起来过了」≠ 动作真实发生；核对当前外环证据 |
| X [@ba3hit](https://x.com/ba3hit/status/2115780343341129871) | 长会话忘已改内容；步间要 checkpoint **state** |
| Local same-day | 目录 LIVE 堆叠 = 历史峰值 harness；OWNER-FAVOR **current rung 仍 0**；不得把曾 LIVE 计成 rung+ |

**Rules（钉在 CHECKPOINT-LADDER 上，≠新 *-GATE）：**

1. **Current predicates only：** 梯档得分 = 此刻谓词仍真（人情已发出、绑定回令在、付费单在）。曾 READY / 曾 LIVE / 曾 SCORE PASS **不再真** → 不得保留 credit。
2. **Historical-peak FAIL：** 用「本周最多 LIVE 数 / 曾爬到过的叙事档」替代当前 rung → **FAIL**（对偶 PartHackBench historical witness）。
3. **Rollback sensitivity：** 若外环证据消失（回令撤回、帖删、单退）→ 当前 rung **必须下降**并标 REGRESSION-ON-LADDER；禁止挂 stale 峰值。
4. **Directory LIVE ≠ durable rung：** LIVE 是边界切片瞬时态；不写入 OWNER-FAVOR 当前谓词向量。
5. **L11/L12：** 不新开 `CURRENT-STATE-GATE.md` / `HISTORICAL-PEAK-GATE.md`。

对照卡（可选镜像）：[checkpoint-current-state-scorecard.html](checkpoint-current-state-scorecard.html)。父核分数卡：[checkpoint-ladder-scorecard.html](checkpoint-ladder-scorecard.html)。
