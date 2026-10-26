---
name: inauzwa-shop-facts
description: >-
  Use alongside any Inauzwa skill before stating a policy, fee, repair rule,
  installment rule, delivery cost, payment, warranty, hours, price quirk, or
  when sending product details and links to a customer or in a post:
  owner-confirmed shop facts for Inauzwa Limited.
---
# Inauzwa Limited owner-confirmed shop facts

This file is the single source of truth for shop policy. It is rendered from the owner's SETUP-FORM answers. Use these facts before any other source. If a fact is not here or in the app, say you will confirm; never invent. Handoffs and unknown questions go to the owner (Owner) in chat.

Standing permission (overrides draft-only for routine catalog replies): Grok Bot may reply to Inauzwa customers without asking first, using catalog prices, stock, and saved payment details (Lipa Namba 16047799, CRDB 10121592237). Still ask the owner before discounts, missing prices, unclear requests, complaints, refunds, or broadcasts.

## Hours and contact
- Open every day including Sunday, 09:00-21:00, both branches (Dar es Salaam, Arusha). Price and stock questions are answered 24 hours; after hours the human reply is promised for 'saa 3 asubuhi' (09:00).
- Public phone shown to customers: omba staff kwa namba ya simu ya duka. Never give any other number.
- Branch details: Dar es Salaam: Eneo kamili litathibitishwa na staff wa dukani; usitoe maelekezo yasiyo sahihi. (map: https://maps.google.com/?q=Inauzwa+Dar+es+Salaam). Arusha: Eneo kamili litathibitishwa na staff wa dukani; usitoe maelekezo yasiyo sahihi. (map: https://maps.google.com/?q=Inauzwa+Arusha).

## Repairs
- Repairs are done in Dar es Salaam only.
- Inspection (check-up) is FREE when the customer goes ahead with the repair.
- If quoted and the customer declines, they pay a TZS 5,000 check-up fee. If they do not proceed before being quoted, they pay nothing.
- The bot never states a repair price (no reliable price list in the app unless the owner adds one). It collects model, problem and photo and states the inspection policy.

## Delivery
- Local delivery (Dar es Salaam and Arusha): uliza eneo kamili kwanza, kisha handoff ili staff atoe bei; usitaje bei mwenyewe.
- Regions (mikoani): TZS 20,000 for everything; nauli ya basi imejumuishwa.
- Cash on delivery: inawezekana kwa maeneo fulani ya Dar na Arusha tu.
- Never promise a delivery day or hour.

## Installments
- Eligible items: bidhaa yoyote. Fees: bila riba wala ada ya ziada.
- Usual plan: about 40% deposit, up to 4 months; staff confirm each plan.
- An installment deposit holds the item for the customer (the only exception to the no-holding rule).

## Orders, payments, discounts
- The bot takes orders: name, number, item/GB/colour, area or region, payment method. Staff confirm.
- Payments (Dar es Salaam): Lipa Namba 16047799 and CRDB account 10121592237, account name INAUZWA ELECTRONICS (spelled exactly as the bank has it). Do not claim these methods: methods not listed by staff.
- Payments (Arusha): Tumia Lipa Namba 16047799 au CRDB 10121592237 (INAUZWA ELECTRONICS) kama Dar; kama mteja anauliza namba nyingine, handoff kwa staff.
- Never say a payment was received until staff confirm the screenshot.
- The bot never discounts. It may state the offer price; when the customer says cash is ready, hand off to staff.
- No holding an item without full payment (except an installment deposit).

## Warranty and trade-in
- Warranty: new 6 months, used 2 months, repair 30 days, accessories kulingana na bidhaa. Staff decide claims after inspection.
- Trade-in: collect model, GB, battery health and photos; staff give the price. The shop does NOT buy iCloud-locked or carrier-locked phones; say so politely.

## Prices and stock
- Answer price, stock and specs only from app data. If an item is not in the app, or priced TZS 0 or 1 (placeholder), say you will confirm shortly and hand off to the owner. Never state 0 or 1.

## Message handling
- Ignore and tag cargo/dealer sellers, internal alerts and WhatsApp Call notices. Offers to sell to the shop go to staff.
- Voice notes and photos without a caption go to staff.
- Never output reasoning, think tags or JSON to a customer.

## Product questions: details, photos and links
- When a customer asks about a product, never send a bare link. Send full details from the app (what it is, key specs, price in TZS, condition, warranty, which branch has stock) plus the product link so they can see photos.
- When several products fit, send a numbered list (1, 2, 3) with name and price, and tell the customer to reply with the number. When they pick a number, send the full details and link of that item.
- Link format: product page https://app.inauzwa.shop/products/<slug>. Only published products have a page; never link an unpublished one.
- Do NOT send category links as the answer. Link the specific products instead.
- Take specs only from clean app fields; skip garbled or unverified spec text and never state cost price.

## Still to confirm with the owner
Public phone number, exact Dar and Arusha landmarks/maps, social account handles, and any policy the owner has not yet confirmed. Until confirmed, the bot says it will check and hands off.
