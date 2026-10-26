# Inauzwa bots backup

Backup of Grok Bot team **skills** and **agent profiles** for Inauzwa Limited.

**Repo:** https://github.com/Mtaasisi/DukaniProBot

## Quick links (public)

- **Browse:** https://github.com/Mtaasisi/DukaniProBot
- **Download zip:** https://github.com/Mtaasisi/DukaniProBot/archive/refs/heads/main.zip
- **Clone:**
  ```bash
  git clone https://github.com/Mtaasisi/DukaniProBot.git
  ```

## What’s here

- `skills/` — reusable skill playbooks (`SKILL.md`)
- `agents/` — each bot’s `profile.json` + `settings.json`
- `routines/` — automation definitions when available
- `meta/manifest.json` — snapshot index

## What is NOT here

- Chat history / transcripts
- Secrets, API tokens, vault items
- Live Inauzwa shop data

## Restore / install (simplest)

1. Open **Grok Bot** (coordinator) in the Grok Bot app.
2. Say: **restore from DukaniProBot**  
   Or paste this zip link:  
   `https://github.com/Mtaasisi/DukaniProBot/archive/refs/heads/main.zip`  
   Or ask to restore one piece: **restore skill inauzwa-sales-closer** / **recreate bot Sales Closer**.
3. Grok Bot pulls from this repo and reinstalls skills; recreates missing bots from `agents/*/profile.json`.

Manual (optional): copy a folder from `skills/<slug>/` and ask Grok Bot to save it with UpdateSkill, or recreate a bot from the matching `agents/*/profile.json` name + description.

## Auto-backup

Weekdays ~7:00 Africa/Dar_es_Salaam, Grok Bot re-exports skills + profiles and pushes here when GitHub access works.

## Privacy

Prefer keeping this repository **Private** if shop playbooks should not be public. Change visibility in GitHub → Settings → Danger Zone → Change repository visibility.
