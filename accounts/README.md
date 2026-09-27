# Accounts

One folder per lead or customer. The folder holds a `STATUS.md` (where things stand, who has the ball, the log) and the raw material: transcripts, emails and notes, verbatim, with the date in the filename.

| Folder | Who is in it |
|---|---|
| `leads/` | Open deals, not signed yet |
| `customers/` | Signed |
| `lost/` | Said no, or went quiet. Keep the folder: the lesson is in it. |
| `churned/` | Was a customer, stopped |

A folder moves at most once, when the deal closes. The finer stage (first call, proposal, negotiation) lives in `pipeline.md`.

To start one, copy `leads/_template/` to `leads/YYYY-MM-DD-<name>/` and fill in `STATUS.md`. The full rules are in `AGENTS.md`.
