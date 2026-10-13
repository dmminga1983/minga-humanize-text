# minga-humanize-text

Claude Code skill that strips the "AI smell" out of a finished text — descriptions, tags, reels, lyrics, tables/reports, conversational scripts — before it goes out for publishing or voice-over.

It's a final polish pass, run *after* the content itself (facts, structure, meaning) is already done — not a replacement for writing.

## What it catches

A two-pass diagnostic across five pattern groups:

- **Content patterns** — phantom sources ("according to studies" with no study), vague generalizations, empty praise, overstated significance, wishy-washy "on one hand / on the other" with no actual position
- **AI vocabulary** — filler intros ("in today's world", "it's worth noting"), inflated nouns/verbs ("ecosystem", "unlock the potential", "seamless"), excessive intensifiers, "this isn't just X, it's Y" constructions
- **Style patterns** — too-even paragraph lengths, the "rule of three" examples where two or four would read more naturally, overused dashes, decorative emoji, suspiciously polished rhythm
- **Structural patterns** — "in this article we'll cover..." openers, "thus we can conclude" closers, headings that just restate the prompt
- **Communication patterns** — servile sign-offs ("let me know if you have questions"), hedge-disclaimers, apologizing before a direct criticism

If a paragraph hits 2+ markers, it gets rewritten whole rather than patched line by line.

Format-specific notes are included for reel/post captions and tags, song lyrics, tables and management reports, and spoken/voice-over scripts — each has its own version of "sounds human."

If the user's own writing-style profile is already saved, the skill leans on that voice first; otherwise it falls back to the general principles above.

## Install

Copy `SKILL.md` into your skills folder:

```bash
mkdir -p ~/.claude/skills/minga-humanize-text
curl -fsSL https://raw.githubusercontent.com/dmminga1983/minga-humanize-text/main/SKILL.md -o ~/.claude/skills/minga-humanize-text/SKILL.md
```

(Or just download this repo and drop `SKILL.md` into `~/.claude/skills/minga-humanize-text/` yourself.) Claude Code picks it up automatically next session — no restart, no config, nothing to enable.

## License

Free and open-source for any purpose — [MIT License](./LICENSE).

## Like it?

A ⭐ on the repo is the simplest way to tell me it's useful.
