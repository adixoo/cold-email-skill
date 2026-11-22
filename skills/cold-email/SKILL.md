---
name: cold-email
description: Write personalized cold emails and cold DMs that get replies - to startup founders, recruiters, hiring managers, employees (for referrals) and potential freelance clients - plus follow-ups, reply handling and an outreach tracker. Uses the Context + Relevance + Proof + Small Ask formula, 80-150 words. Use this skill whenever the user wants to write, improve or review a cold email, cold DM (LinkedIn, X, WhatsApp), internship or job outreach, referral request, freelance client pitch, or follow-up email, even if they only say "help me reach out to X" or "email this founder".
---

# Cold Email

Write cold outreach that gives a stranger a genuine reason to start a conversation, instead of asking them for a favour.

Method adapted from the "Cracked the Cold Email Game" playbook by Sumit Kesarwani (https://crackcoldemail.vercel.app/).

## Step 1: Gather the details (ask before writing)

A good cold email needs real, specific facts. Never invent them. Check what the user already gave you, then ask in ONE message for only what is missing. Required:

1. **Goal** - join a startup, apply for a specific role, get a referral, find a freelance client, a short LinkedIn/X DM, or a follow-up.
2. **Recipient** - name and role (founder, recruiter, hiring manager, employee, business owner).
3. **Company / product** - name, and the role title + job link if it's an opening.
4. **One genuine observation** - something specific about their product, feature, recent launch, post, or a real problem you noticed. If the user has none, tell them to spend 5 minutes on the company site/recent posts and come back; offer what to look for. Do not make one up.
5. **The user's relevant skills** - the 1-2 that match THIS recipient, not their whole stack.
6. **Proof of work** - 1-2 links (portfolio, GitHub, deployed project, case study) and what they personally built or achieved, with real results if any.
7. **Sender name and links** to sign with (portfolio, GitHub, LinkedIn).

For a follow-up, also ask for the original email (or its subject and topic) and how many days ago it was sent.

If the user says "just give me a template", give the matching template from `references/templates.md` with placeholders, and list what they must fill in.

## Step 2: Pick the template

| Goal | Template in `references/templates.md` |
|------|------|
| Join a startup / reach a founder | 1 - Founder |
| Advertised internship or full-time role | 2 - Role application |
| Referral from an employee | 3 - Referral |
| Freelance / service client | 4 - Client pitch |
| LinkedIn / X / WhatsApp DM | 5 - Short DM |
| No reply yet | 6 - Follow-up |

Read `references/templates.md` and use the chosen template's structure. It is a guide, not a script: rewrite it in the user's own voice.

## Step 3: Write it with the formula

**Context + Relevance + Proof + A Small Ask**

- **Context** - why this person: one specific, true observation about their company, product or work. This is the line that shows the email isn't mass-sent.
- **Relevance** - connect the user's 1-2 most relevant skills to what the recipient is building or hiring for. Match the job description (backend role -> backend proof).
- **Proof** - one or two links that show real work. Show, don't claim.
- **Small ask** - exactly ONE easy question ("Are you open to bringing on developers?", "Would it help if I shared a few ideas?"). Never stack a job + referral + mentorship + call in one message.

Rules:
- **Length:** 80-150 words for emails (people read on phones; if it needs scrolling, it loses). DMs: 2-4 short lines, and under the platform limit (LinkedIn connection notes are ~200-300 characters).
- **Subject line:** direct, humble, relevant. Patterns: `Interested in building with [Company]`, `[Role] at [Company] | [Skill or Project]`, `An idea for [Product]`, `Quick question about [Role] at [Company]`. No clickbait, no sales slogans.
- Short paragraphs, plain words, working links.
- Sound like a person: no "esteemed organization", "Respected Sir", "I hope this email finds you well", "kindly revert", no filler or AI-sounding phrasing ("I'm thrilled", "leverage synergies", "delve").
- **Honesty:** never exaggerate the user's contribution, invent results, invent problems on a client's site, or promise revenue they can't back up. Everything must be something they can explain on a call.
- Attach or offer a resume only when it helps (role applications, referrals); include the job link for referrals so the helper doesn't have to search.

## Step 4: Self-check before showing it

Check the draft against this list and fix anything that fails:

- [ ] First line is a specific, true observation, not "I am looking for an internship"
- [ ] Only skills relevant to this recipient
- [ ] 1-2 proof links, no link dump
- [ ] Exactly one question/ask
- [ ] Within the word/character limit
- [ ] No placeholder left unfilled (or clearly marked if the user must fill it)
- [ ] Nothing invented or exaggerated

## Step 5: Deliver

Give the user:
1. The subject line (emails only) and the message, ready to copy.
2. One line on why it works and one line on what would make it stronger (e.g. a sharper observation, a deployed link instead of a repo).
3. The follow-up plan: first follow-up after 3-5 business days (Template 6), at most one final polite check-in later, then move on. Stop immediately if the person asks.

If the user is sending to many people, remind them: don't send the same message to everyone - personalize each Context line. 10 well-researched people beat 100 copy-pastes.

## When someone replies

Help the user respond:
- Asked for a resume -> send it promptly.
- Asked about experience -> answer directly with the single most relevant example.
- Offered a call -> propose 2-3 concrete time slots and prepare what to discuss.
- "Nothing right now" -> thank them warmly and keep the door open.
- No reply after follow-ups -> move on; don't rely on one person.

## Tracking (if the user asks, or is doing outreach at volume)

Offer a simple tracker with columns: person, company, channel, contact date, reason for reaching out, message version, follow-up date, response, outcome.

Metrics (keep the denominator = delivered messages for all three):
- **Reply rate** = replies / delivered
- **Positive reply rate** = interested or constructive replies / delivered
- **Outcome rate** = calls or interviews / delivered

Use them to compare message versions and targets, then adjust.

## If the user's proof is weak

The email earns attention; the proof earns credibility. If the user has nothing to link, say so kindly and suggest the fastest fix: build and deploy one useful project, solve a real problem and write up the approach, or contribute to an open-source project they understand. A portfolio item should answer: what was built, what problem it solves, what they personally did, can I see it working, and what evidence shows the result.
