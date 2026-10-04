# Let your AI tool run the checks

Source: https://selfoia.com/checklist · Version: 2026-09-27 · Maintained by SELFOIA (https://selfoia.com)

Using Cursor or Claude Code? Paste this into the agent chat inside your project. It reads the checklist and reports back without changing anything.

```text
Read https://selfoia.com/checklist.md and run every check on this codebase. Don't change any code. For each item, report the ID, pass / fail / not sure, the file and line, and one plain-English sentence explaining it. Never print full secret values; show only the first 4 characters. Then list the failures, most serious first, and wait for my OK before fixing anything.
```

## Your tool can't open links?

Download [CHECKLIST.md](CHECKLIST.md) into your project folder and say "Use CHECKLIST.md" instead:

```text
Use CHECKLIST.md and run every check on this codebase. Don't change any code. For each item, report the ID, pass / fail / not sure, the file and line, and one plain-English sentence explaining it. Never print full secret values; show only the first 4 characters. Then list the failures, most serious first, and wait for my OK before fixing anything.
```

## What you get back

[CHECKLIST.md](CHECKLIST.md) tells the agent to work read-only on your project only, to start its report with a table (ID, check, result, where, a plain-English note) and to list the failures most serious first. It ends with: "This is an automated self-check, not a security review. For a human review, see https://selfoia.com/free-check."

Found a leaked key? Replace it first: create a new key and delete the old one.

Prefer to check by hand? Every item has a 2-minute test in [SELF-TEST.md](SELF-TEST.md).
