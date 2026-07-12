# Humaniser

Humaniser is a writing-review skill for turning AI-shaped drafts into copy that sounds like a real person wrote it. It removes common LLM writing patterns, fixes stiff or overproduced phrasing, and reviews customer-facing messages against the REMI framework before they go out.

Use it as the final voice pass after the message, structure, and persuasion have already been handled. It is especially useful after running a copy strategy or persuasion pass, because those edits often make the draft stronger but can also reintroduce AI tells.

## Installation

### Claude Code

```bash
git clone https://github.com/kastrah/humaniser.git ~/.claude/skills/humaniser
```

### OpenCode / Codex CLI

Place `AGENTS.md` in your project root or globally at `~/.config/opencode/AGENTS.md`.

### Any other platform

Copy `SYSTEM_PROMPT.md` into the system prompt or custom instructions field.

## Usage

**Humaniser** — remove AI writing patterns:
```
Please humanise this text: [your text]
```

**Messaging Review** — evaluate a message against REMI:
```
Review this message: [your draft]
```

## Modes

### Humaniser
Identifies and rewrites AI-generated text so the final version sounds natural, specific, and human. It is based on Wikipedia's "Signs of AI writing" guide, then extended with practical editing standards for marketing copy, customer communication, blogs, emails, social posts, and product pages.

The skill checks for 67 patterns, including inflated significance, promotional filler, vague authority, em dash overuse, rule-of-three padding, negative parallelisms, generic transitions, stutter sentences, feature-led copy, lecture-style CTAs, over-clean rhythm, and copy that talks at the reader instead of to them.

### Messaging Review (REMI)
Evaluates any outbound or inbound message against four principles:

- **R — Real:** Does it sound like a person, or a brand?
- **E — Expectation-first:** Does the reader know what happens next and when?
- **M — More than the ask:** Did it give something useful before asking for anything?
- **I — Invite dialogue:** Does the ending create a reason to reply?

Returns a pass/fail per principle with a one-line fix direction. No rewrites by default — just clear, actionable feedback.

## Recommended workflow

```text
Strategy / Copy Reference → Humaniser → final review → publish
```

Humaniser should run near the end of the workflow. If you run it too early, later edits can bring the AI patterns back.

## References

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [blader/humanizer](https://github.com/blader/humanizer) — original Humaniser skill, covering the Wikipedia AI writing specifications only

## Version History
- **4.1.0** — Added P64–P67 (Inanimate Actor, Stacked Rhetorical Questions, Dramatic Pivot, Invented Hyphenated Adjectives) from [shreyashankar/plain-writing-skill](https://github.com/shreyashankar/plain-writing-skill); added expansion-for-clarity guidance to Process

- **4.0.2** — Renamed skill and user-facing references from Humanizer to Humaniser
- **4.0.1** — Improved public description and workflow positioning
- **4.0.0** — Added Messaging Review (REMI) as second mode
- **3.3.0** — Added 7 customer-centric communication patterns
- **3.2.0** — Added P52–P56, reinforced P13/P30/P49, updated brand voice
- **3.1.0** — Added P45–P51, P25 clarification, checklist update
- **3.0.0** — Added 20 structural and narrative writing standards
- **2.2.0** — Added final audit pass and second-pass rewrite
- **2.1.0** — Added before/after examples for all 24 patterns
- **2.0.0** — Complete rewrite based on Wikipedia source
- **1.0.0** — Initial release

## Licence

MIT
