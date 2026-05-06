# Office Hours Skill

A 10-minute strategy interview for AI coding agents. Forces founders to get specific about product, target user, and wedge.

Works with Claude Code, Cursor, Codex, or any agent that can read a skill file.

## What It Does

Asks forcing questions until you have:
- A specific target user (named, with pain)
- A narrow wedge (what you're shipping THIS week)
- A scary cut (what you're NOT doing)
- A proof point (number + deadline)

Outputs a `.strategy.md` file.

## Install

Copy this folder to your repo, then tell your agent:

```
Follow ./office-hours-skill/SKILL.md to run Office Hours.
```

Or reference it in your system prompt.

## Usage

```
Run Office Hours for my project.
```

```
I need help figuring out my strategy.
```

```
What should I build first?
```

## The Flow

1. **What** - What are you building? (Push past categories)
2. **Who** - Who is this for? (Push to a named person)
3. **Why Now** - Why would they switch this week? (Find the trigger)
4. **Wedge** - Smallest shippable thing? (Push past platforms)
5. **Scary** - What are you NOT doing? (Find the focus)
6. **Proof** - How will you know it's working? (Get a number)

## Example Output

```yaml
---
product: API security monitoring that catches auth abuse patterns
target_user: Sarah, DevOps lead at 50-person fintech, spends 4hrs/week on manual log review
current_solution: grep + spreadsheets + prayer
why_now: Just failed a SOC2 audit, board asking questions
wedge: Weekly email digest of suspicious API patterns, manually reviewed
not_doing: No dashboard, no real-time alerts, no enterprise features
proof: 5 teams using weekly by May 30
created: 2026-05-06
---
```

## Then What

Use the [OKR skill](https://github.com/heathermhuang/okr-skill) to turn your strategy into measurable Key Results.

For persistent strategy context across AI sessions, see [okr.io](https://okr.io).

## License

MIT
