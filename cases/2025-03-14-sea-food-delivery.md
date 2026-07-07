# Food delivery app for Southeast Asia

> Sample consultation — a fictional idea used to show how a `/consult` session runs end to end. No real client, no real data.

- Date: 2025-03-14 (started) / 2025-03-14 (last updated)
- Stage: Analysis
- Status: in progress

## Problem definition (Clarification output)

The founder wants to "launch a food delivery app in Vietnam." Clarification narrowed this sharply. The pain they actually care about is the **diner's**, not the restaurant's or the rider's — and it's a *time* pain, not a *money* pain: diners can't find good food near them quickly. So the re-defined problem is **discovery, not delivery**: *"in Vietnamese metros, diners cannot efficiently discover good food nearby, even where delivery logistics are already solved."*

- Assumption: scope is limited to Ho Chi Minh City and Hanoi for entry (overturn if the wedge proves nationwide).
- Assumption: "good food" = quality + fit to the diner's current craving, not just cheapest/nearest.

## Structure & hypotheses (Structuring)

- Decomposition axis: **customer journey** (crave → search → decide → order → receive → return). The pain concentrates at *search → decide*, so we cut there rather than by segment.
- Hypothesis 1 (priority): **Discovery is the real unmet need — solving it beats launching a fourth delivery app.** Incumbents (Grab, ShopeeFood) own logistics; competing on delivery is a losing battlefield.
- Hypothesis 2: **The discovery gap is worst for the "I don't know what I want" diner**, not the "I know the dish, find it cheapest" diner — so the wedge is curation/recommendation, not price search.
- Pruned: "build our own delivery fleet" — ruled out in Clarification; logistics is the incumbents' moat, not our lever.

## Verification design (Analysis)

| Hypothesis | Key Question | Answer First (evidence to find) | Status |
|---|---|---|---|
| H1: discovery is the real unmet need | Where do diners abandon the incumbent apps — at logistics, or at *choosing*? | Funnel/drop-off data or user interviews showing search-abandon > checkout-abandon | untested |
| H1 | Do the incumbents already treat discovery as solved (thin recommendation UX)? | Teardown of Grab/ShopeeFood discovery surfaces; app-review complaints about "can't decide" | no info |
| H2: gap worst for the undecided diner | What share of order sessions start with no specific dish in mind? | Survey / session-intent data segmented by "knew the dish?" | untested |

## Conclusion

(Not reached — the founder needs to run the two untested KQs before a direction is locked.)

## Next actions

- [ ] Interview 8–10 diners in HCMC: is the friction *finding* or *getting*? (validates H1)
- [ ] Tear down Grab/ShopeeFood discovery UX — is curation genuinely thin? (validates the H1 sub-question)
- [ ] Draft the "undecided diner" persona and test whether it's a large enough segment (validates H2)

## Session log

- 2025-03-14: Reframed "delivery app" → "discovery problem" in Clarification. Founder produced H1 themselves after a "so what?" push. Designed KQ/AF for H1–H2; two KQs left untested pending real research. Stopped before Conclusion by design — no data yet.
