---
name: inauzwa-instagram
description: >-
  Use when planning or drafting Instagram (or Facebook/WhatsApp status) content
  for Inauzwa Limited: wire the ig-* pack to shop facts, live catalog prices,
  Swahili tone, and owner approval. Use for Reels, captions, carousels, stories,
  weekly plans, profile audits, viral research, comments, replies, or DMs for
  @inauzwa.
---
# Inauzwa Instagram bridge

Load this before any `ig-*` skill when the account is Inauzwa. It sits on top of the Instagram pack and the shop rules. Never invent prices, stock, warranty, delivery, installments, or discounts.

## Always load first

1. `inauzwa-shop-facts` — hours, phones, warranty, delivery, installments, payments, what is still unconfirmed.
2. `inauzwa-app-tools` — live price and stock only from the app. Skip out-of-stock and TZS 0/1 placeholders.
3. Then the matching `ig-*` skill (reel, caption, carousel, story, plan, viral, profile, human, comment, reply, dm, repurpose, audit).

## Account and voice

- Instagram: `@inauzwa`. Facebook page: Mtaasisii.
- Voice file: `/home/box/.claude/instagram/voice.md` (same as `~/.claude/instagram/voice.md`). Read it before writing spoken scripts.
- Tone: casual Swahili with English product names (iPhone, MacBook, GB). Short lines people can say on camera.
- Store stills still use the Inauzwa Product template (red tag, large price, short Swahili pitch, product photo, Quality Loyalty Trust). Reels/carousels from `ig-*` are scripts and slide copy; they do not replace that template for product grid posts.

## Hard rules (override the ig pack where they conflict)

- **Draft only.** Never publish, schedule, broadcast, or send a DM/comment as the shop until the owner says yes.
- **Price in the first 125 characters** of every product caption, with a DM CTA. Cap hashtags at five; prefer `#Inauzwa` / `#InauzwaTZ` and specific product terms.
- **Live catalog only.** Name, price (TZS), condition, warranty from the app. No fabricated metrics, sales numbers, or fake customer stories. Use `{{your number}}` or ask the owner when a proof number is missing.
- **Phones to customers:** only `0712378850` and `0769601663`. Landmarks still hand off to staff.
- **Payments:** Lipa Namba `16047799` and CRDB `10121592237` (INAUZWA ELECTRONICS) only when the draft needs them; never invent other methods.
- **Standing permission** covers routine catalog replies in customer chat, not Instagram publishes or cold outreach.

## Which ig skill to run

| Ask | Run |
| --- | --- |
| Week calendar / what to post | `ig-plan` then product picks from app |
| Reel / hook / voiceover | `ig-reel` then `ig-human` then `ig-caption` |
| Caption only | `ig-caption` (Job A if reel hooks; Job B if photo/carousel) |
| Carousel / slides | `ig-carousel` then `ig-human` + `ig-caption` |
| Stories / WA status | `ig-story` + posting-status daily plan |
| Niche research / swipe file | `ig-viral` → write `~/.claude/instagram/swipe.md` |
| Profile bio/grid score | `ig-profile` once, then rare |
| Comments on others | `ig-comment` |
| Replies under own posts | `ig-reply` |
| Instagram DMs / keyword | `ig-dm` — hand hot buyers to Sales Closer; quiet leads to Follow-up |
| Long video → week of posts | `ig-repurpose` |
| What worked last month | `ig-audit` |
| De-slop any draft | `ig-human` before showing the owner |

## Output to the owner

Show a copy-ready block (script / caption / slides), the tool receipt (`REEL READY`, `CAPTION READY`, etc.), and the product ids/prices used. End with: reply **yes** to approve posting, or say what to change. Nothing goes live on a silent turn.

## Out of scope

Captain/Msaidizi, repairs board, pricing changes, Ops KPI reports, Hermes Telegram alerts, and Website deploys do not use this bridge.
