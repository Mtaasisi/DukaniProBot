# Inauzwa bots backup

Private backup of Grok Bot team **skills** and **agent profiles** for Inauzwa Limited.

## What’s here
- `skills/` — reusable skill playbooks (`SKILL.md`)
- `agents/` — each bot’s `profile.json` + `settings.json`
- `routines/` — automation definitions when available
- `meta/manifest.json` — snapshot index

## What is NOT here
- Chat history / transcripts
- Secrets, API tokens, vault items
- Live Inauzwa shop data

## Restore (skills)
1. Copy a skill folder from `skills/<slug>/` into the bot’s workflows (or ask Grok Bot to reinstall with UpdateSkill from the SKILL.md body).
2. Recreate or UpdateAgent using the matching `agents/*/profile.json` name + description.

## Auto-backup
A weekday routine on Grok Bot re-exports and commits here when GitHub is connected.
