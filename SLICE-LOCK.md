# SLICE-LOCK · 切片基线锁死总均分（核心 · 非 *-GATE）

**One-liner（CN）：** 总均分/总 RESULT PASS 会掩盖单片回归；Agent 循环的验收必须按切片基线锁死（per-case / per-field），保留完整评分产物并做差分，不能只报 mean。任务成功 ≠ 脚手架健康（TraceTrial：约 31% 跑通任务却至少一项 harness 失败）。

**English short:** Mean / aggregate RESULT PASS masks slice regressions. Lock acceptance to per-slice baselines; keep full grade artifacts and compare case-by-case. Task success ≠ harness health.

## Why（signals 2026-10-29 ~18:22 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [Layer-Isolated Evaluation · arXiv 2606.11686](https://arxiv.org/html/2606.11686) | Aggregate masks small drops (−1.7 to −5.9pp) while matching slice craters (−25 to −91pp)；主张 **no-LLM regression-locked harness** — 按切片锁基线 |
| [TraceTrial-Bench · arXiv 2610.32285](https://arxiv.org/html/2610.32285) | **31.1%** task success despite failing ≥1 harness criterion；**harness ≠ outcome** |
| [Google Agents CLI · hill-climbing agent quality](https://developers.googleblog.com/hill-climbing-agent-quality-with-agents-cli-evaluation/)（2026-10-28） | Snapshot **result files not scores**；treat summary metrics with suspicion；per-case compare（chef-prompt 4.0→2.75；model swap 同 mean 不同 case map） |
| X [@DeepWater_SI](https://x.com/DeepWater_SI/status/2115731365316452525) | 同一 Google eval 走读：mean 4.0→2.75，per-case 表分叉 |
| Local same-day money/cognition | RESULT 常一个总 PASS，同时 OWNER-FAVOR FAIL + 目录 LIVE — **聚合绿掩盖开着的切片 FAIL** |

## Relation to existing cores

| Core | Job | This core adds |
|------|-----|----------------|
| [JOB-CONTRACT](JOB-CONTRACT.md) | Six fields + acceptance **before** run | Acceptance must be **decomposed** (per-slice baseline lock), not one mean PASS |
| [OBSERVE-NOT-NARRATE](OBSERVE-NOT-NARRATE.md) | Claims need independent surviving provenance | Even a proven “mean PASS” can hide a localized FAIL — need **per-slice** evidence |
| [EXCEPTION-ONLY](EXCEPTION-ONLY.md) / EXCEPTION-QUEUE | Which classes leave Kevin queue; packet for rung2 | Not a new human gate; scoring discipline for agent RESULT |
| [ACCEPTANCE-GATE](ACCEPTANCE-GATE.md) | Buyer-acceptable unit + paid next hop | Buyer commercial unit ≠ agent RESULT slice table |

**Harder than JOB-CONTRACT alone：** JOB 说「写验收」；SLICE-LOCK 说「验收必须按切片基线，不能用总均分糊过去」。

**Harder than OBSERVE-NOT-NARRATE alone：** OBSERVE 管「主张有没有存活出处」；SLICE-LOCK 管「就算出处证明了 mean PASS，也可能掩盖局部 FAIL」。

**≠ new *-GATE：** 本核是 RESULT 计分纪律，不是第二道 Kevin 批准类（L11）。

## Rules

1. **Per-slice baselines：** 每个可独立失败的验收项（LIVE URL+HTTP、hub commit、Feishu rev、价/$0、OWNER-FAVOR、无新 GATE…）各自有基线与判定，不得折叠成一个绿勾。
2. **Keep full grade artifacts：** 保留完整评分产物（表 / JSON / HTML 分数卡），不要只存 mean 或「PASS」。
3. **Case-by-case diff：** 相对上一基线做差分；单片回归 = FAIL 该片，即使总均分仍绿。
4. **Task success ≠ harness health：** 跑通任务 / 目录 LIVE ≠ 脚手架（OWNER-FAVOR / L11 / NEVER_AUTO）健康。
5. **Mean is suspicious：** 摘要指标仅作索引；判定以切片表为准（cite Google Agents CLI）。
6. **Open FAIL stays FAIL：** OWNER-FAVOR 等开闸切片在 Kevin 动作前必须显式 FAIL，禁止被总 PASS 盖住。

## Pass rules（Agent 自检 · S1–S6）

| # | Check | PASS | FAIL |
|---|-------|------|------|
| S1 | RESULT has per-slice table | 表含基线/证据/判定 | 只有一句「本轮 PASS」 |
| S2 | Full grade artifact kept | 分数卡 HTML 或等价表落盘/上 hub | 只报 mean 数字 |
| S3 | Open gate slices named FAIL | OWNER-FAVOR 等显式 FAIL | 总绿掩盖开闸 FAIL |
| S4 | Task ≠ harness conflated | LIVE/任务成功与脚手架分列 | 「都做好了」混为一谈 |
| S5 | Diff vs baseline when prior exists | 单片回归点名 | 只比总均分 |
| S6 | No new competing *-GATE | 强化计分纪律；L11 守住 | 新 GATE / 第二回令 |

## Anti-patterns

- RESULT 末尾一个 SCORE: PASS 而无切片表
- 用「平均分更高」掩盖 chef-prompt 类单案崩盘
- 目录 LIVE PASS → 暗示 OWNER-FAVOR / CLEAR-COST 也过了
- 另开 `SLICE-LOCK-GATE.md` 抢 L11 注意力
- 扔掉完整评分产物只留摘要

## Complements（不替代 · 不发明并列 GATE）

见 [JOB-CONTRACT.md](JOB-CONTRACT.md) · [OBSERVE-NOT-NARRATE.md](OBSERVE-NOT-NARRATE.md) · [EXCEPTION-ONLY.md](EXCEPTION-ONLY.md) · [ACCEPTANCE-GATE.md](ACCEPTANCE-GATE.md) · [CLEAR-COST.md](CLEAR-COST.md) · [slice-lock-scorecard.html](slice-lock-scorecard.html) · [chat-inline-clear.md](chat-inline-clear.md)。

## Hook · EDIT-TRIGGERED（2026-10-29 ~18:51）

切片表里必须能单列 **触发切片**：目标 PASS ≠ 触发 PASS。见 [EDIT-TRIGGERED.md](EDIT-TRIGGERED.md) · [edit-triggered-scorecard.html](edit-triggered-scorecard.html)。
