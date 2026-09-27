# Company Brain

**An empty company brain in plain markdown.** Clone it, fill it, and let your AI agent (Claude Code, Cursor, Codex, or anything that reads project instructions) answer from it.

You need no app, database or vendor. It is folders of markdown and one instruction file that tells your agent where every fact lives.

## Why

Your company already has a brain. It is spread over your head, your mailbox, old proposals and a dozen tools. Ask an agent a question about your business and it guesses, because it cannot see any of that.

A company brain fixes that with three habits:

1. **Every fact has one home.** Prices live in one file. Positioning in one file. A customer's status in one file. Everything else links there. A copy starts ageing the moment you make it.
2. **Decisions are written down with their reason.** Six months from now, "why did we stop doing X?" has an answer.
3. **Work you repeat becomes a playbook.** The third time you write the same kind of email, it becomes a template in the brain. Next time you fill in names and dates.

## The one problem you will hit: drift

A brain goes stale on its own. A price changes, a deal moves, a decision gets reversed, and the markdown still says the old thing. An outdated brain is worse than none, because your agent answers confidently from last quarter.

So the brain has rules against drift (see `AGENTS.md`):

- Canon files carry a `last_verified` date. Older than 60 days means: check before you trust.
- Numbers that live in a system (revenue in your payment provider, tasks in your board) are never copied into markdown. The agent asks the source.
- Superseded documents get a banner instead of being silently wrong.
- Once a week, ask your agent: *"Walk the brain. What is stale, duplicated or contradicting?"*

The brain works without any software. If you want the checks automated (an index, drift checks on a schedule, MCP tools for your agent), use the engine: [company-os](https://github.com/mondayrunner/company-os).

## What is in here

```
AGENTS.md                 the rules your agent follows, and where every answer lives
CLAUDE.md                 one line that points Claude Code to AGENTS.md
company.md                legal name, registration, address, bank, accountant
knowledge/
  README.md               map: which file answers which question
  positioning.md          who you are for, who you are not for, the objections you hear
  pricing.md              the one place prices live
  finance.md              scorecard, loans, commitments, money rules; never the figures themselves
  brand.md                voice, words, colours, fonts
  team.md                 who does what, including your agents
  compass.md              what you want, what you do not; steers every piece of advice
  decisions.md            open questions on top, dated decisions and their reason below
accounts/                 one folder per lead or customer, sorted by side
  leads/                  open deals; copy _template/ per lead
  customers/              signed
  lost/                   said no or went quiet; the lesson stays
  churned/                was a customer, stopped
pipeline.md               every open deal, who has the ball, next action
contacts/                 partners, suppliers, network: people who are not accounts
legal/                    terms, contract templates, privacy statement
playbooks/
  README.md               how a playbook works
  _template/              copy this to start a new one
  example-workshop-day/   a filled-in example
transcripts/_inbox/       raw call notes and recordings waiting to be filed
```

Every folder has a `README.md` that says what goes in it.

## Quickstart

```bash
git clone https://github.com/mondayrunner/company-brain.git my-brain
cd my-brain
rm -rf .git && git init          # it is your brain now, keep it private
```

Then open your agent in that folder and say:

> Read AGENTS.md. Interview me to fill company.md, knowledge/positioning.md and knowledge/pricing.md. One question at a time.

Twenty minutes later your agent can answer the basics. Fill the rest in this order, each as its own conversation:

1. **`company.md`**: the facts on your invoice. This takes five minutes.
2. **`positioning.md`** and **`pricing.md`**: who you are for and what it costs. Your agent gets asked these two things most.
3. **`brand.md`**: paste three texts you are proud of and let your agent describe your voice. From then on its drafts sound like you.
4. **`compass.md`**: start with the anti-vision, the Tuesday you do not want. Ask your agent to interview you; it is easier to answer questions than to face an empty page.
5. **`decisions.md`**: list the open questions you are carrying around. When one is decided, it moves to the log with the date and the reason.
6. **`finance.md`** and **`team.md`**: the numbers you watch and where they live, your fixed commitments, and who (or which agent) does what.
7. **Accounts**: one folder per open lead or customer, copied from `_template`. Paste in what you have (emails, notes) and let your agent write the status.
8. **Playbooks**: skip these for now. Make one when you notice you are writing something for the third time.

After that, feed the brain as you work:

- After a call, paste the transcript and ask your agent to update the account.
- After a decision, ask it to log the decision.
- When you write the same email a third time, ask it to make a playbook.

**Keep your own brain private.** This template is public, but your filled-in copy contains customers, prices and decisions.

## Related

- [company-os](https://github.com/mondayrunner/company-os): the engine that indexes, checks and serves a brain like this one.
- [compounding-sales](https://github.com/mondayrunner/compounding-sales): a deeper sales module (call reviews, anti-patterns) that fits in `accounts/`.

## License

MIT
