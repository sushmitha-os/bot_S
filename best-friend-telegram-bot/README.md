# Best Friend Telegram Bot (n8n + Groq)

Telegram bot "Buddy" built as an n8n workflow, powered by Groq (llama-3.3-70b-versatile).

## Import
1. In n8n: Workflows -> Import from File -> `best-friend-telegram-bot.json`
2. Open **Telegram Trigger**, **Send Reply**, **Send Text-Only Notice** and select your Telegram credential.
3. Open **Groq Chat Model** and select your Groq credential.
4. Activate the workflow (n8n needs a public HTTPS URL for the Telegram webhook).

## Flow
Telegram Trigger -> Has text? -> (true) Buddy Agent (Groq + Simple Memory, 10 msgs per chat) -> Send Reply
                              -> (false) Send Text-Only Notice
