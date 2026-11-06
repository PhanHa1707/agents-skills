# Worked example: TinySift Overview, 2026-11-06

Source: tiny-cli `docs/specs/2026-11-06-stats-pages-roles/ledger.md` (SP4, SP19–SP31); mocks in
`~/scratch/tiny-cli/stats-pages/`.

## What went wrong

- The machine record (`MachineRecord`) returns a time series for CPU, RAM and network, so the agent's round-1
  proposal was "readings strip adds Network and Battery, each with a 1 h sparkline" (SP4.1). The owner
  approved the round as a whole.
- Five Sonnet mock agents received that line in their briefs. Three Overview directions came back that
  differed in layout (rail, shared timeline, 2×2 grid) and were identical in content: every reading a
  number over an area chart.
- An Opus review checked ledger fidelity, duplication between pages and taste rules. It did not ask whether
  each element's form fit its data, so it passed the template.
- The owner: "this Overview cluster uses one kind of display for everything; Disk could show only the GB and
  the last 24 h change, up or down, why must it have a chart? We still feel limited on ideas."

## What the element sheet would have said

| Element | Question | Kind | Lead figure | Second line | Form |
|---|---|---|---|---|---|
| CPU | Is the Mac busy, and getting busier? | rate | `38%` | `7 of 12 cores free`, `↑ Load rising` (red) | figure + 12 core cells (P/E) |
| RAM | Is memory short? | level + status | `41.2 of 64 GB` | `Pressure Normal`, `22.8 GB free or cached` | figure + composition bar |
| Disk | Will I run out of space? | stock | `61 GB free` | `↓ 3.2 GB in 24 h · full in ~19 days` | text only |
| Network | Is something transferring? | rate | `↓ 2.4 MB/s ↑ 310 KB/s` | `1.8 GB down · 120 MB up in 6 h` | text only |
| Battery | How long will it last, is it healthy? | stock | `72%` | `5h 8m left`, `Health 91% · 412 cycles` | figure + battery glyph |
| Limits | How much agent quota is left? | budget | `7% left` | `resets 14:30` | thick "left" bar, used hatched |
| Hot Mac | Is it throttling? | event | — | "Your Mac is hot and slowing down" → Open CPU | attention line, only when serious |

Template check: six different forms, no chart; the charts stay on the CPU, RAM and Network pages, which also
removes duplication between Overview and those pages.

## What the organising ideas were

Headroom (everything as what is left), status sentence (one line when calm; the attention block replaces it
when not), today's digest (needs history kept across Quit — deferred), machine diagram (rejected as
decoration). The owner picked headroom + sentence, then the bento "Headroom board" (H2) where tile size and
shape follow each reading, and asked for the totals to lead each tile.

## Lesson

The template came from the agent, not the owner, and every later step copied it faithfully. The fix is not a
stronger model; it is filling the element sheet before the first proposal, and briefing forms per element.
