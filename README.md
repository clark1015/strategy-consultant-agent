# 🧭 Strategy Consultant Agent

**English** | [한국어](README.ko.md)

**An AI strategy consultant that interviews you — instead of answering for you.**

Most AI "business advisors" dump a generic SWOT and call it a day. This one does the opposite. It runs a **Socratic, McKinsey-style interview**: it asks one or two sharp questions at a time, structures your answers back to you, and refuses to move on until the *real* problem is defined. The insight comes out of *your* mouth — the agent just makes sure you don't skip a step.

**What this repo really is:** a worked example of taking a consulting methodology — structured, hypothesis-driven problem-solving — and *engineering it into a working [Claude Code](https://docs.claude.com/en/docs/claude-code) agent*. Not a prompt you paste, but an agent you think alongside: a persona (`CLAUDE.md`) + two workflow skills + a distilled method library. The interesting part isn't the frameworks — it's that a way of *thinking* got compiled into something that runs.

---

## Why I built this

This didn't start as a portfolio piece. It started with a frustration I kept hitting while taking my own side project to production.

Shipping was never the bottleneck — with AI, code gets written fast. The hard part was every decision *in front of* the code: which user's pain to solve first, whether a feature was a direction or a distraction, whether the problem I was excited about was even real. I kept catching myself deciding on momentum and vibes — skipping cases, never stating a hypothesis in a form that could be killed. Code has types, tests, and reviews to catch my mistakes. My strategy decisions had nothing.

What I wanted was the discipline firms like McKinsey are famous for institutionalizing: **structured, hypothesis-driven problem solving** — MECE decomposition so no option goes unexamined, conclusion-shaped hypotheses so every claim can be proven or killed, and a partner who refuses to move on until the problem is actually defined.

So I dug into the publicly available material on that methodology, rewrote it in my own words as the `concepts/` library, and engineered it into an agent I can sit across from whenever a real decision comes up. Not a "write me a business plan" bot — an interviewer aspiring to consulting-grade rigor that makes *me* do the thinking. Because the only conclusions I'll actually act on are the ones that came out of my own mouth.

---

## Why this is different

| Typical "AI advisor" | This agent |
|---|---|
| Gives you the answer | Asks questions until *you* find the answer |
| Fills in a framework template | Uses frameworks to reach an **insight**, then stops |
| Jumps to solutions | Won't leave *problem definition* until it's airtight |
| One-shot dump | Stateful: consultations are saved and resumed |

The design bet: **for strategy, a good question beats a confident answer.** A consultant who hands you conclusions makes you dependent; one who interrogates your thinking makes you sharper.

---

## 90-second demo

> A representative `/consult` session — fictional idea, real flow. The human is exploring a food-delivery idea for Southeast Asia.

```
You:    I want to launch a food delivery app in Vietnam.

Agent:  Before we size anything — whose pain does this remove, exactly?
        Restaurants, riders, or diners? Pick the one you'd cry over losing.

You:    Diners. Ordering is a mess.

Agent:  "A mess" — is that a *time* problem or a *money* problem for them?

You:    Time. It takes forever to find something good near you.

Agent:  Good. Let me reflect that back: your problem isn't "delivery,"
        it's *discovery* — diners can't find good food fast. Agree?

You:    ...huh. Yeah, actually.

Agent:  Before we pick where to play — let's split the diner's journey with
        no gaps: crave → search → decide → order → receive. Any step that
        falls *between* those?

You:    No, that covers it. And it breaks at search → decide.

Agent:  Good — so we're not guessing which problem to attack, we've ruled the
        others out. That's the MECE discipline: no case left unlooked-at.

Agent:  Then here's the trap: Grab and ShopeeFood already own delivery.
        If your wedge is discovery, that's a different fight.
        Say it as a claim we can prove or kill — "___ is true."

You:    Discovery is underserved even where delivery is saturated?

Agent:  That's a question, not a hypothesis. Commit to a verdict.

You:    Discovery is the real unmet need — solving it beats a 4th delivery app.

Agent:  Now we have something to test. What would you need to *see* in the
        market to know that's true? (That's your Key Question.)
```

Notice: the agent never said "here's your business plan." It moved the user from a vague idea → a sharp, falsifiable hypothesis → a validation question, one nudge at a time.

---

## The method: CSAC

Every consultation follows four stages. The agent always knows which one it's in and won't let you skip ahead.

```
Clarification  →  Structuring  →  Analysis  →  Conclusion
 (real problem?)   (break it down,   (design tests   (what to do
                    form hypotheses)  for each)        next)
```

- **Clarification** — re-define the problem until scope, terms, and assumptions are locked. "Is this even the real problem?"
- **Structuring** — break the problem down MECE-style, then turn facts into *conclusion-shaped hypotheses* ("X is true!", not "is X true?").
- **Analysis** — for each hypothesis, design a **Key Question** (what would prove it?) and an **Answer-First** shape (what data would the answer live in?). Once the design stands, the agent can run the checks itself — reporting every result as *fact → implication for the hypothesis*, never a data dump.
- **Conclusion** — converge validated findings into a one-paragraph strategy and 2–3 concrete next actions — optionally written up as a one-page, conclusion-first memo (Pyramid Principle + SCQA).

Core stance, borrowed from the source methodology:

> *"The best strategy is the one you'll regret least — which means considering every option before you choose, and not moving on until you have."*

---

## What you can think through with it

Not just "validate my startup idea." It's a structured thinking partner for any decision where skipping a step is the real risk:

- **A new product or service idea** — pressure-test it before you build anything.
- **A service / feature-direction call** — "should we go A or B?" reasoned out MECE-ly, not decided on vibes.
- **Market entry or positioning** — find the battlefield you can actually win on.
- **A pitch or proposal** — run `/pitch-review` to stress-test it against seven lenses.

Every time, the job is the same: keep you from skipping a step, and make the conclusion come from *you* — so you own it, and can defend it.

---

## What's in here

```
CLAUDE.md            The consultant persona. Drop into Claude Code and it
                     becomes an interviewer, not an answer machine.
concepts/            The methodology, distilled into 7 reference notes
                     (MECE, CSAC, initial research, Key Questions, frameworks,
                     the pyramid memo…).
.claude/skills/
  consult/           /consult  — run a full CSAC interview on a new idea.
  pitch-review/      /pitch-review — stress-test a pitch deck with 7 lenses.
cases/               Saved consultations (living documents, resumable).
```

## Try it

1. Install [Claude Code](https://docs.claude.com/en/docs/claude-code).
2. Clone this repo and open it: `cd strategy-consultant-agent && claude`.
3. Just describe an idea — or run `/consult` to start the structured interview.

The `CLAUDE.md` in the repo root is what flips Claude into consultant mode automatically.

---

## Credits & scope

The methodology is distilled from strategy-consulting fundamentals (structured problem-solving, hypothesis-driven thinking, MECE) — the same toolkit taught in top consulting firms and reconstructed here **in my own words**. This repo ships *my* rewrite and agent design, not any third party's slides or copyrighted material.

Not affiliated with, or endorsed by, any consulting firm.
