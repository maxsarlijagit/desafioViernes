# The Office - Multiplayer Game

A real-time multiplayer office simulation with proximity chat, zone-based voice, and cyberpunk aesthetics.

## Stack
- Backend: Node.js + Express + WebSocket (ws)
- Frontend: Vanilla Canvas 2D
- Renderer: Procedural pixel art sprites

## Setup

```bash
npm install
npm run dev
```

Open http://localhost:3000 in browser.

## Controls
- WASD or Arrow keys: Move
- Chat: Type message + Enter

## Environment Variables

```bash
# Discord Bot (optional)
DISCORD_BOT_TOKEN=
DISCORD_VOICE_OFFICE=
DISCORD_VOICE_FOCUS_ROOM=
DISCORD_VOICE_CAFETERIA=
DISCORD_VOICE_ARCADE=
DISCORD_VOICE_STUDIO=
```

## Deploy to Railway

```bash
railway init
railway up
```

Set PORT env var in Railway.

## Features
- 5 zones: OFFICE, FOCUS ROOM, CAFETERIA, ARCADE, STUDIO
- Proximity chat (4 tile radius)
- Global chat panel
- Avatar animation
- Minimap with player dots