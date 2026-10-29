# EDIT-TRIGGERED · 改动必须被执行轨迹证明触发（核心 · 非 *-GATE）

**One-liner（CN）：** 目标任务变好 + 保护任务不回退，仍不够。接受一次 harness / 流程改动前，还必须有执行证据证明**预定改动路径真的被触发**（组件调用 / 模型输入含新字段 / API 写路径响应 / 相关代码路径）。缺触发证明 = 局部胜利可能是巧合或化妆；候选不得升为正本。

**English short:** Target↑ + protected stay-green is not enough. Accept a harness/process edit only when execution evidence also proves the intended edit path was actually triggered (component invocation, new fields in model input, write-API response, relevant code path). No trigger proof → local win may be coincidence/cosmetic; candidate stays unaccepted.

## Why（signals 2026-10-29 ~18:51 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [Trace-to-Architecture · arXiv 2610.16725](https://arxiv.org/html/2610.16725) | Acceptance requires **all three**: target-task improvement · regression protection · **edit triggering**（execution records confirm the edit was actually triggered） |
| T2A Appendix E.3 (life-span R5) | Target+protected scored 100,但新 blocking rule **从未触发** → 整配置保留候选、**不接受**；后轮才以新计划验收 |
| [Google Agents CLI · hill-climbing](https://developers.googleblog.com/hill-climbing-agent-quality-with-agents-cli-evaluation/)（2026-10-28） | Per-case compare / snapshot result files — 同 mean 不同 case map；改动是否打中目标案需证据 |
| X [@greg_radzio](https://x.com/greg_radzio/status/2108308545439412326) | trajectory.json → grader extracts evidence → metric scores one property — 触发证据在轨迹，不在摘要句 |
| Local same-day money | 目录「LIVE」若只有 GET 页 200，而无 POST/submit 原始响应，则**未证明写路径被触发**（化妆 LIVE 风险） |

## Relation to existing cores

| Core | Job | This core adds |
|------|-----|----------------|
| [JOB-CONTRACT](JOB-CONTRACT.md) | Six fields + acceptance **before** run | Acceptance must include an **edit-trigger check** when the job claims a change/fix/LIVE-write |
| [SLICE-LOCK](SLICE-LOCK.md) | Per-slice baselines; mean masks regressions | Trigger-proof is its **own slice**; target PASS ≠ trigger PASS |
| [OBSERVE-NOT-NARRATE](OBSERVE-NOT-NARRATE.md) | Claims need independent surviving provenance | Provenance must show the **intervened path fired**, not only a downstream symptom (e.g. GET after POST) |
| [EXCEPTION-ONLY](EXCEPTION-ONLY.md) | Which classes leave Kevin queue | Not a new human gate; validation discipline for agent-accepted edits |

**Harder than JOB-CONTRACT alone：** JOB 说「写验收」；EDIT-TRIGGERED 说「验收必须含触发证明，不能只测目标结果」。

**Harder than OBSERVE-NOT-NARRATE alone：** OBSERVE 说「有存活出处」；EDIT-TRIGGERED 说「出处必须证明**预定改动**被触发，不能用副作用冒充」。

**Harder than SLICE-LOCK alone：** SLICE-LOCK 说「按切片计分」；EDIT-TRIGGERED 钉死其中必有的一类切片——**触发切片**。

**≠ new *-GATE：** 本核是改动验收纪律，不是第二道 Kevin 批准类（L11）。

## Three conditions（缺一不可）

1. **Target improvement** — 预定目标任务/指标按计划变好（目录 LIVE、分数卡上线、Feishu rev…）
2. **Regression protection** — 保护项保持成功（价不变、$0、OWNER-FAVOR 仍显式 FAIL、无新 GATE…）
3. **Edit triggering** — 执行记录证明改动路径被进入：POST body / sid / 组件调用日志 / 模型输入含新字段 / 相关 code path

Until all three hold, previous accepted harness/process stays canonical; candidate may be retained for further revision but is **not accepted**.

## Shop rules（本店）

1. **Directory LIVE：** 必须保留 **write-path** 证据（POST status + response JSON / sid），不得仅用 GET 页 200 自称 LIVE。
2. **Hub / cognition edit：** 声称「强化了 X」时，RESULT 须指出被改文件 + commit SHA（触发=diff 进入主线），不能只写「已思考」。
3. **Scorecard / Pages：** 新分数卡上线 = target；`git show`/`Pages HTTP 200` = 触发；开着的 OWNER-FAVOR FAIL = 保护项保持。
4. **Untriggered ≠ failed：** 若规则预定可触发但本轮无机会触发，记 **not triggered**（候选/待验），**不得**记 PASS 该触发切片。
5. **Cosmetic win FAIL：** 目标变好但触发切片缺失 → 整轮改动 **不接受**（可记候选）。

## Pass rules（Agent 自检 · T1–T6）

| # | Check | PASS | FAIL |
|---|-------|------|------|
| T1 | Three conditions named before/with RESULT | 目标/保护/触发三栏齐全 | 只有「做好了」 |
| T2 | Trigger evidence is path-specific | POST/sid/调用日志/含新字段的输入 | 仅下游症状（GET 200） |
| T3 | Protected slices explicit | 价/$0/OWNER-FAVOR/L11 分列 | 被总绿吞掉 |
| T4 | Untriggered ≠ PASS | 无机会触发记 not-triggered | 未触发却标 PASS |
| T5 | Candidate vs accepted | 缺触发则不升正本 | 缺证也标 ACCEPTED |
| T6 | No new competing *-GATE | 核心名 EDIT-TRIGGERED；L11 | 新 GATE / 第二回令 |

## Anti-patterns

- 「页开了所以提交成功了」（缺 POST）
- 「分数更高所以改动生效了」（缺触发轨迹；T2A 倾斜面案例）
- 用 OBSERVE 的 URL 出处代替触发证明（出处≠触发）
- 另开 `EDIT-TRIGGERED-GATE.md` 抢 L11
- 把 not-triggered 记成 PASS

## Complements（不替代 · 不发明并列 GATE）

见 [JOB-CONTRACT.md](JOB-CONTRACT.md) · [SLICE-LOCK.md](SLICE-LOCK.md) · [OBSERVE-NOT-NARRATE.md](OBSERVE-NOT-NARRATE.md) · [EXCEPTION-ONLY.md](EXCEPTION-ONLY.md) · [edit-triggered-scorecard.html](edit-triggered-scorecard.html) · [chat-inline-clear.md](chat-inline-clear.md)。
