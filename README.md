# slack.rip

**Save your Slack history before it's gone.**

Slack terminated all Greater China workspaces on April 1, 2026. Thousands of teams lost years of messages, files, and knowledge overnight. Data will be permanently deleted on July 1, 2026.

This project helps you:
1. **Export** your Slack data with [Slackdump](https://github.com/rusq/slackdump) (no admin access needed)
2. **Import** into [EverOS](https://github.com/EverMind-AI/EverOS) to create an AI-powered, searchable knowledge base

## Quick Start

### Step 1: Install Slackdump

```bash
# macOS
brew install rusq/tap/slackdump

# Linux
curl -sSfL https://github.com/rusq/slackdump/releases/latest/download/slackdump_Linux_x86_64.tar.gz | tar xz

# Windows — download from GitHub releases
```

### Step 2: Export Your Workspace

```bash
# Interactive login (opens browser)
slackdump export -o my-workspace.zip

# Or with token (if you have it)
slackdump export -token xoxc-your-token -cookie "d=your-d-cookie" -o my-workspace.zip
```

This exports:
- All public channels you're in
- Private channels you have access to
- Direct messages and group DMs
- All files and attachments
- User profiles
- Complete thread context

### Step 3: Import into EverOS

```bash
# Install EverOS
git clone https://github.com/EverMind-AI/EverOS.git
cd EverOS
pip install -r requirements.txt

# Import your Slack export
python -m everos import --source slack my-workspace.zip
```

### Step 4: Search Your History

```bash
python -m everos chat
> What did the team decide about the Q3 launch plan?
> Find all messages about the API redesign
> Summarize the #engineering channel from last month
```

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
Everything runs locally. Both Slackdump and EverOS are open source. No data is sent to any third party.

## Built With

- [Slackdump](https://github.com/rusq/slackdump) — Export Slack messages, files, and users without admin privileges
- [EverOS](https://github.com/EverMind-AI/EverOS) — Open-source memory OS for AI-powered knowledge management

## License

MIT
