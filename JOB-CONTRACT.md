# JOB-CONTRACT · Agent 任务必须写成六栏契约（核心 · 非 *-GATE）

**One-liner（CN）：** 「Grow the company」是野心，不是任务。每个 Agent 任务开工前必须写清六栏：触发 · 可用信息 · 有界产出 · 独立验收测试 · 异常路由 · 具名主人；缺栏 = 不得静默升阶。验收测试写在动手前，且不得由同一 Agent 自批。

**English short:** Ambition is not a job. Every agent job needs six fields before it runs: trigger, allowed inputs, bounded output, independent acceptance test, exception route, named human owner. Missing a field = no silent raise. Write the acceptance test before the agent starts; the same agent may not self-pass it.

## Why（signals 2026-10-29 ~17:45 Asia/Shanghai）

| Signal | Point |
|--------|-------|
| [Nexius Labs · Five-Loop one-person AI company](https://dev.to/nexius_labs_d748e1551ced8/a-five-loop-operating-model-for-a-one-person-ai-company-5a91) | Agent jobs as contracts: trigger · inputs · bounded output · acceptance test · exception route · named owner；authority 同精度（可起草≠可发送） |
| [Governed Autopilot](https://sfeilden.substack.com/p/governed-autopilot-is-the-future) | 目标不是 autonomous business，而是 human-governed agentic execution；从**一个** governed loop 开始 |
| [SalarsNet · Automate normality](https://salars.net/ai/automate-normality) | 例外要有 owner + decision packet + 时限；只有警告+长对话 = 没把难事变容易 |
| X [@samuelpiatanesi](https://x.com/samuelpiatanesi/status/2115725022861901983) | Harvard 718 家：产出↑30% 但完工持平；修法=**验收测试写在 Agent 动手前** |
| X [@Al_Grigor](https://x.com/Al_Grigor/status/2115715269159256077) | Spec 先于代码：Users/Workflow/MVP/Out of scope/Agent 不可做的决定 |
| X [@Bagel8343](https://x.com/Bagel8343/status/2115668663256613106) | 加 Skill 前先问：结果是否经过**独立**验收测试？ |
| X [@evgheni_D](https://x.com/evgheni_D/status/2115731401651941647) | 委派者必须拥有结果，并在 Agent 开工前设好 escalation |
| Local same-day | money/cognition 循环常有 RESULT，但缺「验收测试先于动手」栏；目录 LIVE 有 HTTP 出处却仍不等于清闸 |

## Relation to existing cores

| Core | Job | This core adds |
|------|-----|----------------|
| [EXCEPTION-ONLY](EXCEPTION-ONLY.md) | Which decision classes leave Kevin queue (rung3+) | **Shape** of every job that may run at any rung — six fields, not just class |
| [OBSERVE-NOT-NARRATE](OBSERVE-NOT-NARRATE.md) | Claims need independent surviving provenance | Acceptance test is declared **before** run; provenance proves the test, not a post-hoc story |
| [ACCEPTANCE-GATE](ACCEPTANCE-GATE.md) | First-sale counts only buyer-acceptable + paid next hop | Buyer commercial unit ≠ agent-job contract fields |
| [CLEAR-COST](CLEAR-COST.md) / EXCEPTION-QUEUE | Cheap clear + packet for rung2 | Packet fills exception-route + owner fields; still needs the other four |

**Harder than EXCEPTION-ONLY alone：** EXCEPTION-ONLY 说「哪一类可升」；JOB-CONTRACT 说「升或不升，任务本身必须是六栏契约，否则连跑都不完整」。

**Harder than OBSERVE-NOT-NARRATE alone：** OBSERVE 管「主张有没有存活出处」；JOB-CONTRACT 管「开工前有没有写验收测试」——事后找出处补 RESULT ≠ 先写测试。

## Six fields（必填）

1. **Trigger** — 什么事件/时刻启动（cron、表单、用户一句、目录提交成功…）
2. **Allowed inputs** — 可用信息边界（哪些源、哪些禁止：主业宠物询盘、密钥、未授权账号…）
3. **Bounded output** — 允许做什么/产出什么；明确**禁止**的动作（发人情帖、花钱、代说「是」…）
4. **Acceptance test** — 独立、可复核的通过条件（HTTP/URL/commit/raw 路径；或 Kevin 绑定回令）；**写在动手前**
5. **Exception route** — 不确定/失败时去哪（packet → Kevin；降阶；暂停 routine；记 FAIL）
6. **Named owner** — 对人负责的名字（Kevin / 本店 Agent 日志责任仍归 Kevin）

Authority precision: draft ≠ send · prepare batch ≠ release funds · suggest price ≠ bind Kevin.

## Pass rules（Agent 自检 · J1–J6）

| # | Check | PASS | FAIL |
|---|-------|------|------|
| J1 | Six fields present before work | RESULT/契约表六栏齐全 | 只有感想或野心句 |
| J2 | Acceptance test pre-declared | 动手前写清通过条件 | 事后补「我觉得 OK」 |
| J3 | Acceptance ≠ self-grade | 测试可由独立出处/主人复核 | 同一 Agent 自标 PASS 不可逆项 |
| J4 | Exception route named | 失败/不确定有路由 | 静默重试烧钱或空喊催批 |
| J5 | Bounded output respects NEVER_AUTO | 未越权发人情/花钱/代说是 | 越权或暗示可代办 |
| J6 | No new competing *-GATE | 强化契约，不另开门禁抢注意力 | 新 GATE / 第二回令（L11） |

## Shop living contracts（本店）

### Money loop（自主赚钱循环）
| Field | Value |
|-------|-------|
| Trigger | cron `0,30 9-22 * * *` Asia/Shanghai |
| Allowed inputs | 公开目录/工具页、hub、Gumroad 价、既往 RESULT；**禁止**主业宠物询盘当副业、密钥外泄 |
| Bounded output | 免费目录 LIVE、hub/Pages 镜像、Feishu 财富日志；**禁止**代发人情、花钱、改价未授权 |
| Acceptance test | LIVE 主张须有 URL + HTTP/原始 JSON 落盘；价/$0 可陈述；OWNER-FAVOR 不得自标 PASS |
| Exception route | 目录失败 → 记 FAIL 换下一站；需 Kevin → 唯一 chat-inline packet；花费 → 停等确认 |
| Named owner | Kevin（Agent 执行，Kevin 对人结果负责） |

### Cognition loop（认知挖掘与实践）
| Field | Value |
|-------|-------|
| Trigger | cron `15,45 9-22 * * *` Asia/Shanghai |
| Allowed inputs | 全网+X 高信号认知（创业/副业/Agent/学习决策）；**禁止**鸡汤、主业宠物情报 |
| Bounded output | ≤1 新核或强化旧核；实践须有文件/飞书；**禁止**只堆链接、新并列 GATE |
| Acceptance test | 新核须比旧核更硬（关系表写清）；实践有 hub commit / 本地目录 / lark-cli rev；聊天极短结果 |
| Exception route | 无更硬信号 → 「无新增」+强化；lark 失败 → 记卡点不弹 MCP 卡 |
| Named owner | Kevin |

## Anti-patterns

- 用「继续增长/再测渠道」当任务而无六栏
- 验收测试写在 RESULT 末尾当补丁
- 把 ACCEPTANCE-GATE（买家结果单位）与本核（Agent 任务契约）混为一谈
- 另开 `JOB-CONTRACT-GATE.md` 抢 L11 注意力
- 缺异常路由却无限重试目录/烧 token

## Complements（不替代 · 不发明并列 GATE）

见 [EXCEPTION-ONLY.md](EXCEPTION-ONLY.md) · [OBSERVE-NOT-NARRATE.md](OBSERVE-NOT-NARRATE.md) · [ACCEPTANCE-GATE.md](ACCEPTANCE-GATE.md) · [CLEAR-COST.md](CLEAR-COST.md) · [job-contract-scorecard.html](job-contract-scorecard.html) · [chat-inline-clear.md](chat-inline-clear.md)。
