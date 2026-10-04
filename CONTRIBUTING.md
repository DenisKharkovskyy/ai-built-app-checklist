# Contributing

Thanks for helping keep the checklist accurate. There are two ways to contribute:

- **[Suggest a new check](../../issues/new?template=new-check.yml):** a common problem in apps built with AI tools that the 24 checks don't cover.
- **[Suggest a correction](../../issues/new?template=correction.yml):** a wrong or outdated fact, a dashboard path that moved, a broken link, a SQL query or command that doesn't work, a severity you disagree with, or wording that isn't clear.

Please use an issue, not a pull request, for changes to the checklist text. The text is published on [selfoia.com/checklist](https://selfoia.com/checklist) first and mirrored here, so a merged pull request would be overwritten at the next sync. Pull requests that fix a typo or a broken link in this repo's own files (README, CONTRIBUTING) are welcome.

## Ground rules

1. **Never post secrets.** No API keys, tokens, passwords, connection strings, or URLs that contain tokens. If you pasted one by mistake, replace the key first: create a new key and delete the old one. Editing the issue isn't enough.
2. **No real user data.** No names, emails, screenshots of customer records or database rows.
3. **Your own apps only.** Don't report problems you found in someone else's app here, and don't test apps you don't own or don't have written permission to test. If you found a problem in someone else's app, tell its owner privately.
4. **Evidence for every fact.** Link a public source: official documentation, a peer-reviewed study, a public incident write-up, or a reproducible example on your own test project. A number needs its source and its scope: who or what was measured, how many, and when.
5. **Plain English.** The checklist is read by founders without a technical background. Say what a problem means for their users or their money.

## What makes a good new check

- It happens often in apps built with AI tools such as Lovable, Bolt, Cursor, Replit, v0, Base44 or Claude Code, not only in one app.
- It fits one of the five zones: Leaks, Break-ins, Money, Speed or Safety net.
- An owner can test it on their own app, safely, in about 2 minutes, or a coding agent can check it by reading the code without changing anything.
- It isn't already covered by one of E01–E24.

## How issues are reviewed

1. The maintainer reads every issue and may ask for more evidence. There's no fixed response time.
2. Accepted changes are made on selfoia.com first, then mirrored to this repo.
3. The version date changes, [CHANGELOG.md](CHANGELOG.md) gets an entry, and the issue is closed with a link to the release.
4. Declined suggestions are closed with a short reason.

## Versions

- Versions are dates. `CHECKLIST.md` and `SELF-TEST.md` start with `Version: YYYY-MM-DD`, the same date as on selfoia.com.
- Each version is a GitHub release tagged `vYYYY-MM-DD`, for example `v2026-09-27`.
- IDs are stable. An ID (E01, E02…) is never renumbered or reused. A new check gets the next free number.
- Each check has a default severity: Critical, High, Medium or Low. The real severity always depends on the app: what data it holds, whether it takes money, and how many users it has.

## License of contributions

The checklist is licensed under [CC BY 4.0](LICENSE). By contributing text, you agree that it's published under the same license.
