# Playbooks

A playbook is work you repeat, written down once. Think of a proposal email, an onboarding, a workshop day or a monthly report: anything you have done three times the same way.

## Why

The third time you write the same kind of email, you are rewriting something that already exists somewhere in your sent folder. The best version is buried in an old thread. With a playbook you dig it up once and keep it where your agent can find it.

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

- **No prices in templates.** Prices come from `knowledge/pricing.md` when you use the template. That way a price change does not mean editing every template.
- **Link the real examples** the playbook was built from, so you can check what it was based on.
- **List the ingredients that must never be missing** in the README. Most of the value is in that list.
- **Update the playbook when you improve a real email.** The playbook holds your best version so far and keeps improving.

Start from `_template/`.
