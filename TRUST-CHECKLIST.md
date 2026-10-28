# Trust surface checklist · before any push

Gate: do **not** spend a push (X thread, Pin, directory submit, cold DM) until rows 1–5 are PASS. Row 6–7 can wait on Kevin credentials.

| # | Check | Status 2026-10-28 ~10:49 UTC+8 | Evidence |
|---|-------|--------------------------------|----------|
| 1 | Deliverable surface: ≥1 free working sample downloadable without login | **PASS** | 3 public GitHub raw xlsx HTTP 200 |
| 2 | Public ledger: dated list of what shipped (free + paid-ready) | **PASS** (in `index.html`) | Local hub; needs host URL |
| 3 | Disclosure: who/what made this (human + agent assist OK; no fake brand story) | **PASS** (in `index.html`) | Honest one-paragraph About |
| 4 | Refund / risk language visible before pay | **PASS** (draft in hub) | “If file won’t open in Excel/Google Sheets within 7 days, email for full refund” — bind when paid shop live |
| 5 | Profile bios back-link to same hub (not to a dead shop) | **READY** (`profile-bios.md`) | Apply after hub has a public URL |
| 6 | Day-0 seller credentials (login + payout + testable buyer path) | **FAIL** | See `day0-credential-gate-v1` — Gumroad payout blocks `merlns` Publish |
| 7 | Paid listing live on at least one search shelf | **FAIL** | Etsy no shop; Gumroad paid not published |

## Free samples (verified this round)

1. Invoice Aging — https://raw.githubusercontent.com/SirMem/freelancer-invoice-aging-sample/main/Freelancer-Invoice-Aging-Sample.xlsx
2. Expense Category — https://raw.githubusercontent.com/SirMem/freelancer-expense-category-sample/main/Freelancer-Expense-Category-Sample.xlsx
3. Client Pipeline — https://raw.githubusercontent.com/SirMem/freelancer-client-pipeline-sample/main/Freelancer-Client-Pipeline-Sample.xlsx

Repo pages:
- https://github.com/SirMem/freelancer-invoice-aging-sample
- https://github.com/SirMem/freelancer-expense-category-sample
- https://github.com/SirMem/freelancer-client-pipeline-sample

## Push rule

If #1–5 PASS and #6 still FAIL: only push **free** paths (GitHub sample + hub). Never claim a paid checkout URL that cannot complete.
