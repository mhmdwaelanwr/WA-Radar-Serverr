# WA Radar Server

A small self-hosted Node.js experiment that watches a WhatsApp Web session and can forward deleted-message events to a Telegram bot for the account operator.

> **Authorized-use only.** Use this project only with WhatsApp accounts, devices, and conversations you are permitted to operate and monitor. Respect participant privacy, applicable law, and WhatsApp / Telegram platform terms. Do not use it for covert monitoring or to access another person's account.

## Technology

- Node.js
- `whatsapp-web.js`
- Puppeteer
- Telegram Bot API

## Local setup

Install dependencies:

```bash
npm install
```

Create a local `.env` file with your own Telegram bot configuration:

```env
TG_TOKEN=your_bot_token
TG_CHAT_ID=your_chat_id
```

Do not commit the `.env` file or any session credentials.

Start the server:

```bash
npm start
```

The WhatsApp Web session must be authenticated by the account owner/operator before the project can observe events available to that session.

## Privacy and security notes

- Deleted messages may still contain sensitive personal information; keep forwarded data private and minimize retention.
- Never publish WhatsApp session files, Telegram bot tokens, chat IDs, QR-authentication data, or exported message content.
- A Telegram bot destination should be controlled by the same authorized operator.
- Review dependency and platform behavior before deploying the project to a persistent server.
- This repository is a development experiment, not a compliance, archival, or forensic product.

## Scope

This repository is provided for self-hosted development and learning. It does not provide a hosted monitoring service and does not grant permission to monitor third-party accounts or conversations.

## License

Review the repository license and the licenses / terms of the upstream libraries and services before redistribution or deployment.