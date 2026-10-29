# EXCEPTION-ONLY · 决策类自治阶梯（核心 · 非 *-GATE）

**One-liner（CN）：** 自动化把约束挪到人签字；正确解法不是催人更快点批/再开并列闸门，而是把可逆·低爆破半径决策升到「事后抽查/仅异常」（rung3+），只把不可逆人情单元（OWNER-FAVOR）留在事前批准（rung2）；已有一条未清 Kevin 闸时，禁止再开新批准类。

**English short:** Constraint moves to human sign-off after agents speed execution; "approve faster" / more competing gates = wrong fix. Raise reversible/low-blast agent work to review-after/exception-only; keep only irreversible owner-favor at approve-before. While one Kevin gate is open, do not open another.

## REVIEW ≠ RATIFY（reinforce 2026-10-29 ~16:22 Asia/Shanghai）

**HITL 不是二元开关。** 每个动作只有三种决策权位置：

| Mode (EN) | 本店 rung | 人在哪儿 | 何时用 |
|-----------|-----------|----------|--------|
| Autonomous | 4 | 不在关键路径（聚合抽查） | 可逆 · 低爆 · 高可观测 · 高频 |
| Review-after / exception-only | 3 | **事后**审轨迹（可回滚） | 可逆 · 可观测 · 时间敏感 |
| Approve-before | 2 | **事前**批准 | 不可逆 · 高爆 · 或花费/人情 |

**REVIEW ≠ RATIFY：** 审阅权可下放（含 Agent 自检 / 分数卡），因为审阅本身可逆；**批准不可逆承诺（ratify）** 必须是具名主人（Kevin）——本店 = OWNER-FAVOR / Spend。把「审过分数卡」当成「Kevin 已批准人情帖」= FAIL。

**Dial / 迁移：** 新动作类可先放 rung2；证据与可观测性够了再升到 rung3/4。冻结一切在 approve-before = 自动化剧场（橡皮图章）。本店目录/hub/Feishu 已升阶；人情与花费永不静默升阶。

### Reinforce signals（~16:22）

| Signal | Point |
|--------|-------|
| [AdvantageWorks · 3 decision-rights](https://advantageworks.com/posts/ai-agent-governance-when-to-let-agents-act-ask-or-be-reviewed) | Autonomous / Approve-before / Review-after；按可逆·爆破·合规·可观测·频率落位；非按模型能力 |
| [Reversibility Partition · Zenodo](https://doi.org/10.5281/zenodo.19661592) | Review authority 可下放；Ratification of irreversible 必须具名主人 |
| [Makmel · HITL = latency budget](https://makmel.info/blog/human-in-the-loop-latency-budget) | 人注意力有硬顶；重复批准 = 未写成政策；可逆用事后审 |
| X [@Dejvyq](https://x.com/Dejvyq/status/2112489156022816853) | Reversibility is the only real prerequisite for autonomy |
| X [@chriscouch](https://x.com/chriscouch/status/2112608737533825060) | Reversibility beats accuracy (Autonomy Tax) |
| Local same-day money | submitby / CurlShip / DevElif / Zearches LIVE 而 OWNER-FAVOR 仍 FAIL → 出站 = rung3+ / **0 CLEAR-COST** |

## Why（signals 2026-10-29 ~15:49 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [superkind · approval bottleneck](https://superkind.ai/blog/approval-bottleneck) | Approval bottleneck; graduated autonomy ladder; bottleneck breaks rung2→rung3; rubber-stamp trap |
| [agentexperience · approval is a workflow](https://agentexperience.tech/insights/approval-is-a-workflow/) | Anthropic ~93% Claude Code permission prompts approved → attention fatigue; Oversight Has a Capacity |
| X [@0xdaba](https://x.com/0xdaba/status/2115665088606777536) | Approvals piling → rubber stamp; gate only irreversible + attach evidence |
| X [@organ_app](https://x.com/organ_app/status/2115705856667037919) | Ask must be cheap or rubber-stamp; auto-allow boring; irreversible waits |
| Local same-day | Money loops keep shipping CurlShip/DevElif LIVE while OWNER-FAVOR FAIL; CLEAR-COST/TOKEN-LATENCY/REPLY-BIND stack still floods Kevin with gate docs every cycle |

## Complements（不替代 · 不发明并列 GATE）

| Core | Job |
|------|-----|
| [ACTIVITY-BIAS-LOCK](ACTIVITY-BIAS-LOCK.md) | What does **not** count as first-sale progress while B=FAIL |
| [CLEAR-COST](CLEAR-COST.md) / [TOKEN-LATENCY](TOKEN-LATENCY.md) | Lower cost of the **one** remaining Kevin clear |
| [GATE-IN-CHANNEL](GATE-IN-CHANNEL.md) / [REPLY-BIND](REPLY-BIND.md) | That clear lives in chat; one paste ↔ one reply |
| [OWNER-FAVOR-GATE](OWNER-FAVOR-GATE.md) | Names the irreversible warm unit that stays at rung2 |
| **This core** | Classifies **which decision classes** may leave Kevin's queue (rung3+) vs stay approve-before |

EXCEPTION-ONLY answers *which classes leave the queue*; CLEAR-COST lowers cost of the one that stays.

## Autonomy ladder · THIS shop

| Decision class | Reversibility | Blast | Target rung | Rule |
|----------------|---------------|-------|-------------|------|
| Directory / awesome / CurlShip LIVE | High | Low | 3–4 (agent alone) | Do while B=FAIL only as SECONDARY honesty; never as clear progress |
| Hub scorecard / Pages mirror | High | Low | 4 | Agent alone |
| Feishu cognition/wealth log | High | Low | 4 | Agent alone via lark-cli |
| WeChat Moments / classmate favor (OWNER-FAVOR) | Low (trust burn) | High (first-sale path) | 2 approve-before | ONE open clear only; chat-inline |
| Spend / Etsy fee / paid boost | Low | High | 2 | Always Kevin confirm |
| New competing GATE / second reply token while B=FAIL | n/a | Attention | **FORBIDDEN** | L11 FAIL |

**Rung legend (shop-local):** 2 = approve-before · 3 = review-after / exception-only · 4 = agent alone (log only).

## Money-loop outbound map（应用 · 0 CLEAR-COST）

同日已出站类一律 **rung 3–4 · Waiting on Kevin = No · CLEAR-COST 分 = 0**。RESULT / Feishu 不得把它们记成清闸进度。

| Outbound class (2026-10-29) | Status | Mode | CLEAR-COST pts |
|-----------------------------|--------|------|----------------|
| submitby.ai free-badge | LIVE | 4 Autonomous | **0** |
| CurlShip free→dofollow | LIVE | 4 | **0** |
| DevElif Finance & Fintech | LIVE | 4 | **0** |
| Zearches Software & SaaS | LIVE | 4 | **0** |
| Canopy Launch | LIVE | 4 | **0** |
| Share Your Startup | QUEUED | 3 Review-after | **0** |
| Launching Next / Ignlab | PENDING | 3 | **0** |
| awesome-list PRs | OPEN/MERGED | 3–4 secondary | **0** |
| X / paid boost / Etsy fee | — | 2 Approve-before | n/a（未发起） |
| WeChat Moments OWNER-FAVOR | FAIL | 2 | **唯一** clear 目标 |

## EXCEPTION-QUEUE（reinforce 2026-10-29 ~16:49 Asia/Shanghai）

**异常必须是一等公民工作项，不是「请批准」口头禅。** 留在 rung2（approve-before）的动作，Agent 只能交付一份 **exception packet**；禁止空喊催批、禁止用分数卡/货架 LIVE 冒充清闸。

| Packet field | 必须有 | 本店 OWNER-FAVOR 例 |
|--------------|--------|---------------------|
| Why escalated | 为何不能升 rung3+ | 朋友圈人情不可逆 · 信任燃烧 |
| Evidence | 已备好的可核对材料 | 故事脚注全文（chat-inline 粘贴块） |
| Proposed action | 具体可执行一步 | 复制 → 发朋友圈/同学群 |
| Decision question | 一个二元/一行回令 | 发完回绑定令牌 |
| Owner + deadline feel | 谁批 · 不堆第二闸 | Kevin · 唯一开闸；L11 禁并列 |

**SAY-YES LOCK：** Agent 可备订单/出站/草稿/日志；**永远不代「说是」**（不代发人情、不代花、不代批准）。「说是」= ratify = Kevin。

**Bare ask = FAIL：** 「请更快批」/「打开分数卡再决定」/ 无粘贴块的催促 — 全部 FAIL。packet 必须已把可逆准备工作做完，只留不可逆那一击。

### Reinforce signals（~16:49）

| Signal | Point |
|--------|-------|
| [Silpho · approval & exception boundaries](https://silpho.com/insights/supervised-ai-agents-approval-exceptions) | Exceptions = first-class state: reason · evidence · proposed action · owning decision · follow-up |
| [TechEMC · exception queue](https://techemc.com/blog/ai-workflow-exception-queue-what-to-review-before-approval/) | Narrow queue; AI prepares; human decides before consequence |
| [type.com · concrete proposal](https://type.com/blog/ai-agent-approval-workflows) | 「Should I continue?」难判；具体提案才可批 |
| [Accelate · HITL bottleneck](https://accelate.ai/blog/human-in-the-loop-approval-bottleneck) | 每动作同审 = 新瓶颈；按风险分层 |
| [Agentled · delegated approval](https://www.agentled.ai/en/blog/post/from-approval-queues-to-delegated-approval) | Draft-only → approve consequential → delegated within policy |
| X [@NullContex1s](https://x.com/NullContex1s/status/2113420371718529453) | Remove 80% boring workflow; keep 2-min approval for risky 20% |
| X [@M1k3meta](https://x.com/M1k3meta/status/2113359129741807869) | Bots run side business; never allowed to **say yes** |
| X [@0xForem](https://x.com/0xForem/status/2114032775674102137) | Structure autonomy by reversibility, not task size |
| Local | OWNER-FAVOR 仍 FAIL；chat-inline 已是 packet 雏形 — 本轮钉死字段与 SAY-YES LOCK |

## Pass rules（Agent 自检）

1. While OWNER-FAVOR **B=FAIL**, primary deliverable must **not** open a new competing approval class / new `*-GATE.md` / second reply token (**L11**).
2. Agent-openable work (directories, hub mirrors, Feishu logs) = rung3+ and scores **0 CLEAR-COST**.
3. Keep/refresh only the **single** [chat-inline-clear.md](chat-inline-clear.md); do not invent dual menus.
4. Spend / paid boost stays rung2 forever — never silent.
5. RESULT must score decision-class table ([exception-only-scorecard.html](exception-only-scorecard.html)): each class PASS if on target rung, FAIL if still waiting on Kevin when it should not.
6. **REVIEW≠RATIFY:** 分数卡/货架审阅 ≠ Kevin 批准人情；不得用「已开 scorecard」冒充 clear 完成。
7. **EXCEPTION-QUEUE:** 每个 rung2 开闸必须是完整 packet（why/evidence/proposed/decision/owner）；bare ask = FAIL；Agent 永不代「说是」。

## Anti-patterns

- 「催 Kevin 更快批」当主解
- 在一条未清闸旁再开 AUDIENCE-RENT / CONNECTOR / 新 GATE 抢注意力
- 把 CurlShip / submitby LIVE 记成清闸进度
- 把 EXCEPTION-ONLY 再拆成新 `*-GATE.md`
- 把 HITL 当成「有人/无人」二元（丢掉 Review-after）
- 把 Agent 自检审阅当成主人批准（REVIEW 冒充 RATIFY）
- 空喊「请批准」而无 exception packet 字段
- Agent 代发人情 / 代花 / 代说「是」（违反 SAY-YES LOCK）
