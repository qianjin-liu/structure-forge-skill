# Structure Forge — Explain it once. Reuse it forever.

**Turn the format you spent half an hour explaining to an AI into a small note you can reuse.**

**English** · [简体中文](README.md) · [Usage guide](USAGE.md) (Chinese) · [Full example](examples/weekly-report.md) (Chinese) · [Skill file](SKILL.md)

> The "note" is just plain text. Copy it, send it to any AI, and the AI knows what to write.
> No plugin, no internet, no new concepts to learn. The skill file calls it a *structure spec* — same thing.

---

## Sound familiar?

You go back and forth with an AI a dozen times. Finally it gets it right: how many sections, what goes in each, where to stop waffling. You're happy.

The next day, with a new topic, you explain it all over again.

And the annoying part: you can't actually **say what that format is**. You can only get there by giving examples, correcting it, and saying "no, not like that."

Why? Because that format **only ever lived inside that one chat**. Close the window and it's gone.

Think of a regular coffee order. Every time a new barista is on, you repeat "no sugar, oat milk, extra hot." You don't need better words — you need a little card with the order written on it.

**This skill writes that card for you.**

---

## What it actually does

You paste in the chat log (or one output you liked). It does three things:

1. **It reads first.** From the conversation, it works out how many parts the format has, what each part is called, and in what order. You don't have to describe it. Not being able to describe it is fine.
2. **It asks a few very easy questions.** 3–5 of them, one at a time, each with ready-made options and a recommended answer. "Use the recommended" is a complete reply. No recalling, no summarizing, no long answers.
3. **It hands you a note.** Once you nod, it writes plain text you can send straight to an AI. The format, the things it must not write, and how to check the result are all spelled out.

For the same kind of task later, **the note stays exactly as it is. You only fill in what changed.**

> In plain words: **you get aligned once, then you just fill in the blanks.**

---

## Watch one full run

Here's a weekly report. This is the real rhythm, shortened:

```
You:  Last week I spent ages getting the AI to write my weekly report the way
      I want. Save that format for me.
      (paste the chat log)

It:   I read it. Your format looks like 5 parts — is this order right?
      1 Title  2 Done this week  3 Risks  4 Next week  5 Notes
      (recommended: yes, keep this)            [question 1/5]

You:  Use the recommended

It:   I found a few things you clearly didn't want. Untick any you disagree with:
      [x] polite opening lines   [x] "Overall..." summary sentences   [x] made-up numbers
      (recommended: keep all)                [question 2/5]

You:  Keep all

It:   Should unfinished work always be marked [in progress]?
      (recommended: yes)                     [question 3/5]

You:  Yes

It:   One last look at the format:
      Title -> Done this week -> Risks -> Next week -> Notes.
      No part may be dropped, no heading reworded. OK?

You:  OK

It:   Last choice, how strict should it be?
      A Follow the template exactly (recommended) / B Loosely / C Add a sample to copy
      A is safest, B is flexible but drifts, C helps a beginner. Which one?

You:  A

It:   Here's your note, copy it from below.
```

A piece of the note (this is just a slice — see the [full example](examples/weekly-report.md)):

```
Write a weekly report. It must have exactly these 5 parts, in this order,
with these exact headings:
  1. Title   2. Done this week   3. Risks   4. Next week   5. Notes

Do not write: polite opening lines, sentences starting with "Overall...",
numbers you have no source for.
Mark unfinished work [in progress].
Before finishing, check: are all 5 parts there? Were any headings changed?
Did you invent any numbers?

## Fill in for this run
Topic: Q4 review
Done this week: ...
```

**Next week's report: keep every line above unchanged. Edit only the last two.**

---

## Six steps, in plain words

| | What happens | What you do |
|---|---|---|
| Step 1 | Turns the chat log into a rough format | Paste your material |
| Step 2 | Asks 3–5 easy questions to catch things you never said out loud | Reply "use the recommended", or tick an option |
| Step 3 | Shows you the format and **won't write a word until you say yes** | Glance at it, say "OK" |
| Step 4 | Offers 2–3 ways to write it, with the good and bad of each | Pick one (the recommended one is fine) |
| Step 5 | Writes the note and checks its own work | Nothing, really |
| Step 6 | Hands it over and shows you how to fill it in later | Save the file |

The usage guide calls these S0 to S5. Same six steps, just formal names.

**After step 3 it stops asking questions.** From there it only confirms, offers choices, and checks — same care, without repeatedly interrupting you.

---

## Three rules

| | In plain words |
|---|---|
| 1 | **No writing until you nod.** It won't throw out a "quick first draft" that quietly changes the format. If you say "stop asking, just do it", it uses every recommended answer — but tells you clearly which parts it guessed. |
| 2 | **Skipped is not agreed.** Anything you skipped is labelled "this is a guess, say the word and I'll change it". It will never pretend you confirmed it. |
| 3 | **One note, nothing else.** No side documents, no web pages, no code — unless you ask for something extra. |

---

## What's written on the note

There are 11 small blocks. That sounds like a lot, but they're really just five kinds of information:

| What it says | In plain words |
|---|---|
| What the note is for, and when to use it | So the AI knows the job from the first line |
| **How many parts, their exact headings, their order** | The most important bit — headings must not be reworded or reordered |
| What it must not write, plus rules you always assumed but never said | E.g. "no polite openings", "mark unfinished work" |
| How to check the result | A short list you can tick off one by one |
| What to do when information is missing, and what it won't do | No inventing; missing things are marked "to fill" |

The 11 block names (these are English headings in the note; you don't need to memorise them):

`Purpose` what it's for · `Context` when to use it · `Task` what to produce · `Format` the format (most important) · `Constraints` rules to follow · `Prohibited` things not to write · `Gold Standard` one ideal sample · `Self-Check` the checklist · `Fallback` when information is missing · `Rule Priority` which rule wins in a conflict · `Non-Goals` what it won't do

At the very end there's a `## Fill in for this run` block. **Reusing the note means the 11 blocks never change — only that last one does.**

---

## How is this different from "just ask the AI to write me a prompt"?

| | Ask directly | With this skill |
|---|---|---|
| Where the format comes from | You have to explain it, or the AI guesses | Found in the chat log — **works even if you can't explain it** |
| Mistakes you already fixed | You fix them again next time | Written into "do not write", fixed once |
| Things the AI guessed | Quietly treated as agreed | Clearly labelled, easy to change |
| Using it later | Dig up the old chat and copy | Fill in two lines |

---

## Install and use

**Install** (copy one file; no dependencies, no internet):

```bash
mkdir -p ~/.workbuddy/skills/structure-forge
cp SKILL.md ~/.workbuddy/skills/structure-forge/SKILL.md
```

**Use it**: tell the AI "save this format for me", or say `structure forge` / `turn this conversation into a template` / `lock in this format`, then paste your material.

**Later**: send the note as-is to any AI and change only the `## Fill in for this run` lines.

Every step in detail, the kinds of material you can paste, and how to check or edit the note are in the **[usage guide](USAGE.md)**. For the full conversation and the whole note, see the **[full example](examples/weekly-report.md)**.

---

## Common questions

**I can't write prompts at all. Can I use this?**
Yes — that's the point. You only need to paste a chat log and reply "use the recommended".

**Will it ask me a huge list of questions?**
By default 3–5, one at a time, all with a recommended answer. Say "ask it all at once" if you prefer, or "stop asking, just do it" to skip them.

**Does it work with a different AI?**
Yes. The note is plain text. It doesn't depend on this skill or on WorkBuddy.

**What if it guessed wrong?**
At step 3 it shows you the format — just say "drop part 3". A note you already saved is plain text too, so you can edit it by hand.

**How do I know the AI followed it?**
Paste the AI's output back and tick through the checklist: are all parts there, were headings changed, did it write anything forbidden.

**Do I need to install anything or be online?**
No. Installing is copying one file, the AI does the work, and the note itself is just text.

---

## When not to use it

- If you need the AI to be **100% identical every time** — that isn't possible. The checklist helps you spot problems; it isn't a guarantee, so give the result a look.
- Regulated work (medical, legal, financial) — the note has no built-in industry rules; add your own hard requirements.
- If you want live data, code execution, or messages sent for you — it only writes text.
- This repository holds the instructions and docs, not a program. You need an AI tool that can load `SKILL.md`.

The usage guide and full example are currently Chinese only.

---

## What's in this repository

```
structure-forge-skill/
├── SKILL.md              Skill file (the only file you need to install)
├── README.md             Chinese overview
├── README.en.md          This file
├── USAGE.md              Usage guide: every step, FAQ, troubleshooting (Chinese)
├── examples/
│   └── weekly-report.md  Full example: one chat -> one whole note (Chinese)
└── LICENSE               MIT license
```

---

## License

MIT — see [LICENSE](LICENSE).
