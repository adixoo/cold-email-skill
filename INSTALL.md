# Installation guide

Pick the option that matches where you use Claude. Each takes about 2 minutes.

| You use | Option |
|---------|--------|
| Claude Code (terminal, desktop Code tab, VS Code, JetBrains) | [A. Plugin](#a-claude-code-plugin-recommended) or [B. Manual copy](#b-claude-code-manual-copy) |
| claude.ai in the browser, or the Claude desktop/mobile app chat | [C. Upload the zip](#c-claudeai-and-the-claude-apps) |
| You want to share it with others | [D. Publish it on GitHub](#d-publish-it-so-anyone-can-install-it) |

---

## A. Claude Code plugin (recommended)

Needs the skill to be on GitHub (see [D](#d-publish-it-so-anyone-can-install-it)). Replace `<github-user>/<repo>` with the repo name.

1. Open Claude Code.
2. Add the marketplace:
   ```
   /plugin marketplace add <github-user>/<repo>
   ```
3. Install the skill:
   ```
   /plugin install cold-email@cold-email-skill
   ```
4. Restart Claude Code if it asks you to.

**Update later:** `/plugin marketplace update cold-email-skill`
**Remove:** `/plugin uninstall cold-email@cold-email-skill`

Installing from a local folder instead of GitHub also works:
```
/plugin marketplace add D:/path/to/cold-email-skill
```

---

## B. Claude Code (manual copy)

Copy the `skills/cold-email` folder into your skills folder.

**For all your projects** - Windows (PowerShell):
```powershell
Copy-Item -Recurse "skills\cold-email" "$env:USERPROFILE\.claude\skills\cold-email"
```

macOS / Linux:
```bash
mkdir -p ~/.claude/skills && cp -r skills/cold-email ~/.claude/skills/
```

**For one project only:** copy it to `<your-project>/.claude/skills/cold-email` instead.

Start a new Claude Code session; the skill loads automatically.

---

## C. claude.ai and the Claude apps

1. Download [`cold-email.zip`](cold-email.zip) from this repo.
2. Open [claude.ai](https://claude.ai) → **Settings** → **Capabilities**.
3. Make sure **Code execution and file creation** is turned on (skills need it).
4. Under **Skills**, click **Upload skill** and choose `cold-email.zip`.
5. Make sure the `cold-email` skill is toggled on.

The skill then works in every new chat, on web, desktop and mobile.

> On Team / Enterprise plans an admin may need to allow custom skills first.

---

## D. Publish it so anyone can install it

1. Create an empty **public** repo on GitHub (for example `cold-email-skill`).
2. From this folder, push it:
   ```bash
   git init
   git add .
   git commit -m "feat: add cold-email skill"
   git branch -M main
   git remote add origin https://github.com/<github-user>/cold-email-skill.git
   git push -u origin main
   ```
   Or, with the GitHub CLI: `gh repo create cold-email-skill --public --source . --push`
3. Share the repo link. People install with option [A](#a-claude-code-plugin-recommended) or download the zip for option [C](#c-claudeai-and-the-claude-apps).

**Releasing a new version:** edit the files, bump `version` in `.claude-plugin/plugin.json`, rebuild `cold-email.zip` (zip the `skills/cold-email` folder so the zip contains a top-level `cold-email/` folder), commit and push.

---

## Check it works

Ask Claude:

> Write a cold email to the founder of a startup for a frontend internship

It should first ask you for the missing details (recipient, company, one real observation about them, your skills, your proof-of-work links), then write an 80-150 word email with a subject line and a follow-up plan.

In Claude Code you can also run `/cold-email` directly (plugin installs: `/cold-email:cold-email`).

## Troubleshooting

| Problem | Fix |
|---------|-----|
| Claude writes an email without using the skill | Mention "cold email" or "cold DM" in your request, or call `/cold-email` in Claude Code. |
| `/plugin marketplace add` fails | Check the repo is public and the name is `<user>/<repo>`; the repo root must contain `.claude-plugin/marketplace.json`. |
| Upload rejected on claude.ai | The zip must contain the `cold-email/` folder with `SKILL.md` inside, not the files loose at the top. |
| Skill not showing after manual copy | The path must be `.claude/skills/cold-email/SKILL.md`. Start a new session. |
