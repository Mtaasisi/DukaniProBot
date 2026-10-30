---
name: inauzwa-posting-status-2
description: >-
  Use to plan, draft, schedule and report on social posts and WhatsApp status from in-stock products for Inauzwa Limited. Schedule only after owner approval. Uses inauzwa-instagram + ig-plan/ig-story when building the week.
---
# Posting and status playbook

Goal: keep the shop's social accounts and WhatsApp status active with accurate, engaging, selling content, with the owner approving every public post. Use with inauzwa-app-tools and inauzwa-marketing-social.

## Hard rules
- Facts come from the app, never memory: price, stock, specs, condition and photo from search_products, get_product, get_inventory. Advertise only items shown in stock with a real photo. If a lookup fails, say so and skip the item; never guess.
- Never publish or schedule without the owner's yes in chat (the app also asks for confirmation). Drafts are free. A confirmation token works once.
- Never post: unconfirmed warranty, installment, trade-in, repair-price, delivery-fee, address or hours claims; discounts the owner has not approved; cost price; customer names, chats or screenshots with identifying details.
- Engagement never overrides truth: no fake scarcity, fake countdowns, fake giveaways or invented reviews.
- Never use accounts that belong to another business. Never read the owner's private inboxes (any personal/private inbox (never train/attach Captain)). One new idempotency_key per create call.

## Accounts (check list_social_accounts each run)
- Instagram @inauzwa: feed, reels, stories. Facebook page Mtaasisii: treat as unproven until a test post publishes. TikTok (TikTok handle Owner confirms — do not invent): video only. Only use accounts the owner named; check which accounts must never be touched.
- WhatsApp status: the app CAN post it with post_whatsapp_status (inbox id from get_my_context; image needs a direct public https media_url; always asks for owner confirmation; verify with list_whatsapp_status_posts). Never post without the owner's yes in chat.

## What the audience does (learn it from your own data, then record it here)
- Check how chats begin (often as a reply to a WhatsApp status) and what share ask the price. If many type only "Bei", the image had no price: put the price on the image.
- Check which price bands get the most asks and which categories sell the most units vs the most money; mix both in the plan.
- Check the hours when messages peak and post just before them.
- Review the best-performing reel/post and copy its structure (real product, price, specs, honest scarcity only when true). Memes and debate posts get comments but few buyers.

## Brand voice
Friendly mtaani Kiswahili (Tanzania). Call followers "boss". Prices as "Bei: [price]/=" or in the shop's own price style. "Share na rafiki" for shares. Humour is welcome, but a sales post stays specific.

## Engagement toolkit (rotate through the week)
1. **Hook line first** (first 8 words decide the scroll). Examples to adapt: "Budget ya [bei]? Hii ni yako 👀", "Laptop ya kazi kwa chini ya [bei]?", "boss, hii ndio simu ya wiki", "Zimebaki 2 tu" (only when true).
2. **Tag-a-friend and share prompts:** "Mtag rafiki anayetafuta laptop ya chuo", "Share na ndugu mwenye budget ya [bei]".
3. **Poll and question stickers in stories:** "Unapenda iPhone au Samsung?", "Budget yako ni ipi: chini ya [bei] au zaidi?", "Laptop ya kazi au gaming?" Then use the winning answer to choose next week's products.
4. **Price-guess game** (no prize needed): "Kisia bei ya hii, jibu kwenye comment, tunaanika jibu saa 12." Then reveal the real price in a story.
5. **Showcase reels, 15-30 seconds:** unbox, screen and battery check, speed test, "kabla na baada" for repairs and cleaned devices. Show the real item, price overlay at the end, CTA "Tuma BEI WhatsApp".
6. **Use-case posts:** "Inafaa kwa: kazi za ofisini, masomo, YouTube, Zoom". Speak to the buyer's life, not specs alone.
7. **Customer proof:** a happy-buyer photo or quote only with the customer's clear permission, no name or number.
8. **Behind the shop:** a repair in progress, stock arriving, the team, "tunafunga saa moja" closing-time stories.
9. **Tip posts:** battery care, how to check a used laptop, spot a fake charger. These get saves and build trust, then a soft link to a product.
10. **Replies as content:** answer a common question ("Je, mna warranty?") only once the owner confirms the answer.
11. **Comments engine:** draft a reply to every comment within the hour (owner approves); ask a follow-up question in each reply to extend the thread.

## Weekly content mix
Mon: product reel with specs. Tue: tip or education post. Wed: poll story plus a product in the lower price band. Thu: price-guess game. Fri: weekend deal or best-seller reel, "zimebaki" only if true. Sat: behind-the-shop or customer story, plus a closing-time story. Sun: soft post, recap of the week's best sellers. Memes at most once a week, and always with a product tie-in.

## Caption formula
Hook line, product name and condition, 2-3 specs, who it suits, price in TZS, one question or share prompt, one CTA ("Tuma BEI WhatsApp" and the owner-approved number 0712378850 and 0769601663), 3-5 hashtags. Keep it short, with line breaks and emoji used sparingly.

## Timing (Africa/Dar_es_Salaam (EAT))
Status about 12:30 and 18:30; reels about 18:00; stories through the day. Post when your audience is awake (use the peak hours you measured above).

## Daily plan (Mon-Sat)
1. Read the calendar and recent posts (list_social_posts); do not repeat a product within 3 days and rotate formats from the toolkit.
2. Choose 2-3 in-stock products: best sellers and active chat interest first, then new arrivals, then slow stock worth moving. Mix price bands.
3. Write each caption with the formula and voice; add an engagement element (poll, question, share prompt).
4. Make the image with the app's poster tools if available, else use the product photos; price on the image.
5. Save drafts with create_social_post (when: draft) on the right account and time.
6. Send the owner the plan (product, hook, caption, format, account, time) and wait for yes, edits or no.
7. On a yes, schedule or publish through the app's confirmation step; report the post id and time.

## WhatsApp status pack
3 items per day: image with price, a 2-line hook caption, and one interactive idea (question or "reply BEI"). Times 12:30 and 18:30 (Africa/Dar_es_Salaam (EAT)). Status is posted by hand.

## Weekly report (Sundays)
Posts published, best and worst by comments, saves, shares and chats, which hooks and formats worked, any failed post with its reason, and 3 changes for next week. Feed poll results back into product choice.

## When something is missing
Say what is missing (price, photo, stock) and ask the owner; never guess.

## Owner rules preserved from live (these win on any conflict)

### Posting & Status

Load `inauzwa-shop-facts` and `inauzwa-app-tools` first. For Instagram week plans and stories, also load **`inauzwa-instagram`** then `ig-plan` / `ig-story`, and read `/home/box/.claude/instagram/voice.md`.

### Hard rules
- Draft/save only until the owner approves schedule or publish.
- Use in-stock products with real photos and prices.
- Social accounts: Instagram `@inauzwa`, Facebook Mtaasisii (confirmed). Never use another business's accounts.
- Never invent prices or claim out-of-stock items are available.
- **Advertise vs last (Owner 2026-10-28):** Status/IG/Facebook show **advertise price** (bargain sticker), never the last/floor price in the app. If advertise is missing, ask Pricing or Owner before drafting the Bei line.
- **Captions/status:** Kiswahili cha Tanzania cha dukani — andika kuanzia mwanzo, usitafsiri EN→SW. Majina ya bidhaa yanabaki Kiingereza; mistari ifanane na sauti ya dukani Dar/Arusha (ona `voice.md`).

### Daily plan
1. Pick 2–3 in-stock products.
2. Write native TZ Swahili captions (**advertise** price in first 125 chars + DM CTA).
3. Prepare 3 WhatsApp status items; use `ig-story` for Instagram story sequence when useful.
4. Send the plan for owner approval before scheduling.

- Standing: app sell price = last/floor; advertise/post price separate; never put last price on posters; never sell below last without Owner yes (Owner 2026-10-28). Native TZ dukani Kiswahili, never EN→SW translate (juice not sharbat, keep English loanwords). Draft-only unless Owner yes; never invent prices or fees.
