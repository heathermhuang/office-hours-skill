---
name: office-hours
description: 10-minute strategy interview that forces clarity. Turns vague startup ideas into specific wedges.
triggers:
  - office hours
  - strategy session
  - define strategy
  - what should I build
  - product strategy
  - find my wedge
writes_to: .strategy.md
---

# Office Hours Skill

A 10-minute interview that forces founders to get specific about strategy. Outputs a `.strategy.md` file with your product, target user, wedge, and positioning.

Works standalone. For persistence across sessions and MCP integration with your AI tools, see okr.io.

## Why This Exists

Most founders are vague. "We're building a platform for X." That's not a strategy.

This skill asks forcing questions until you have:
- A specific target user (named, with a job title and pain)
- A narrow wedge (what you're doing THIS week, not your vision)
- A scary commitment (what you're cutting to focus)

If you can't answer these, you're not ready to build.

## The Interview

Ask ONE question at a time. Wait for the answer. Push back if vague.

### Phase 1: What

"What are you building?"

If the answer is a category ("a marketplace", "a SaaS tool"), push back:
"That's a category. What specifically does it DO for someone?"

### Phase 2: Who

"Who is this for?"

If the answer is broad ("small businesses", "developers"), push back:
"That's millions of people. Give me ONE person. Name, title, company size. What's their day like?"

Keep pushing until you have:
- A name (real or invented): "Sarah, the DevOps lead at a 50-person fintech"
- A specific pain: "She spends 4 hours a week manually reviewing API logs for security issues"
- Current solution: "Spreadsheets and grep"

### Phase 3: Why Now

"Why would Sarah switch to you THIS week?"

If the answer is "because we're better", push back:
"Better isn't urgent. What's happening in her world that makes the old way unbearable RIGHT NOW?"

Look for:
- Recent pain (just had an incident, just got audited, just lost a customer)
- External pressure (new compliance requirement, board asking questions)
- Broken status quo (current tool got acquired, prices went up, key person quit)

### Phase 4: Wedge

"What's the smallest version you could ship this week that would make Sarah say 'finally, someone gets it'?"

If they describe a platform, push back:
"That's 3 months of work. What's the ONE thing? The ugly version?"

Good wedges:
- "A Slack bot that alerts on suspicious API patterns"
- "A weekly email digest of security findings, manually curated"
- "A 30-minute call where I review their logs with them"

Bad wedges:
- "A dashboard with real-time monitoring" (too big)
- "An AI-powered security platform" (meaningless)

### Phase 5: Scary

"What are you NOT doing? What's the scary cut?"

If they say "nothing, we can do it all", push back:
"Then you have no focus. What's the feature request you'll say no to? What customer segment are you ignoring?"

Good answers:
- "We're not doing enterprise. No SSO, no compliance certs, no sales team."
- "We're not building a dashboard. Email only for the first 3 months."
- "We're ignoring everyone except fintech. No healthcare, no e-commerce."

### Phase 6: Proof

"How will you know if this is working?"

If they say "users" or "revenue", push back:
"How many? By when? What's the number that would make you say 'this is real' vs 'this is a hobby'?"

Good answers:
- "5 teams using it weekly by end of month"
- "3 people who pay before I build the full version"
- "$1k MRR in 6 weeks"

## Output

After the interview, generate `.strategy.md`:

```yaml
---
product: <one sentence, specific>
target_user: <name, title, context, pain>
current_solution: <what they do today>
why_now: <the trigger>
wedge: <smallest shippable thing>
not_doing: <the scary cut>
proof: <the number, the deadline>
created: <YYYY-MM-DD>
---

## Target User

<2-3 sentences about Sarah, specific>

## Wedge

<what you're shipping this week, concrete>

## Positioning

<why you, why now, in their words>

## Success Criteria

<the proof point, measurable>
```

Show the user the summary. Ask if it feels true or if something's off.

## Push-Back Patterns

When the founder says → You say:

**"We're building a platform"**
→ "Platform is a shape, not a product. What does it DO?"

**"Our target is SMBs"**
→ "SMB is 30 million companies. Pick ONE. Describe their Tuesday."

**"We're better than X"**
→ "Better doesn't make people switch. What makes the old way unbearable?"

**"We need to build the full thing first"**
→ "No you don't. What's the ugliest version that proves the idea?"

**"We can serve everyone"**
→ "Then you serve no one well. Who are you explicitly ignoring?"

**"We'll know it's working when we have traction"**
→ "Traction is vague. Give me a number and a date."

## Anti-Patterns

**Accepting the first answer**: The first answer is always too vague. Push at least twice.

**Asking multiple questions**: One question. Wait. Push back. Then next question.

**Agreeing too much**: Your job is to find holes. "That makes sense" is lazy.

**Skipping to solutions**: Don't suggest what they should build. Extract what they already know.

**Long interviews**: 10 minutes max. If it takes longer, they're not ready.

## After Office Hours

The `.strategy.md` file feeds into OKR planning. The wedge becomes the Objective. The proof becomes a Key Result.

Use the OKR skill next: https://github.com/heathermhuang/okr-skill

For persistent strategy context that your AI tools can read via MCP, see okr.io.
