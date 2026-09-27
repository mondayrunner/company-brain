# Company Brain — instructions for the agent

This folder is the company's memory. Markdown is the truth. Answer from these files, cite the file you used, and say so when the brain does not know.

## Where every answer lives

**One home per fact. Link to it, never copy it.** Any other place a fact appears is not canon.

| Question | Source |
|---|---|
| Company details (legal name, registration, VAT, bank, accountant) | `company.md` |
| Who we are for, who we are not for | `knowledge/positioning.md` |
| Prices, packages, rates | `knowledge/pricing.md` |
| Where money figures live, loans, fixed commitments, money rules | `knowledge/finance.md` |
| Voice, words, colours, fonts | `knowledge/brand.md` |
| What we want and what we do not (read before advising) | `knowledge/compass.md` |
| Open questions, and what we decided, when and why | `knowledge/decisions.md` |
| Status of one lead or customer | `accounts/<side>/<name>/STATUS.md` |
| All open deals, who has the ball | `pipeline.md` |
| Partners, suppliers, network (not leads or customers) | `contacts/<name>.md` |
| Terms, contract templates, privacy | `legal/` |
| How we do recurring work (emails, onboarding, delivery) | `playbooks/<name>/` |
| Map of all knowledge | `knowledge/INDEX.md` |

Documents with a `⚠️ SUPERSEDED` banner are history, not advice.

## Rules

- **Anything outward-facing is a proposal.** Sending an email, publishing a post, sending an invoice, booking a meeting or deleting something waits for a human who has seen the final version and said yes. Any change after that, even a typo fix, resets the yes.
- **Never copy a number a system already knows.** Revenue lives in the payment provider, tasks on the board, meetings in the calendar. Ask the source or say you cannot see it. A copied figure is wrong the day after you paste it.
- **Never quote a price from memory or from an old proposal.** Only from `knowledge/pricing.md`.
- **Write in the voice from `knowledge/brand.md`** whenever you draft something that leaves the building.
- **Log decisions.** When the human decides something that changes how the company works, add a dated line to `knowledge/decisions.md` with the reason. If it answers an open question, move that question from **Open** into the log. Offer to do it; do not skip it.
- **Supersede, do not silently overwrite.** When a document stops being true, add a `⚠️ SUPERSEDED — see <file>` banner at the top and link to what replaced it.

## Keeping the brain fresh (drift)

Every canon file has frontmatter with `last_verified: YYYY-MM-DD`.

- Older than 60 days: say so when you answer from it, and ask whether it still holds.
- When the human confirms or updates it, set `last_verified` to today.
- When asked to "walk the brain": list stale files, facts that appear in two places, links that point nowhere, accounts whose status file is older than the last contact, and pipeline rows that disagree with account folders. Propose fixes; change nothing until the human agrees.

## Accounts

- A new lead: copy `accounts/leads/_template/` to `accounts/leads/YYYY-MM-DD-<name>/` and fill `STATUS.md`.
- Every status file has a `**Ball with:**` line. Keep it true; it is the most-asked question.
- **Folders are the side, the pipeline is the stage.** `accounts/` has four sides: `leads/` (open), `customers/` (signed), `lost/` (no, or went quiet), `churned/` (was a customer, stopped). A folder moves at most once per deal, when it closes. The fine stage (first call, proposal, negotiation) changes often and lives as a row in `pipeline.md`, so links to the folder never break.
- Raw material (transcripts, notes, pasted emails) goes in the account folder, verbatim, with the date in the filename.
- Unfiled transcripts wait in `transcripts/_inbox/`. File them into the right account when you know who it was with.

## Playbooks

Work that repeats becomes a playbook. The trigger: the third time the human writes the same kind of email or runs the same kind of process, propose one.

- A playbook is a folder in `playbooks/` with a `README.md` (the chain of steps, when each happens, the ingredients that must never be missing) and one template file per step.
- Build templates from the human's best real examples, not from scratch. Link to those examples in the README.
- Templates contain `[PLACEHOLDERS]`, never prices. Prices come from `knowledge/pricing.md` at the moment of use.
- To use a playbook: copy the template into the account folder, fill it, and hand it to the human to send.
