# Playbooks

Work you repeat, written down once. A proposal email, an onboarding, a workshop day, a monthly report: anything you have done three times the same way.

## Why

The third time you write the same kind of email, you are rewriting something that already exists somewhere in your sent folder. The best version is buried in an old thread. A playbook digs it up once and keeps it where your agent can find it.

## How a playbook looks

One folder per recurring process:

```
playbooks/
  <process-name>/
    README.md        the chain: which steps, when each happens, what must never be missing
    01-<step>.md     template for step one, with [PLACEHOLDERS]
    02-<step>.md     ...
```

## Making one

Do not write templates from scratch. Ask your agent:

> Find every email I sent for [process] in the account folders. Keep what worked, drop the rest, and turn it into a playbook in playbooks/[process-name]/ using the template.

Then read it and fix what is not you.

## Rules

- **No prices in templates.** They come from `knowledge/pricing.md` when you use the template. Prices change; templates should not have to.
- **Link the real examples** the playbook was built from, so you can check what it was based on.
- **List the ingredients that must never be missing** in the README. That list is where most of the value is.
- **Update the playbook when you improve a real email.** The playbook is the best version so far, not a frozen one.

Start from `_template/`.
