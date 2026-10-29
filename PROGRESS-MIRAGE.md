# PROGRESS-MIRAGE · 自评分造进步幻觉（核心 · 非 *-GATE）

**One-liner（CN）：** Agent 自评分 / 只读 transcript·diff 的带内评判当闸门时，会造「进步幻觉」：每轮都自称变好，但实测世界 Δ 为零或为负过半。开放目标的成功信号若在 transcript 外，**带外世界状态闸**是结构要求，不是锦上添花；放大评判模型挡不住幻觉。

**English short:** When the loop gate is the agent's self-score or an in-band judge that only reads the transcript/diff, you get a **progress mirage**—claimed improvement every cycle while measured real-world Δ is ≤0 on a majority of cycles. For open-ended goals whose success signal lives outside the transcript, **out-of-band world-state evaluation is structural**. Scaling the judge does not close the gap.

## Why（signals 2026-10-29 ~19:22 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [Progress Mirage · arXiv 2607.25152](https://arxiv.org/abs/2607.25152) | 54 cycles: frontier agent claimed improvement **every** time; **56%** measured Δ ≤0；self-verdict → accept-all；best deployed state eroded **19%** |
| Same paper · in-band judge | Strongest in-band judge (full artifact + diff + verdict history) still accepted **44%** real regressions and rejected **38%** real improvements |
| Same paper · boundary task | When success is verifiable **from the artifact itself**, mirage → 0 — gap depends on **where the success signal resides** |
| [Anthropic · Demystifying evals](https://www.anthropic.com/research/demystifying-evals-for-ai-agents) | Capability vs **regression** suites；hill-climb without regression gate = silent backslide |
| [Google · Past the vibe check](https://developers.googleblog.com/evaluating-ai-agents-moving-past-the-vibe-check/) | Boolean gates + **zero regression** on core metrics；don't throw tests / move the baseline |
| X [@eveliqTrace](https://x.com/eveliqTrace/status/2102137683287929180) | SELF-MODIFICATION ≠ SELF-IMPROVEMENT；BENCHMARK GAIN ≠ VERIFIED SYSTEM IMPROVEMENT |
| X [@MyndfulDave](https://x.com/MyndfulDave/status/2114026419697455355) | New eval beat old? Same inputs? Quietly easier test set ≠ progress |
| Local same-day loops | 多轮 RESULT「SCORE PASS」+ 目录 LIVE，而 Gumroad 销量 Δ≈0、OWNER-FAVOR 仍 FAIL — 典型 mirage 表面 |

## Relation to existing cores

| Core | Job | This core adds |
|------|-----|----------------|
| [OBSERVE-NOT-NARRATE](OBSERVE-NOT-NARRATE.md) | Claims need independent surviving provenance | Provenance of a **transcript claim** still leaves mirage if the **gate** is in-band; need **world Δ** channel |
| [EDIT-TRIGGERED](EDIT-TRIGGERED.md) | Target↑ + protect + edit-path trigger | Trigger proof ≠ measured shop progress; POST sid can PASS while sales Δ=0 |
| [SLICE-LOCK](SLICE-LOCK.md) | Per-slice baselines; mean masks regressions | Add a mandatory **world-Δ slice**; harness PASS must not swallow Δ≤0 |
| [JOB-CONTRACT](JOB-CONTRACT.md) | Six fields + acceptance before run | Acceptance test for open goals must name an **out-of-band** oracle when success lives outside transcript |
| [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md) | Shelf/LIVE ≠ first-sale while B=FAIL | Formalizes why LIVE+self-PASS is mirage, not SCOPE-FAIL alone |

**Harder than OBSERVE alone：** OBSERVE 要存活出处；PROGRESS-MIRAGE 说出处仍可在带内，**闸门信道类型**才决定是否幻觉。

**Harder than EDIT-TRIGGERED alone：** EDIT 证明改动路径开火；PROGRESS-MIRAGE 证明开火+叙事好看 ≠ 世界 Δ。

**≠ new *-GATE：** 本核是评估/验收纪律，不是第二道 Kevin 批准类（L11）。

## Rules（本店）

1. **Separate channels：** 每轮 RESULT 必须分列 **Harness / practice PASS** 与 **World Δ**（销量、回令、人情是否发出、客单价等）。禁止把前者写成店进度。
2. **Self-verdict ≠ gate for open goals：** Agent 不得用「我读了自己的 RESULT/分数卡」关闭开放目标验收。带内 LLM 复读 transcript/diff 同理。
3. **World-Δ slice always present：** 即使 Δ=0 / OWNER-FAVOR FAIL，也要**显式**写出，不得省略装绿。
4. **Accept-all smell：** 连续 ≥3 轮自称「变好」且 World Δ 无正值 → 标 **MIRAGE-RISK**，停止堆平行「PASS」叙事，回到可测外环（人情帖 / 首单）。
5. **Boundary exception：** 仅当成功规格可从本轮产物本身判定（布尔文件存在、HTTP 写路径 sid、契约字段齐全）时，带内判定合法——那是边界任务，不是开放赚钱目标。
6. **L11：** 不新开 `PROGRESS-MIRAGE-GATE.md`；不抢 Kevin 回令。

## Pass rules（Agent 自检 · M1–M6）

| # | Check | PASS | FAIL |
|---|-------|------|------|
| M1 | Harness vs World Δ 分列 | RESULT 两栏都有 | 只有「本轮 PASS」 |
| M2 | Open-goal gate not self-score | 赚钱/人情进度不靠自评分关闭 | Agent 自标 OWNER-FAVOR / 首单 PASS |
| M3 | World Δ explicit even if 0 | 写「销量 Δ=0 · 人情未发」 | 省略负/零 Δ |
| M4 | In-band judge not used as sole gate | 开放目标引用外环证据 | 仅「分数卡自评绿」 |
| M5 | Accept-all smell checked | ≥3 轮无正 Δ 则 MIRAGE-RISK | 继续堆 SCORE PASS |
| M6 | No new *-GATE | 核心名 PROGRESS-MIRAGE；L11 | 新 GATE / 第二回令 |

## Anti-patterns

- 「今天又 PASS 了」而 Gumroad/人情 Δ 空白
- 用更强模型重读 RESULT.md 来「确认进步」
- 把目录 LIVE 数当 World Δ
- 把 EDIT-TRIGGERED 的 POST sid 当成首单进度
- 另开 `PROGRESS-MIRAGE-GATE.md`

## Complements

见 [OBSERVE-NOT-NARRATE.md](OBSERVE-NOT-NARRATE.md) · [EDIT-TRIGGERED.md](EDIT-TRIGGERED.md) · [SLICE-LOCK.md](SLICE-LOCK.md) · [JOB-CONTRACT.md](JOB-CONTRACT.md) · [ACTIVITY-BIAS-LOCK.md](ACTIVITY-BIAS-LOCK.md) · [progress-mirage-scorecard.html](progress-mirage-scorecard.html) · [chat-inline-clear.md](chat-inline-clear.md)。
