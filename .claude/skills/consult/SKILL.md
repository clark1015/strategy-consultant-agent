---
name: consult
description: Interview a new business idea or problem in CSAC order (Clarification → Structuring → Analysis → Conclusion). Draw the user's hypotheses and insight out with questions, and save a record to cases/ at the end.
---

# /consult — idea consulting by interview

Dig into the user's idea or problem using the CSAC process. **This is not where you analyze *for* them — it's where your questions make them analyze.** Apply the conversation rules from `CLAUDE.md` (one or two questions at a time, reflect answers back structured, hypotheses from their mouth) through every stage.

## Start

- If they've thrown out even a one-line idea, begin. If not, ask for the idea (or the worry) in one line.
- Check `cases/` for a file on the same topic; if it exists, read it and continue.
- Open by naming the four stages you're about to walk, one line each, so they have the map.

## Stage 1: Clarification — fix the real problem

Goal: turn a vague idea into a problem statement with settled scope, terms, and assumptions.

- Question order: **big picture → specific context → detail → validation.** What to pin down: background/context, term definitions, scope (time / geography / target), available resources & authority.
- Tone: "Whose pain, exactly, does this remove?" → "Is that 'inconvenient' a *time* problem or a *money* one?" → "If we narrow the target to X, who falls out?"
- For anything they can't answer, fix it as an assumption together: "Let's assume ___ for now, and flag it so we can overturn it later."
- **Exit condition:** write the re-defined problem as one paragraph, show it, get their agreement.

## Stage 2: Structuring — MECE decomposition and hypotheses

Goal: break the problem down into 1–3 conclusion-shaped hypotheses.

- Let them pick the decomposition axis first: "We could split this by customer journey, or by segment — which one won't cut through the heart of it?" (If needed, recommend a lens from `concepts/05-frameworks.md`.)
- Have them fill the branches, and check MECE with a question: "Split this way, is there a case that falls through the gap?"
- When a fact appears, push it up with "So what?" into a **conclusion-shaped hypothesis** ("X is true!"). Reject question-shaped ones: "That's a question — say it as a verdict."
- Prune branches that Clarification or common sense already rules out (say the reason out loud).
- **Exit condition:** a prioritized list of hypotheses.

## Stage 3: Analysis — Key Questions, Answer First, and verification runs

Goal: a verification design per hypothesis — and, if they want it, the verification itself.

- Per hypothesis: "What would you need to *see* to know this is true?" → derive the **Key Question.** Check it against the two tests (descends from the hypothesis / useful once answered).
- "What *shape* of data would that answer live in?" → fix the **Answer First.** Then: "If you can't find data of that shape, what happens to this hypothesis?"
- If they're still hypothesis-hunting, run **initial-research-level** searches — only to the three depth targets (industry structure / major players / pain points), qualitative feel over precise numbers, `filetype:pdf` trick included.
- Once the hypothesis–KQ–AF chain stands, **offer to run the checks yourself.** Per KQ, search for evidence of the AF's shape — follow news citations upstream to primary sources. If one KQ needs a broad, cross-checked answer, suggest running the `deep-research` skill on it and fold its report back into the table.
- Report every result as **fact → implication for the hypothesis**, never a data dump. Two or three solid sources per KQ is enough here — direction over precision; exact figures still wait for deep validation.
- Keep the interview alive through the verdicts: show the evidence, then hand it back — "given this, where does the hypothesis land?" **They** pronounce it true / no info / false. Treat "no info" as a real verdict: a hypothesis you can't verify is moot (`concepts/04-key-questions.md`).
- **Exit condition:** a [hypothesis – KQ – AF – status] table.

## Stage 4: Conclusion — synthesis and next actions

- Filter the surviving KQs by the three tests (contributes to the solution / touches the core / carries an interesting insight), let findings converge upward, and have **them** state the conclusion first: "In one sentence, what's the conclusion so far?"
- Polish it into final form, then lay out 2–3 next actions (KQs to validate deeply, things to build, people to meet).

## Record

If the session went somewhere real, offer to save it as `cases/YYYY-MM-DD-topic.md` (using `cases/_TEMPLATE.md`). After saving, note that "next time, call `/consult topic` to continue."

## Notes

- Don't try to finish all four stages in one session. Follow their pace; if it breaks off, record up to the current stage.
- On each transition, announce it — "Stage 2 done, moving to Stage 3" — so they always know where they are on the map.
