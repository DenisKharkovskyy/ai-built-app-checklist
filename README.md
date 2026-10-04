# The AI-built app checklist

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

**24 checks before your first paying users.**

These are 24 common problems in apps built with Lovable, Bolt, Cursor, Replit, v0, Base44 and Claude Code. They're grouped into five zones: Leaks, Break-ins, Money, Speed and Safety net. Each one comes with a self-test that takes about 2 minutes on your own app. No coding needed for most.

It is written for solo founders and teams of 1–3 people without a technical background. There are two versions: [SELF-TEST.md](SELF-TEST.md) for you, and [CHECKLIST.md](CHECKLIST.md) for your AI coding tool.

Version: 2026-09-27 · Human version: [selfoia.com/checklist](https://selfoia.com/checklist) · Agent version: [selfoia.com/checklist.md](https://selfoia.com/checklist.md)

## Use it in 60 seconds

**1. Let your AI tool run the checks.** Using Cursor or Claude Code? Paste this into the agent chat inside your project. It reads the checklist and reports back without changing anything.

```text
Read https://selfoia.com/checklist.md and run every check on this codebase. Don't change any code. For each item, report the ID, pass / fail / not sure, the file and line, and one plain-English sentence explaining it. Never print full secret values; show only the first 4 characters. Then list the failures, most serious first, and wait for my OK before fixing anything.
```

**2. Your tool can't open links?** Download [CHECKLIST.md](CHECKLIST.md) into your project folder and say "Use CHECKLIST.md" instead. Both prompts are in [PROMPT.md](PROMPT.md).

**3. Checking by hand?** Open [SELF-TEST.md](SELF-TEST.md). Every check has a 2-minute test you run on your own app.

### Before you start

- **Only test apps you own.** Never run these checks on someone else's app.
- **Use test accounts,** and Stripe's test mode for anything to do with payments.
- **Don't click admin actions or delete anything** on your live app while testing.
- **Passing all 24 doesn't mean your app is safe.** It means you've closed common gaps. A full review goes further.

## The 24 checks

Click an ID for its 2-minute test.

### Zone 1 · Leaks: "My keys or my users' data are visible"

| ID | Check | In plain English | Default severity |
|---|---|---|---|
| [E01](SELF-TEST.md#e01) | Secret keys shipped to the browser | Is my OpenAI key inside the app where anyone can grab it? | Critical |
| [E02](SELF-TEST.md#e02) | Database open to anyone | Is my database open to anyone? | Critical |
| [E03](SELF-TEST.md#e03) | Public file storage | Can anyone download our files? | High |
| [E04](SELF-TEST.md#e04) | Personal data sent to third parties | Could my app leak what users typed to the AI? | Medium |

### Zone 2 · Break-ins: "Someone can see or change other people's stuff"

| ID | Check | In plain English | Default severity |
|---|---|---|---|
| [E05](SELF-TEST.md#e05) | Users can reach other users' data (IDOR/BOLA) | Can users see each other's data? | Critical |
| [E06](SELF-TEST.md#e06) | Admin pages without server-side checks | Can anyone open my admin page? | Critical |
| [E07](SELF-TEST.md#e07) | Weak login protection | Can someone keep guessing passwords? | High |
| [E08](SELF-TEST.md#e08) | CSRF and SSRF | Can a link make my app do something I didn't mean? | High |

### Zone 3 · Money: "People get Pro for free" or "My AI bill exploded"

| ID | Check | In plain English | Default severity |
|---|---|---|---|
| [E09](SELF-TEST.md#e09) | Paid plan without a verified payment | Can someone get Pro without paying? | Critical |
| [E10](SELF-TEST.md#e10) | Prices and totals trusted from the browser | Could someone order something for a negative price? | High |
| [E11](SELF-TEST.md#e11) | AI features without limits (OWASP LLM10) | Could someone use my AI for free while I pay the bill? | Critical if public, High if login required |
| [E12](SELF-TEST.md#e12) | Prompt injection | Could my chatbot tell a user something it shouldn't? | High |
| [E13](SELF-TEST.md#e13) | AI costs not measured or wasted | Why do my AI costs grow faster than revenue? | Medium |

### Zone 4 · Speed: "It gets slow when more people use it"

| ID | Check | In plain English | Default severity |
|---|---|---|---|
| [E14](SELF-TEST.md#e14) | Slow database access | Why is it fast for me but slow with real data? | Medium to High |
| [E15](SELF-TEST.md#e15) | Heavy pages on phones | Why is the site slow on phones? | Medium |
| [E16](SELF-TEST.md#e16) | Content invisible to crawlers | Why don't Google and ChatGPT show my site? | Medium |
| [E17](SELF-TEST.md#e17) | Free-plan and launch-day limits | Why did it stop working on launch day? | Medium |

### Zone 5 · Safety net: "I find out it's broken from customers"

| ID | Check | In plain English | Default severity |
|---|---|---|---|
| [E18](SELF-TEST.md#e18) | No tested backups | If something deletes my data, is it gone for good? | High |
| [E19](SELF-TEST.md#e19) | AI tools with production access | Could my AI tool break my live app? | High |
| [E20](SELF-TEST.md#e20) | No monitoring or alerts | Why do I only find out it's broken when a customer tells me? | Medium |
| [E21](SELF-TEST.md#e21) | Risky or unknown packages | Did the AI add packages I've never heard of? | Medium |
| [E22](SELF-TEST.md#e22) | Code that breaks when changed | Why does every fix break something else? | Medium |
| [E23](SELF-TEST.md#e23) | Missing security headers | Is my site set up safely at all? | Low to Medium |
| [E24](SELF-TEST.md#e24) | Privacy basics | I have users in Europe. Is that a problem? | Medium |

**Severity:** **Critical:** a stranger could reach your users' data or your money right now. · **High:** a real risk that needs some effort, a login or a specific situation. · **Medium:** makes your app weaker, slower or more expensive. · **Low:** good practice. ([Full definitions](https://selfoia.com/vibe-code-audit#severity))

## What's in this repo

| File | What it is |
|---|---|
| [CHECKLIST.md](CHECKLIST.md) | The checklist for AI coding agents. Same text as [selfoia.com/checklist.md](https://selfoia.com/checklist.md). |
| [SELF-TEST.md](SELF-TEST.md) | The human version, with a 2-minute self-test per check. Same content as [selfoia.com/checklist](https://selfoia.com/checklist). |
| [PROMPT.md](PROMPT.md) | The copy-paste prompts for your AI coding tool. |
| [CHANGELOG.md](CHANGELOG.md) | What changed in each version. |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to suggest a new check or a correction. |
| [LICENSE](LICENSE) | Creative Commons Attribution 4.0 International (CC BY 4.0). |

The canonical versions live on [selfoia.com](https://selfoia.com/checklist). This repo mirrors them: when the version date changes on the site, the files here are updated and the release is tagged `vYYYY-MM-DD`.

## Rather have a person look?

Send us your app. Within 2 business days you get a written reply: the three biggest risks anyone can see from outside, and which of your scanner's warnings are real. Free, no call needed.

**[Get a free check](https://selfoia.com/free-check)**

## Contributing

Found a mistake, an outdated step or a common problem that isn't covered? Open an issue with your evidence. Never post secrets, real user data or problems you found in someone else's app. Details: [CONTRIBUTING.md](CONTRIBUTING.md).

## License and attribution

The checklist, including the SQL queries and other code snippets in it, is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) by SELFOIA S.R.L. You may copy, share, translate and adapt it, also commercially, as long as you give credit, link to the license and say if you changed anything.

Credit it as:

> SELFOIA — https://selfoia.com/checklist

For example:

> Based on "The AI-built app checklist" by SELFOIA — https://selfoia.com/checklist, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Changes: [what you changed, or "none"].

## Maintained by SELFOIA

SELFOIA is a software engineering company in Bucharest, Romania. We review, fix and speed up apps that founders built with AI tools like Lovable, Bolt, Cursor, Replit, v0, Base44 and Claude Code, so they don't leak, break or burn money as they grow. SELFOIA S.R.L. is led by [Denys Kharkovskyy](https://selfoia.com/team/denys-kharkovskyy), founder and lead engineer.

[selfoia.com](https://selfoia.com) · [Free check](https://selfoia.com/free-check)

Not affiliated with Lovable, Bolt, Replit, Cursor, Vercel or Supabase.
