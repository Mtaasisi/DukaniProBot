---
name: inauzwa-catalog-seo
description: >-
  Use to add or audit products in the Inauzwa app: create unpublished with SEO copy, fix missing fields, never publish or change price without owner yes. App
---
# Catalog and SEO

Read inauzwa-shop-facts and inauzwa-app-tools first. Full owner master instructions (reference, read when unsure): reference/catalog-master-instructions.md (copy it to /workspace/catalog-master-instructions.md). Never invent specs, prices or stock; accuracy beats completeness.

## Workflow when the owner gives a model number or product name
(The admin agent relays the owner's messages.)
1. Research the EXACT model on the internet first (official maker product page, official tech specs, support docs, manuals, datasheets; then authorized distributors, established tech publications, reputable parts suppliers for compatibility). Open the real pages, cross-check more than one source, never rely on snippets. Marketplace listings may identify a product or price but never override official docs. If browsing is unavailable say: 'Internet verification unavailable. Specifications below are provisional.' Never invent sources, URLs or verification results. If sources disagree, say so; do not silently pick one.
2. Identify exactly: manufacturer, model, model number, generation, release year, chip/processor variant, supplied configuration, regional variant. A model number can cover several configs (e.g. MacBook Pro A2485 may be M1 Pro or M1 Max; MINISFORUM MS-02 Ultra 5 vs Ultra 9; look-alike soundbars differ). Never mix variants; if a model number covers several variants use only specs shared by all and mark the rest 'Not verified'. RAM/SSD/colour the owner gives are the actual stock configuration; do not assume other parts. Distinguish max supported capacity vs installed, rated vs peak power, theoretical vs real speeds, official specs vs seller claims.
3. Prepare the full catalog block (format below) and LIST EXACTLY WHAT IS MISSING, typically price, quantity per branch, condition, colour, warranty. Send that list to the admin agent (Grok Bot) so the owner is asked with buttons and fill-in fields. Do not ask the owner directly when the request came via the admin.
4. After the owner answers, create the product in the app UNPUBLISHED (create_product, variants, specifications, warranty text per shop facts) with images only if an exact-product image can be found (never generated images, never a different model). Then update_seo, verify with get_product, get_seo, seo_audit, audit_product_data.
5. Report to the admin: product id and link, checklist (created, specs, images, SEO score, issues, what needs the owner). WAIT for the owner's explicit yes before publish_product or sync_storefront_catalog.

## Product name, SKU, brand, category, type
- Names: concise, professional, real brand + model; no hype. Laptop: Brand + Model + Screen when useful + (Processor/RAM/Storage), e.g. 'HP EliteBook 840 G7 (i5/8GB/256GB)', 'MacBook Pro 16" A2485 (M1 Pro/32GB/1TB)'; include a processor only when verified. Soundbar: Brand + Model + Channels + Power + Soundbar. Spare part: Brand + Device + Part Name + Compatible Model Numbers, not overloaded.
- SKU: keep an owner-supplied SKU exactly. Otherwise generate a clean internal one (APL-MBP-A2485-32-1TB, HIS-HS218-200W, MIN-MS02U-U9-32-2TB, APL-MBA-2014). Never call a generated SKU a manufacturer part number. Separate SKUs for separate inventory variants.
- Brand, Category and Product Type are mandatory. Product Type is EXACTLY one of: Product, Spare Part, Accessory, Service. Category must be an EXISTING category (and an active one; check get_product_lookups). The shop's current categories: Phones, Laptops, Tablets, Power Banks, Chargers, Spare Parts, Accessories (use get_product_lookups live). Never create a category or brand automatically; if none fits, suggest an existing one or propose a new one for owner approval. Examples: laptops/MacBooks Laptops+Product; mini PC Computers+Product; MacBook LCD Spare Parts+Spare Part; USB-C hub USB Hubs & Adapters+Accessory; iPhone Smartphones+Product.

## Copy standard (Kiswahili (Tanzania)-English)
- Natural Tanzania Kiswahili with familiar English tech terms (Processor, RAM, SSD, Display, Battery, Bluetooth, Soundbar, Graphics); no awkward translations, no hype, no unsupported promises of performance, battery life, durability or compatibility. Do not repeat every spec in the description.
- Short Description: ONE paragraph, about 35-65 words: exact model, key feature/processor, RAM and storage, display or audio, main uses. No unverified features.
- Description: 2-4 short paragraphs (laptops use 4): (1) design and body, (2) processor, graphics, storage and the benefit, (3) connectivity and ports plus keyboard and trackpad, (4) who it suits plus an honest age/compatibility note for older models. Soundbars: verified channels, formats, subwoofer, connectivity, uses. Mini PCs: processor, RAM, SSD, networking, expansion. Spare parts: purpose, exact compatibility, installation notes, part type.
- Specifications: bullet lists under CAPS headings, only groups that fit the device. Laptops: GENERAL (brand, series, model year, manufacturer, body material, screen sizes), PROCESSOR, MEMORY, STORAGE, GRAPHICS, DISPLAY, CONNECTIVITY (Wi-Fi, Bluetooth, USB, Thunderbolt, charging port, audio port, card slot), CAMERA & AUDIO, KEYBOARD & TRACKPAD, BATTERY & POWER, OPERATING SYSTEM (incl. latest supported OS, only when verified from current maker docs; do not confuse shipped OS with latest supported), PHYSICAL (design, color). Soundbars: GENERAL, AUDIO SYSTEM, POWER, SUBWOOFER, SURROUND SPEAKERS, AUDIO TECHNOLOGIES, CONNECTIVITY, PHYSICAL. Mini PCs: GENERAL, PROCESSOR, MEMORY, STORAGE, GRAPHICS, EXPANSION, NETWORKING, CONNECTIVITY, POWER & COOLING. Spare parts: GENERAL, PART TYPE, COMPATIBLE MODELS, MODEL NUMBERS, TECHNICAL SPECIFICATIONS, COLOR, INSTALLATION NOTES. Phones, TVs, accessories get sensible groups of their own. Never pad with irrelevant fields. Never invent CPU/GPU cores, power output, resolution, refresh rate, battery capacity or life, port count, RAM speed, SSD interface, dimensions, weight, OS compatibility, wireless connectivity or warranty: omit or write 'Not verified'.
- Search Keywords: comma-separated; model + year, model numbers, Tanzania, Dar es Salaam, 'Used' or 'Second Hand' when used, name variants.
- Also SEO fields: seo_title up to 70 characters, meta_description up to 160, clean slug, intro, 3-5 FAQ items, image alt text. FAQ delivery answer follows inauzwa-shop-facts exactly (local delivery rule, regional fee, no 'bure'/free claims unless confirmed, no tax-receipt claim unless the owner confirms, no cash-on-delivery promise beyond the confirmed areas).

## MacBook rules
Verify A-model number, release year, model identifier, processor generation and exact chip (M1/M1 Pro/M1 Max/M2... M5 Max; an A-model does not uniquely identify the chip), RAM, SSD, screen size and resolution, display tech, ports, battery, macOS compatibility. Use the exact verified chip.

## Spare-part compatibility
Compatibility accuracy is critical. Verify exact compatible model numbers and part numbers with reputable repair documentation. Distinguish Complete Display Assembly, LCD Panel Only, Glass Only, Battery, Keyboard, Top Case, Logic Board. Never assume interchangeability from screen size, resolution, generation, looks or similar names; say so when cross-compatibility is uncertain. Never merge inventory SKUs unless compatibility is verified.

## Price and stock
Price comes from the owner; never invent one and never use TZS 0 or 1. If the owner asks for market research: distinguish Buying Price, Market Selling Price and Recommended Listing Price; prefer Tanzania prices in TZS; state currency, date checked, source and seller per price; if none verified write 'Price: Not verified.' Quantity only if given (e.g. 6 Pcs); otherwise omit. No cost price in any public text.

## Output format for a catalog block
ONE single plain-text code block (no tables, no emojis, no citations, no links inside), exactly this order, omitting fields that do not apply and leaving no empty placeholders: Product Name, SKU, Brand, Category, Product Type, Quantity (only if given), Price (only if given/verified), Short Description, Description, Specifications (bullets), Search Keywords. After the block, a separate short 'Verification Sources' note (2-5 real sources, prefer official links; unresolved critical info, e.g. 'A2485 can have M1 Pro or M1 Max; exact chip requires confirmation'). Only claim verification for sources actually inspected.

### Example (format illustration: Apple MacBook Air (2014), SKU APL-MBA-2014, Laptops)
Short: 'Apple MacBook Air (2014) ni laptop nyembamba na nyepesi yenye Intel Core processor, Intel HD Graphics 5000 na SSD storage. Ina muundo wa aluminum, backlit keyboard na Multi-Touch trackpad. Inafaa kwa wanafunzi, matumizi ya nyumbani, internet browsing, kuandika documents na kazi nyepesi za ofisini.' Specs: Early 2014; 11.6 / 13.3 inch; Core i5 1.4GHz, optional i7; Intel HD 5000; 802.11ac, Bluetooth 4.0, 2x USB 3.0, Thunderbolt, MagSafe 2; 720p camera; 45W adapter; macOS Big Sur 11 latest; Silver. Keywords: 'Apple MacBook Air 2014, MacBook Air Early 2014, MacBook Air Intel Core i5, Apple MacBook Air Laptop, MacBook Air Used, MacBook Air Tanzania, MacBook Air Dar es Salaam, Apple Laptop 2014, MacBook Air Second Hand'.

## Quality check before sending
Brand, exact model and variant right; RAM/storage exactly as supplied; specs from the correct model, no mixed variants; category existing and active; Product Type valid; SKU consistent; descriptions factual; prices verified or omitted; everything in one code block; uncertainties disclosed; sources real.

## Adding in the app: tool notes
get_product_lookups for brand/category ids; search_products first to avoid duplicates; create_product (unpublished), create_product_variant, update_product_specifications (with sources), add_product_images_from_url (exact product only; best image as cover; alt text via update_product_image_alt), update_seo, then verify with get_product, get_seo, seo_audit, audit_product_data, get_catalog_health. Used items: condition and battery health in the description. Warranty from inauzwa-shop-facts (new, used and accessories terms).

## Auditing
Run audit_product_data and get_catalog_health; list published products missing price, image or slug, duplicates, price 0 or 1, cost 0, garbled spec text (HTML junk, 'Verify supplier/OEM label'), missing template sections, missing brand/category (active ones), no storefront page. Customer replies send full details plus https://app.inauzwa.shop/products/<slug>, so pages must be complete and clean. Propose fixes; apply only what the owner approves via the app's confirmation flow.

## Never
Publish, change price or cost, merge, unpublish or archive without the owner's explicit yes. Use images of a different model or generated images as product photos. Invent specs, prices or stock.

## Owner rules preserved from live (these win on any conflict)

### Catalog & SEO

Load inauzwa-shop-facts and inauzwa-app-tools first. Load tanzania-retail-pricing when setting or proposing prices.

### Hard rules
- New products created UNPUBLISHED.
- Publishing, price/cost changes, merges, archiving only after explicit owner yes.
- Never invent specs, prices or stock. Never use price TZS 0 or 1.
- Categories only from existing list: Phones, Laptops, Tablets, Power Banks, Chargers, Spare Parts, Accessories.
- **App sell price = last price (Owner 2026-10-28)** — the bargain floor staff may accept. Do not write advertise/sticker prices into the catalog unless the app has a separate field for them; Marketing/Pricing keep advertise outside the last-price field.

### Playbook
Research model → write Swahili-English catalog block → create unpublished → audit (audit_product_data, get_catalog_health) → report checklist for owner.

- Standing: app sell price = last/floor; advertise/post price separate; never put last price on posters; never sell below last without Owner yes (Owner 2026-10-28). Native TZ dukani Kiswahili, never EN→SW translate (juice not sharbat, keep English loanwords). Draft-only unless Owner yes; never invent prices or fees.
