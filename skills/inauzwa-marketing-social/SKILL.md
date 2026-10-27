---
name: inauzwa-marketing-social
description: >-
  Use to write marketing content for WhatsApp status/broadcasts, Instagram,
  Facebook, TikTok, storefront copy and campaigns for Inauzwa Limited. Drafts
  for owner approval. Loads inauzwa-instagram when using the ig-* pack. Native
  Tanzania Swahili only (never translate English to Swahili).
---
# Marketing & Social

Load `inauzwa-shop-facts` and `inauzwa-app-tools` first.

For Instagram Reels, captions, carousels, stories, weekly plans, viral research, profile audits, comments, replies, or DMs, also load **`inauzwa-instagram`** then the matching `ig-*` skill. That bridge enforces live prices, **Kiswahili cha Tanzania cha dukani** (never EN→SW translate), price-in-first-125-chars, and draft-only. Always read `/home/box/.claude/instagram/voice.md` before spoken scripts or captions.

## Hard rules
- Draft only; never publish, broadcast or run ads without a clear yes.
- Prices and stock from live catalog only; never advertise out-of-stock items.
- Never invent warranty, installment, delivery or discount claims.
- **Tone:** Andika Kiswahili cha Tanzania kuanzia mwanzo (Dar/Arusha dukani). Usifikiri Kiingereza kisha utafsiri. Majina ya bidhaa (iPhone, MacBook, GB, trade-in, warranty) yanabaki Kiingereza; sentensi ni Kiswahili. Prefer sauti halisi kuliko hookscore ya Kiingereza.
- Hashtag `#Inauzwa` / `#InauzwaTZ` when useful (max five).
- Product grid stills: Inauzwa Product template (red tag, large price, short Swahili pitch, product photo, Quality Loyalty Trust).
- Voice profile: `/home/box/.claude/instagram/voice.md` (gold sample + bad examples ndani).

## Playbook
1. Pull in-stock products with photos from the app.
2. For a week plan → `ig-plan`. For one Reel → `ig-reel` → `ig-human` → `ig-caption`. For carousels/stories → `ig-carousel` / `ig-story`.
3. Captions: price + DM CTA in the first 125 characters; body in native TZ Swahili.
4. Mark drafts for owner approval. Nothing posts on a silent turn.
