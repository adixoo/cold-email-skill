# Cold Email skill for Claude

Write cold emails and DMs that actually get replies: to startup founders, recruiters, hiring managers, employees (for referrals) and freelance clients. Includes follow-ups, how to answer replies, and a simple outreach tracker.

Method adapted from the [Cracked the Cold Email Game](https://crackcoldemail.vercel.app/) playbook by Sumit Kesarwani.

## Why

Most cold emails fail because they ask a stranger for a favour ("Please find my resume attached, kindly let me know if there are openings"). This skill makes Claude write messages that give the reader a real reason to reply, using one formula:

**Context + Relevance + Proof + A Small Ask**

| Part | What it means |
|------|---------------|
| Context | One specific, true observation about their company, product or work |
| Relevance | Your 1-2 skills that match what they're building or hiring for |
| Proof | 1-2 links to real work: portfolio, GitHub, deployed project |
| Small ask | Exactly one easy question |

Kept to 80-150 words, because most people read email on their phone.

## What it does

1. **Asks before writing.** It asks for only the details that are missing: your goal, the recipient, the company, one thing you noticed about them, your relevant skills and your links. It never invents facts or results.
2. **Picks the right template** for your goal.
3. **Writes the message** with a subject line, in plain human language (no "esteemed organization", no AI filler).
4. **Checks the draft** against a short checklist, then gives you a follow-up plan.
5. **Helps with what comes next**: answering replies and tracking reply rates.

### The 6 templates

| # | Use it to | Sent to |
|---|-----------|---------|
| 1 | Join a startup | Founder |
| 2 | Apply for an advertised role | Recruiter / hiring manager |
| 3 | Get a referral | Employee at the company |
| 4 | Find freelance clients | Business owner |
| 5 | Send a short DM | Anyone on LinkedIn / X / WhatsApp |
| 6 | Follow up | Someone who hasn't replied |

## Install

Quick version (full steps in **[INSTALL.md](INSTALL.md)**):

- **Claude Code:**
  ```
  /plugin marketplace add <github-user>/<repo>
  /plugin install cold-email@cold-email-skill
  ```
- **claude.ai / Claude apps:** Settings → Capabilities → Skills → **Upload skill** → choose [`cold-email.zip`](cold-email.zip).
- **Manual:** copy `skills/cold-email` into `~/.claude/skills/`.

## Usage

Just ask in plain words:

- "Write a cold email to the founder of Acme for a backend internship"
- "Help me ask an engineer at Stripe for a referral for this role: <job link>"
- "Pitch my web design services to this bakery: <website>"
- "Write a LinkedIn DM to a recruiter at Razorpay"
- "They didn't reply to this email, write a follow-up: <email>"
- "Make me an outreach tracker"

In Claude Code you can also type `/cold-email`.

### Example

> **You:** Write a cold email to the founder of a startup for a frontend internship.
>
> **Claude:** Asks for the founder's name, the startup, one thing you noticed about their product, your 1-2 relevant skills, and your portfolio/GitHub links.
>
> **You:** Answer the questions.
>
> **Claude:** Gives a subject line, a ~120-word email ready to copy, one tip to make it stronger, and when to follow up.

## Files

```
cold-email-skill/
├── .claude-plugin/
│   ├── plugin.json           # plugin manifest (name, version)
│   └── marketplace.json      # lets people install via /plugin
├── skills/cold-email/
│   ├── SKILL.md              # the workflow and rules Claude follows
│   └── references/
│       └── templates.md      # the 6 templates
├── cold-email.zip            # upload file for claude.ai
├── INSTALL.md                # step-by-step install guide
└── README.md
```

## Customize

- Change the rules or tone in [`skills/cold-email/SKILL.md`](skills/cold-email/SKILL.md).
- Add or edit templates in [`skills/cold-email/references/templates.md`](skills/cold-email/references/templates.md).
- After editing, rebuild `cold-email.zip` and bump `version` in `.claude-plugin/plugin.json` (see [INSTALL.md](INSTALL.md#d-publish-it-so-anyone-can-install-it)).

## Credits

Based on the cold outreach playbook by Sumit Kesarwani: https://crackcoldemail.vercel.app/. Templates are rewritten, not copied; read the original for the full story and examples.

Results depend on your targeting, message, proof of work and timing. No template guarantees replies.
