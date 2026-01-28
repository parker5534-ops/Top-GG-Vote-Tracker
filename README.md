# Top.gg Vote Tracker

A multi-server Discord bot that tracks Top.gg votes with streaks, leaderboards, and server-scoped totals — built for fairness, transparency, and review compliance.

---

## What This Bot Does

• Receives Top.gg vote webhooks in real time  
• Posts rich vote notification embeds  
• Tracks per-user and per-server vote stats  
• Supports multiple Discord servers safely  
• Prevents vote leakage across servers  
• Runs 24/7 on a VPS (no sleeping)

---

## How Vote Tracking Works

Top.gg votes are global, but this bot uses **server opt-in routing**:

1. A server admin runs `/setup`
2. Vote tracking starts from zero for that server
3. Votes are only credited if the voter is a member of the server
4. Each server tracks its own lifetime, monthly, and weekly stats

No votes are shared across servers.

---

## Slash Commands

### Admin Commands
• `/setup` – Enable vote tracking and choose a channel  
• `/config` – Change the vote channel  
• `/disable` – Disable vote tracking  
• `/reset` – Reset weekly or monthly counters  

### User Commands
• `/votes` – View your vote stats  
• `/leaderboard` – View server leaderboards  
• `/help` – Show help and usage information  

---

## Privacy

This bot stores only the following data:

• Discord User IDs  
• Discord Server IDs  
• Vote timestamps  
• Vote counts and streak data  

No personal information is collected.  
No message content is stored.  
No data is sold or shared.

---

## Self-Hosting (Developers)

### Requirements
• Node.js v18+  
• npm  
• A VPS or always-on server  
• A Discord bot application  
• A Supabase project  
• A Top.gg bot listing  

---

This repository is provided for transparency; the hosted bot runs independently.

### Installation

```bash
git clone https://github.com/YOUR_USERNAME/topgg-vote-tracker.git
cd topgg-vote-tracker
npm install
