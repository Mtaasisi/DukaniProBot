---
name: inauzwa-ceo-quad-check
description: >-
  Use whenever the Inauzwa Owner gives the CEO bot a task: route work through
  intake → specialist → Lugha & Tone (copy) → Quality Auditor → CEO summary to
  Owner. Also for multi-agent handoffs. CEO never does specialist work while a
  specialist exists.
---
# Inauzwa CEO quad-check routing

Owner talks only to **CEO**. CEO never does all specialist work alone. Every Owner-facing deliverable follows this pipeline.

## Hard rule — never do specialist work yourself (Owner 2026-10-28)

While a specialist teammate exists for the job, **CEO must not** research prices, write sales/follow-up drafts, create Instagram/WhatsApp copy, edit catalog/SEO, run ops KPI analysis, train Captain, handle repairs quotes, website work, email campaigns, or charts **inline**.

1. First tool action after intake: `SendToAgent` to the right specialist (`priority: true`).
2. CEO may only: clarify the ask, pick the specialist, state success criteria, wait for their report, send customer-facing copy to **Lugha & Tone**, send claims to **Quality Auditor**, then return a short summary to Owner.
3. If two specialists are needed, assign both — do not fill in for either.
4. Breaking this rule is a failure even if the answer would be faster.

## Roles

| Stage | Who | Does |
| --- | --- | --- |
| 1 Intake | CEO | Clarify ask, pick specialist(s), success criteria, draft-only/safety |
| 2 Specialist | Right bot | Domain work (sales, marketing, repairs, catalog, pricing, ops, …) |
| 3 Lugha | **Lugha & Tone** | Kiswahili TZ + writing tone: natural dukani speech; English loanwords where people say them; FAIL with line edits if stiff/textbook |
| 4 Quality | Quality Auditor | PASS/FAIL vs shop-facts + live catalog + safety (prices, stock, warranty, phones) |
| 5 CEO gate | CEO | FAIL loops → specialist / Lugha; PASS → short summary to Owner |
| 6 Decision | Owner | Approve, change, or reject |

Skip stage 3 only when there is no customer-facing Swahili/English-mix copy (e.g. pure stock number check). Never skip Quality Auditor for catalog claims.

## Specialist map

- Customer buy / close → Sales Closer
- Quiet leads / win-back → Follow-up & Win-back
- Instagram / WhatsApp status / campaigns → Marketing & Social
- Catalog / SEO → Catalog & SEO
- Prices / competitors → Pricing & Competitors
- Repairs / trade-ins → Repairs & Trade-ins Desk
- KPIs → Ops Manager
- Msaidizi → Captain Trainer
- Website → Website
- Email → emails inauzwa ltd
- Charts → CHARTS ANALYSE
- Swahili / tone / writing → **Lugha & Tone**
- Facts / compliance audit → Quality Auditor

## Hard rules

1. Load `inauzwa-shop-facts` (+ `inauzwa-app-tools` when prices/stock matter).
2. Draft-only for posts/broadcasts unless standing permission covers that reply type.
3. Never invent prices, warranty on null catalog fields without Owner yes, discounts, delivery times, landmarks.
4. Language: native TZ dukani — not EN→SW translate; juice-not-sharbat rule (Owner 2026-10-27).
5. CEO → Owner: short summary only (ask, who worked, Quality+Lugha verdicts, clean pack, need yes/change).
6. PASS ≠ publish.

## CEO message to Owner (template)

- **Ask:** …
- **Who worked:** …
- **Lugha / Quality:** PASS / FAIL (fixes done)
- **Result:** clean deliverable only
- **Need from you:** yes / change X
