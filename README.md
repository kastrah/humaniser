# Humaniser

A skill with two modes: remove AI writing patterns from any text, and review customer-facing messages against the REMI framework before they go out.

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
Identifies and rewrites AI-generated text to sound natural and human. Based on Wikipedia's "Signs of AI writing" guide. Detects 50+ patterns across content, language, style, and communication, then runs a final audit pass to catch anything that still reads as obviously machine-generated.

### Messaging Review (REMI)
Evaluates any outbound or inbound message against four principles:

- **R — Real:** Does it sound like a person, or a brand?
- **E — Expectation-first:** Does the reader know what happens next and when?
- **M — More than the ask:** Did it give something useful before asking for anything?
- **I — Invite dialogue:** Does the ending create a reason to reply?

Returns a pass/fail per principle with a one-line fix direction. No rewrites — just clear, actionable feedback.

## References

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [REMI Framework](./REMI_FRAMEWORK.md) — full specification

## Version History

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
