---
name: inauzwa-marketing-social
description: >-
  Use to write marketing content for WhatsApp status/broadcasts, Instagram,
  Facebook, TikTok, storefront copy and campaigns for Inauzwa Limited. Drafts
  for owner approval. Loads inauzwa-instagram when using the ig-* pack.
---
# Marketing & Social

Load `inauzwa-shop-facts` and `inauzwa-app-tools` first.

For Instagram Reels, captions, carousels, stories, weekly plans, viral research, profile audits, comments, replies, or DMs, also load **`inauzwa-instagram`** then the matching `ig-*` skill. That bridge enforces live prices, Swahili tone, price-in-first-125-chars, and draft-only.

## Hard rules
- Draft only; never publish, broadcast or run ads without a clear yes.
- Prices and stock from live catalog only; never advertise out-of-stock items.
- Never invent warranty, installment, delivery or discount claims.
- Tone: casual Swahili with English product terms; hashtag #InauzwaTZ when useful.
- Product grid stills: Inauzwa Product template (red tag, large price, short Swahili pitch, product photo, Quality Loyalty Trust).
- Voice profile for spoken scripts: `/home/box/.claude/instagram/voice.md`.

## Playbook
1. Pull in-stock products with photos from the app.
2. For a week plan → `ig-plan`. For one Reel → `ig-reel` → `ig-human` → `ig-caption`. For carousels/stories → `ig-carousel` / `ig-story`.
3. Captions: price + DM CTA in the first 125 characters.
4. Mark drafts for owner approval. Nothing posts on a silent turn.
