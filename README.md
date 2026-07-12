# humaniser

humaniser is a writing-review skill for turning AI-shaped drafts into copy that sounds like a real person wrote it. It removes common LLM writing patterns and fixes stiff or overproduced phrasing.

It identifies and rewrites AI-generated text so the final version sounds natural, specific, and human. Based on Wikipedia's "Signs of AI writing" guide, then extended with practical editing standards for marketing copy, customer communication, blogs, emails, social posts, and product pages.

The skill checks for 74 patterns, including inflated significance, promotional filler, vague authority, em dash overuse, rule-of-three padding, negative parallelisms, generic transitions, stutter sentences, feature-led copy, lecture-style CTAs, over-clean rhythm, permission phrases, single-sentence-per-line cadence, and copy that talks at the reader instead of to them.

Use it as the final voice pass after the message, structure, and persuasion have already been handled. It is especially useful after running a copy strategy or persuasion pass, because those edits often make the draft stronger but can also reintroduce AI tells.

## How it fits with other tools

This tool is part of a three-skill writing stack. Each tool does one job well.

| Tool | What it does | When to use it |
|------|-------------|----------------|
| [copy-pass](https://github.com/kastrah/copy-pass) | Strengthens persuasion: hooks, CTAs, objections, emotional triggers, platform fit | Before a senior writer reviews copy. Not for final cleanup. |
| [care-review](https://github.com/kastrah/care-review) | Checks whether a message is conversational, actionable, richer than asked, and ends with a reason to reply | Before any customer-facing message goes out. |
| humaniser | Removes AI writing patterns and makes text sound natural | After copy pass. Final voice pass before publishing. |

### If you are on humaniser but need something else

- **Your copy needs stronger hooks, CTAs, or persuasion structure** → use [copy-pass](https://github.com/kastrah/copy-pass)
- **You are writing an email, SMS, WhatsApp message, or complaint response** → use [care-review](https://github.com/kastrah/care-review)
- **You are writing a blog, landing page, or article** → start with [copy-pass](https://github.com/kastrah/copy-pass), then come back here

## Recommended workflow

```text
Content for a general audience:
Research → Draft → copy-pass → humaniser → final review → publish

Messages for a specific person:
Draft → care-review → revise → send
```

humaniser should run near the end of the content workflow. If you run it too early, later edits can bring the AI patterns back.

## Usage

```
Please humanise this text: [your text]
```

## Installation

### Claude Code

```bash
git clone https://github.com/kastrah/humaniser.git ~/.claude/skills/humaniser
```

### OpenCode / Codex CLI

Place `AGENTS.md` in your project root or globally at `~/.config/opencode/AGENTS.md`.

### Any other platform

Copy `SYSTEM_PROMPT.md` into the system prompt or custom instructions field.

## References

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [blader/humanizer](https://github.com/blader/humanizer) — original humaniser skill, covering the Wikipedia AI writing specifications only

## Licence

MIT
