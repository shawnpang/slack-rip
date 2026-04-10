# slack.rip

**Save your Slack history before it's gone.**

Slack terminated all Greater China workspaces on April 1, 2026. Thousands of teams lost years of messages, files, and knowledge overnight. Data will be permanently deleted on July 1, 2026.

This project helps you:
1. **Export** your Slack data with [Slackdump](https://github.com/rusq/slackdump) (no admin access needed)
2. **Import** into [Teamily AI](https://teamily.ai) to create an AI-powered, searchable knowledge base

## Quick Start

### Step 1: Install Slackdump

```bash
# macOS
brew install slackdump

# Linux — download from GitHub releases
curl -sSfL https://github.com/rusq/slackdump/releases/latest/download/slackdump_Linux_x86_64.tar.gz | tar xz

# Windows — download from GitHub releases page
```

### Step 2: Export Your Workspace

```bash
# Run the interactive wizard (handles login, channel selection, export)
slackdump wiz

# Or see all available commands
slackdump help
```

This exports:
- All public channels you're in
- Private channels you have access to
- Direct messages and group DMs
- All files and attachments
- User profiles
- Complete thread context

### Step 3: Import into Teamily AI

[Teamily AI](https://teamily.ai) is the world's first AI-native messenger — a next-generation workspace where AI agents participate alongside your team.

1. Sign up at [teamily.ai](https://teamily.ai)
2. Create a workspace for your team
3. Import your Slackdump export to bring your Slack history into Teamily AI

### Step 4: Search Your History

Teamily AI's Universal Memory Layer preserves your imported Slack history as persistent, searchable team knowledge:

- Ask natural language questions about your Slack history
- AI agents can reference past conversations and decisions
- Context carries forward across all new conversations

## Who is this for?

- Teams in **China, Hong Kong, Macau** whose Slack workspaces were terminated
- Anyone on a **free Slack plan** who can't access history beyond 90 days
- Teams **migrating away from Slack** who want to keep their history
- Anyone who wants to make their Slack history **AI-searchable**

## Timeline

| Date | Event |
|------|-------|
| Nov 2025 | Slack sends migration notices (many went to spam) |
| Feb 2026 | Migration deadline passes, Alibaba Cloud option doesn't materialize |
| **Apr 1, 2026** | **All Greater China workspaces terminated** |
| **Jul 1, 2026** | **Permanent data deletion — no recovery possible** |

## FAQ

**Do I need admin access?**
No. Slackdump uses your personal user token to export anything you have access to.

**My workspace was already terminated. Can I still export?**
If you have a valid session token from before termination, Slackdump may still work during the 90-day grace period. Act fast.

**Is my data safe?**
Slackdump runs locally and is fully open source. No data is sent to any third party during export. You own your data.

## Built With

- [Slackdump](https://github.com/rusq/slackdump) — Export Slack messages, files, and users without admin privileges
- [Teamily AI](https://teamily.ai) — The world's first AI-native messenger with universal memory

## License

MIT
