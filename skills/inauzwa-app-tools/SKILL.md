---
name: inauzwa-app-tools
description: >-
  Use alongside any Inauzwa skill whenever you need live shop data or want to
  act in the inauzwa app: which app tool answers which question, and which
  actions need owner approval.
---
# Inauzwa app tools map (live data first)

Rule: any price, stock level, fee, warranty, balance, repair or follow-up status comes from the inauzwa app through its connector (namespace user-inauzwa), never from memory or from a playbook. Look the tool up with GetDynamicTools before calling it. If a lookup fails or returns nothing, say "haipo kwenye mfumo" and flag the owner. Never invent a number.

## Read-only lookups (safe, use freely)
- Business overview: get_ceo_dashboard, get_dashboard_summary, get_analytics_report.
- Products and stock: search_products, get_product, get_inventory, lookup_stock_unit, get_incoming_stock, get_stock_valuation, list_stock_movements.
- Money: get_receivables, list_installments, get_installment.
- Follow-ups: get_today_follow_ups, get_follow_ups.
- Inbox: get_inbox_queue, list_social_inbox, get_conversation_report, get_inbox_automation.
- Repairs: get_repair_board, get_repairs, get_repair. Trade-ins: list_trade_ins, get_trade_in, estimate_trade_in_offer (staff-only), list_trade_in_valuation_rules, list_trade_in_market_prices.
- Captain (Msaidizi): list_captain_assistants, get_captain_assistant, list_captain_training, list_captain_learning_candidates.
- Team: list_team_reports.

## Actions that change the app (draft first, owner approves, then confirmation step)
- Captain: update_captain_assistant, upsert_captain_scenarios, upsert_captain_training, manage_captain_documents, set_captain_inboxes, decide_captain_learning_candidate.
- Follow-ups and campaigns: create_follow_up, update_follow_up, complete_follow_up, dismiss_follow_up, upsert_follow_up_campaign, start_follow_up_campaign.
- Repairs, trade-ins, installments, stock, payments: create_repair, update_repair_status, take_repair_payment, make_trade_in_offer, record_installment_payment, create_stock_adjustment, transfer_stock and similar. Never mark a payment received until the owner confirms.
- Inbox settings: update_inbox_automation, update_inbox_settings, set_inbox_members.

## Per role
- Sales closer: search_products, get_inventory, lookup_stock_unit before quoting; list_installments for plan rules.
- Follow-up: get_today_follow_ups, get_follow_ups, get_receivables; never complete or dismiss without approval.
- Captain trainer: get_captain_assistant, list_captain_training; changes only after owner agrees.
- Repairs desk: get_repair_board, get_repairs, estimate_trade_in_offer (internal only).
- Ops manager: get_ceo_dashboard, get_analytics_report, get_receivables, get_inbox_queue, get_stock_valuation.
- Marketing: search_products, get_inventory, list_social_inbox; never advertise out-of-stock items.

## Known quirks
- Some write tools return requires_confirmation with a token; call again with the same arguments and token only after the owner has approved. A token works once.
- If the connector is signed out or returns 404, tell the owner and stop guessing numbers.
