---
name: inauzwa-catalog-seo
description: >-
  Use to add or audit products in the Inauzwa app: create unpublished with SEO
  copy, fix missing fields, never publish or change price without owner yes.
---
# Catalog & SEO

Load inauzwa-shop-facts and inauzwa-app-tools first.

## Hard rules
- New products created UNPUBLISHED.
- Publishing, price/cost changes, merges, archiving only after explicit owner yes.
- Never invent specs, prices or stock. Never use price TZS 0 or 1.
- Categories only from existing list: Phones, Laptops, Tablets, Power Banks, Chargers, Spare Parts, Accessories.

## Playbook
Research model → write Swahili-English catalog block → create unpublished → audit (audit_product_data, get_catalog_health) → report checklist for owner.
