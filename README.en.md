# Say it once

Structure Forge turns a chat where you finally got the format right into a note you can reuse.

[简体中文](README.md) · English · [Usage guide](USAGE.md) · [Full example](examples/weekly-report.md) · [Skill file](SKILL.md)

The note is plain text. Copy it. Send it to any AI. That's it.

## Why this exists

Last week it took fourteen messages to get a weekly report right. Five parts. Risks in their own section, before next week's plan. No polite opening. Unfinished work marked [in progress].

This week, a new topic. Fourteen more messages.

You can't describe the format. You just know when it's wrong. "No, not like that." "Try again."

The format never left that chat. Close the window and it's gone. It's like repeating "no sugar, oat milk, extra hot" to every new barista. You don't need better words. You need the order written down.

## What happens

Paste the chat log. That's the only real work.

It reads the log and works out the parts, their names, and their order. You don't have to explain any of it. It asks 3–5 small questions, one at a time. Each comes with options and a recommended answer. "Use the recommended" is enough. Skip a question and it uses the recommended one, then labels it as a guess.

Then you get the note. The format, the things it must not write, and a short checklist it runs on its own.

Next time, keep every line. Change the last two.

## A slice of one run

```
You:  Save this format. Here's the chat where it finally worked.
      (paste the log)

It:   Five parts: Title / Done this week / Risks / Next week / Notes.
      I'll use this. [1 of 3, recommended: keep]
You:  ok

It:   You said no polite openings, no "Overall...", no invented numbers.
      I've made those three rules. [2 of 3, recommended: keep all]
You:  keep all

It:   Unfinished work gets [in progress]? [3 of 3, recommended: yes]
You:  yes

It:   Checked the order. Headings unchanged. Here's the note.
```

```
Write a weekly report with exactly these 5 parts, in this order:
  1. Title   2. Done this week   3. Risks   4. Next week   5. Notes

No polite openings. No sentences starting with "Overall...".
No numbers without a source. Mark unfinished work [in progress].
Check before finishing: all 5 parts? headings changed? any invented numbers?

## Fill in for this run
Topic: Q4 review
Done this week: ...
```

## What you actually have to do

Almost nothing. Paste the material. The questions come with answers attached, and skipping is fine. It checks the format itself, uses the strictest wording by default, and runs its own checklist. If something looks wrong, say one sentence and it goes back to that bit. The guide calls these steps S0 to S5.

It won't write a "quick first draft" before you've seen the format. Anything you skipped is marked as a guess, not "agreed". If you're in a hurry, say "stop asking" and it finishes with the recommended answers, still marking the guesses.

## What's on the note

Eleven small blocks. They cover five things: what the note is for, the exact format, what not to write, how to check, and what to do when something's missing. The headings are English, but there's nothing to memorise: `Purpose`, `Context`, `Task`, `Format`, `Constraints`, `Prohibited`, `Gold Standard`, `Self-Check`, `Fallback`, `Rule Priority`, `Non-Goals`.

At the end there's a `## Fill in for this run` block. That's the only part that changes.

Ask an AI to write you a prompt and you have to describe the format yourself. Here it comes out of the chat log. Even your "no, not like that" becomes a rule.

## Install and use

One file, once:

```bash
mkdir -p ~/.workbuddy/skills/structure-forge
cp SKILL.md ~/.workbuddy/skills/structure-forge/SKILL.md
```

Restart the session. Say "save this format" and paste the chat. Later, send the note to any AI and edit the last two lines.

Step-by-step detail is in the [usage guide](USAGE.md). The whole conversation and the full note are in the [full example](examples/weekly-report.md). Both are Chinese for now.

## Questions

**I can't write prompts.** Good, you don't need to. Paste a chat log, reply "use the recommended".

**How many questions?** 3–5. One at a time. All with a recommended answer. Skipping is fine.

**Another AI?** Yes. Plain text works anywhere.

**What if it guessed wrong?** Say "drop part three" when it shows you the format. The note is text too, so you can just edit it.

## Where it falls short

It won't be identical every time. The checklist helps the AI catch its own mistakes, but you still want to look at the result.

There are no built-in industry rules for medical, legal or financial work. It writes text. It doesn't fetch data, run code, or send messages. This repo holds instructions and docs, not software; you need an AI tool that can load `SKILL.md`.

```
structure-forge-skill/
├── SKILL.md              the only file you install
├── README.md             Chinese overview
├── README.en.md          this file
├── USAGE.md              usage guide (Chinese)
├── examples/
│   └── weekly-report.md  one full run (Chinese)
└── LICENSE               MIT
```

MIT — see [LICENSE](LICENSE).
