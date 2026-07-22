# Daratech Bot — WhatsApp Bot

Multi-purpose WhatsApp bot with 465+ commands built with [Baileys](https://github.com/WhiskeySockets/Baileys).

## Stack

- **Runtime:** Node.js 18+
- **WhatsApp:** @whiskeysockets/baileys
- **Entry point:** `index.js`

## Running on Replit

The workflow `Start application` runs `node index.js`.

### First-time setup (pairing)

1. Make sure `OWNER_NUMBER` is set as an environment variable (your WhatsApp number, country code + digits, no `+` or spaces — e.g. `5599984843091`).
2. Start the workflow. A **pairing code** will appear in the console logs.
3. In WhatsApp: **Settings → Linked Devices → Connect a device → Connect with phone number** → enter the code.
4. Once connected, the session is saved in the `session/` folder. Future restarts reconnect automatically — no re-pairing needed.

### Re-pairing (if session expires)

Delete the `session/` folder contents and restart the workflow.

## Environment Variables

| Key | Description |
|-----|-------------|
| `OWNER_NUMBER` | Your WhatsApp number with country code (no `+` or spaces) |

## Key files

- `index.js` — bot entry point, WhatsApp connection & pairing
- `main.js` — message routing and command dispatch
- `settings.js` — bot name, owner number, GitHub repo for auto-update
- `commands/` — individual command modules (465+ commands)
- `lib/` — utilities (exif, store, auto-update, etc.)
- `data/` — persistent JSON state (ban lists, economy, etc.)
- `session/` — WhatsApp session credentials (gitignored)

## User preferences

- Language: Portuguese (Brazilian)
