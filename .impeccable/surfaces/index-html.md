---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

# PR Monitor board

Scope: the whole single-page app (`index.html`). Mode: Operate.
Audience and job: one developer checking in rounds on a laptop; first job is "which PRs are my move", then "what is stuck".
Constraints: single static HTML file, system fonts, English UI, GitHub.com data, demo mode.

## Direction contract

THESIS: Every PR is a game in progress with a clock running on one side. The board shows whose clock is running and for how long. It refuses the default grey kanban of identical cards with emoji badges and a coloured left stripe.

OWN-WORLD: Tournament chess. Near-black green "clock case" for the header and the Your move rail; pale board-green grey ground; off-white cards; tournament green for the opponent's running side; amber lit face for your side; flag red for a fallen flag (stale). System sans, tabular clock digits, drawn 1.75px stroke icons, no emoji.

STORY: The user opens the page, reads the count of PRs on their clock, works the Your move rail left to right (longest-waiting first), then scans the lanes for flags that have fallen.

FIRST VIEWPORT: Dark case header across the top with the product name, the Your move count as the largest number on screen, last update, refresh, settings, avatar. Directly under it, still on the dark case, the Your move rail: one row of clock tiles, each with repo#number, title, verb (Review, Re-review, Address feedback, Merge) and the lit wait time. Below on the light ground: a toolbar (segmented All / Mine / Reviewing with counts, repo select, search, group toggle) and the six-lane board.

FORM: Chess clock, candidate 1 of my ordered list (user chose it over the assigned Circulation desk). seed: seed:b7512591880d253c. Signature move: a two-faced clock on every card, "You" and "Them"; the face whose turn it is is lit and shows the running wait; a flag drops on the face when the wait passes the stale threshold; done PRs show a stopped clock.

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
