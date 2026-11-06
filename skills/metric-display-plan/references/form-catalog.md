# Form catalog

Forms per data kind, with when each fits and when it misleads. Pick the form from the element's question and
kind (SKILL.md step 2), never from what the neighbouring element uses.

| Kind | Forms that fit | When | Misleads when |
|---|---|---|---|
| **rate** | big "now" figure + direction arrow / word | a summary surface; the chart lives elsewhere | the user needs to see a spike's shape |
| | sparkline or area chart | the page owns "when did it change"; window ≥ several cycles of change | the window is too short or long for the rate |
| | cell grid (per core, per worker) | parts run at different rates and imbalance matters | there is one part, or parts are interchangeable |
| **level** | figure "x of y" + position bar with threshold | bounded; the limit matters | the limit is unknown or soft |
| | status word leading, figure second | the system reports a judgement (memory pressure) | the word is invented by us, not reported |
| **stock** | figure + change over a natural period (24 h, 7 d) | it drains or fills over hours/days | the period is shorter than its movement |
| | time to empty/full ("full in ~19 days", "5h 8m left") | there is a trend to project; show only within a horizon that matters (e.g. < 30 days) | the trend is noise; projecting from one sample |
| | glyph filled to level (battery) | the object has a familiar shape | used decoratively for things without one |
| **budget** | thick bar of what is LEFT, used part hatched, reset beside | quota with a reset | the reset is unknown — then say so |
| | "% left" figure in severity colour at threshold | near exhaustion | colour is the only signal |
| **composition** | one segmented bar + legend with figures | 2–5 parts of a whole | more than ~6 parts (use a ranked list) |
| **event** | a line in an attention block, with one action | it happened and needs the user | it is fine (then show nothing, not "all good") |
| **list** | top-N rows with one bar each, other measure muted | "who" is the question | the full list belongs to another page (link to it) |
| **status** | one word, colour only for warning/critical | binary-ish state | a normal state painted green as decoration |

## Change arrows

An arrow says which way, its colour says good or bad. Settle the colour rule with the owner once (TinySift
chose good = green, bad = red, so rising CPU load is red and growing free disk is green) and apply it to
change arrows only. Direction labels (network ↓ download / ↑ upload) are not changes and stay neutral.

## Charts: the two-question test

1. Is the user's question about the *shape over time* (when, how often, how fast)?
2. Does the data move meaningfully inside the window the chart shows?

Both yes → chart. Either no → a figure with a change line, a projection, or nothing.
