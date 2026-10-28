# PAYOUT-EMAIL-LOCK gate · payout-email-lock-v1 · 2026-10-28 ~16:18 Asia/Shanghai (UTC+8)

**Core:** Until Gumroad shows **≥$100 net sales after fees** *and* a completed payout (or admin-verified bypass that Kevin does not have), platform Emails / Workflows / Broadcasts are **locked**. Free downloads still capture addresses, but **writing a Workflow is not nurture**. Pre-unlock asset work = CSV export + offline/outboard send path, or press for a first paid sale that unlocks the gate.

Complements [OWNED-LIST](../owned-list-nurture-v1/OWNED-LIST-GATE.md): that gate says *what* to send per segment; this gate says *whether Gumroad can send at all*.

## Gate (fail = do not claim “nurture live”)

| Check | Pass if |
|-------|---------|
| L1 Sales floor | Gumroad Analytics / balance shows ≥$100 **net after fees** (gross downloads of $0 SKUs do **not** count) |
| L2 Payout | At least one **completed** payout, OR account is Gumroad-verified (admin) — Kevin: assume **not** verified |
| L3 Send surface | Emails / Workflows UI accepts compose without the $100/payout lock banner |
| L4 Until L1∧L2∧L3 | Treat Workflow drafts as **queued**, not live; nurture = **export CSV** → segment → external mail / manual 1:1 |
| L5 No vanity | Do not celebrate free-download count as “list working” while L4 holds |

## Why harder than owned-list alone

owned-list-nurture-v1 left SEQUENCES.md paste-ready for Gumroad Workflow. Help Center + X (THforRus 2026-10-18; Gumroad docs) make clear: **cannot send** until $100 after fees **and** payout. A July 2026 code change lets *verified* creators skip completed payout but **keeps** the $100 sales floor — irrelevant until first paid revenue. Money loop ~16:05 still listed “paste Workflow” as next step — that step is **blocked** until L1–L3.

## Sources

- [Gumroad Workflows help](https://gumroad.com/help/article/131-using-workflows-to-send-automated-updates) — explicit $100 + payout lock
- [Gumroad Audience / Email updates](https://gumroad.com/help/article/170-audience) — same lock on newsletter
- antiwork/gumroad `dc42464` (2026-07) — verified bypass of payout only; $100 sales unchanged
- InsightRaider Gumroad email list 2026 — free product captures email; send gate still applies
- X @THforRus 2026-10-18 — documents the same condition in the wild

## Kevin shelf (2026-10-28 ~16:18)

| Segment | Free LIVE | Feeds paid | Pre-unlock nurture |
|---------|-----------|------------|-------------------|
| `free_aging` | merlns | Invoice $6 | CSV + OFFBOARD Path A |
| `free_expense` | tbkad | Expense $5 | CSV + OFFBOARD Path B |
| `free_client` | kaaxfy | Client $5 | CSV + OFFBOARD Path C |
| `free_adhd` / `free_re` | LIVE | none | soft tip only; no money-tracker pitch |

**Rule:** Until L3, do **not** mark PROGRESS “Workflow pasted” as distribution success. Unlock metric = first paid sale(s) toward $100 net, then first payout.
