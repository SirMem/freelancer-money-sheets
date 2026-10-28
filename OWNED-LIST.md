# OWNED-LIST gate · owned-list-nurture-v1 · 2026-10-28 ~15:54 Asia/Shanghai (UTC+8)
# Amended 2026-10-28 ~16:18 — Expense/Client free LIVE + send-lock (see PAYOUT-EMAIL-LOCK.md)

**Core:** Free-download count is vanity. The asset is a reachable list **segmented by which free SKU they took**, each segment mapped to **exactly one** paid offer (sku-pain-split). $0 buyers and paid buyers never share the same sequence.

**Send lock:** Until Gumroad ≥$100 net after fees **and** a completed payout, platform Workflows/Emails cannot send. Treat paste-ready sequences as **queued**; pre-unlock nurture = CSV export + offboard path. Full gate: [PAYOUT-EMAIL-LOCK.md](PAYOUT-EMAIL-LOCK.md).

## Gate (fail = do not celebrate downloads)

| Check | Pass if |
|-------|---------|
| G1 Segment tag exists per free LIVE SKU | `free_aging` / `free_expense` / `free_client` / `free_adhd` / `free_re` |
| G2 Each free segment maps to ≤1 paid CTA | Aging → Invoice; Expense → Expense; Client → Client; ADHD/RE → **none** (soft hub only) |
| G3 Sequence exists for every free→paid map | Aging→Invoice SEQUENCES Path A; Expense/Client → OFFBOARD Paths B/C |
| G4 Paid buyers excluded from free nurture | Tag `paid_*` or purchase suppresses free sequence |
| G5 Export path known | Gumroad customers exportable; list not trapped in one UI forever |
| G6 Send surface unlocked | Else G3 drafts stay queued — see PAYOUT-EMAIL-LOCK L1–L4 |

## Why this is harder than “have a freebie”

sku-pain-split locks **which paid** each free may feed. gap-question locks **what signal** means demand. This gate locks **what happens to the email after download**. Without it, free LIVE SKUs pile silent addresses while we keep polishing listings.

## Sources (brief)

- Gatedleads / Gumroad free vs gated: download email is the start; first emails decide buyer vs unsubscribe
- SendOwl free-order advice: $0 and paid are different people — segment or leak LTV
- LifeMathMoney Gumroad free products: free = taste + email asset, not a dead end
- X: “X discovers, email retains and sells” / owned audience + lead magnet + nurture stack (aakashkapil01 2026-10-16)
- Nightcore: free solves first problem → paid solves **next** problem; follow-up teaches before it asks
- Gumroad Help + PAYOUT-EMAIL-LOCK: capture ≠ send until $100 + payout

## Kevin shelf map (2026-10-28 ~16:18)

| Segment | Free LIVE | Feeds paid | Sequence |
|---------|-----------|------------|----------|
| `free_aging` | merlns $0+ | Invoice $6 | Path A — SEQUENCES / OFFBOARD |
| `free_expense` | tbkad $0+ | Expense $5 | Path B — OFFBOARD (queued on Gumroad) |
| `free_client` | kaaxfy $0+ | Client $5 | Path C — OFFBOARD (queued on Gumroad) |
| `free_adhd` | adhd-2027-planner-sample $0 | none (free-only ICP) | Soft: tip only, no money-tracker pitch |
| `free_re` | re-listing-copy-prompts $0 | none (free-only ICP) | Soft: tip only, no money-tracker pitch |

**Rule:** if a free SKU has no paid twin (ADHD/RE), do **not** invent a cross-ICP pitch to Invoice. That violates sku-pain-split.
