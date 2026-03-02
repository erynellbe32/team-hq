# 🌱 Team HQ

Task management dashboard for AI agent teams.

## What is HQ?

HQ is a Trello-like task board where you can:
- Assign tasks to AI agents (Trader, Designer, Marketer, Security, Secretary)
- Track tasks through Kanban columns (Backlog → To Do → In Progress → Review → Done)
- Agents can login and update their own task status
- All tasks sync to the cloud (JSONBin)

## Quick Start

1. Open `board.html` in your browser
2. Login as "Sir" for full access
3. Add tasks and assign to agents
4. Click "Trigger" to notify agents

## Accessing from Anywhere

### Option 1: Deploy to Vercel (Recommended)
```bash
# 1. Go to https://vercel.com
# 2. Drag & drop the TeamDashboard folder
# 3. Your HQ is live!
```

### Option 2: Deploy to Netlify
```bash
# 1. Go to https://netlify.com
# 2. Drag & drop the TeamDashboard folder
# 3. Your HQ is live!
```

## Cloud Sync

Tasks are stored in JSONBin. To connect:

1. Create account at [jsonbin.io](https://jsonbin.io)
2. Create a new bin
3. Copy the bin ID and private key
4. Update these values in `board.html`:
```javascript
const JSONBIN_BIN_ID = 'your-bin-id';
const JSONBIN_PRIVATE_KEY = 'your-private-key';
```

## Features

- **👑 Sir Mode**: Full access - add tasks, trigger agents, delete tasks
- **🤖 Agent Mode**: Login as agent to see and update your tasks only
- **🔄 Auto-sync**: Tasks sync to cloud every 30 seconds
- **📨 Trigger**: Notify agents when tasks are ready
- **📊 Status**: Daily status updates posted to Telegram at 6 PM

## Agent Login

| Agent | How to Login |
|-------|-------------|
| Sir | Select "Sir (Full access)" |
| Trader | Select "Trader" |
| Designer | Select "Designer" |
| Marketer | Select "Marketer" |
| Security | Select "Security" |
| Secretary | Select "Secretary" |

## Commands

When you say **"HQ"** to the manager, it refers to this dashboard.

## Files

```
TeamDashboard/
├── board.html      # Main dashboard (open this)
├── README.md       # This file
└── agent-info.md   # Info for agents
```

## Tech Stack

- Pure HTML/CSS/JS (no build needed)
- JSONBin for cloud storage
- LocalStorage for fallback

## License

MIT
