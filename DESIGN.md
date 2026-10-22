---
name: PR Monitor
description: A chess clock for every open pull request; it shows whose move it is and how long they have been thinking.
colors:
  case: "#1b201b"
  case-raised: "#262c25"
  case-hover: "#303730"
  case-line: "#3a4238"
  case-text: "#eef1ea"
  case-muted: "#a9b2a4"
  board-ground: "#e7eae2"
  lane: "#dce0d5"
  card: "#fbfcf9"
  line: "#c9cfc1"
  line-soft: "#e0e4da"
  text: "#1a1f19"
  muted: "#556050"
  faint: "#5a6556"
  you: "#f2b632"
  you-ink: "#2a1f05"
  you-soft: "#fbe9bd"
  them: "#3f6f34"
  them-soft: "#d5e3cb"
  them-ink: "#21401a"
  flag: "#c23b2a"
  flag-soft: "#f6dcd6"
  ok: "#2f7a3b"
  bad: "#b3372a"
  warn: "#8a5e00"
typography:
  display:
    fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "40px"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: "-0.02em"
    fontFeature: "tnum"
  headline:
    fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "22px"
    fontWeight: 600
    letterSpacing: "-0.01em"
  title:
    fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 600
    lineHeight: 1.3
  title-sm:
    fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "15px"
    fontWeight: 600
  body:
    fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.45
  body-sm:
    fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "13px"
    fontWeight: 400
  label:
    fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "12px"
    fontWeight: 500
  clock:
    fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "13px"
    fontWeight: 600
    fontFeature: "tnum"
  clock-lg:
    fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "18px"
    fontWeight: 600
    fontFeature: "tnum"
  mono:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "12px"
rounded:
  xs: "4px"
  sm: "5px"
  md: "6px"
  lg: "10px"
  pill: "999px"
spacing:
  2xs: "2px"
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
  gutter: "20px"
  xl: "32px"
  2xl: "48px"
components:
  button:
    backgroundColor: "{colors.card}"
    textColor: "{colors.text}"
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: "0 12px"
    height: "32px"
  button-primary:
    backgroundColor: "{colors.case}"
    textColor: "{colors.case-text}"
    rounded: "{rounded.md}"
    padding: "0 12px"
    height: "32px"
  button-primary-hover:
    backgroundColor: "{colors.case-hover}"
  button-ghost-hover:
    backgroundColor: "{colors.line-soft}"
  button-on-case:
    textColor: "{colors.case-text}"
    rounded: "{rounded.md}"
    padding: "0 12px"
    height: "32px"
  button-on-case-hover:
    backgroundColor: "{colors.case-raised}"
  button-icon:
    rounded: "{rounded.md}"
    size: "32px"
  segmented:
    backgroundColor: "{colors.lane}"
    rounded: "7px"
    padding: "2px"
  segmented-option:
    textColor: "{colors.muted}"
    rounded: "{rounded.sm}"
    padding: "0 12px"
    height: "28px"
  segmented-option-active:
    backgroundColor: "{colors.card}"
    textColor: "{colors.text}"
  toggle-flag-on:
    backgroundColor: "{colors.flag-soft}"
    textColor: "{colors.flag}"
  field:
    backgroundColor: "{colors.card}"
    textColor: "{colors.text}"
    rounded: "{rounded.md}"
    padding: "0 10px"
    height: "32px"
  rail-tile:
    backgroundColor: "{colors.case-raised}"
    textColor: "{colors.case-text}"
    rounded: "{rounded.md}"
    padding: "10px 10px 10px 12px"
  rail-tile-hover:
    backgroundColor: "{colors.case-hover}"
  tile-clock:
    backgroundColor: "{colors.you}"
    textColor: "{colors.you-ink}"
    typography: "{typography.clock}"
    rounded: "{rounded.xs}"
    padding: "5px 9px"
  tile-clock-flag:
    backgroundColor: "{colors.flag}"
    textColor: "#ffffff"
  lane:
    backgroundColor: "{colors.lane}"
    rounded: "{rounded.md}"
    padding: "4px 8px 8px"
  card:
    backgroundColor: "{colors.card}"
    textColor: "{colors.text}"
    rounded: "{rounded.md}"
    padding: "10px 12px"
  clock:
    backgroundColor: "{colors.card}"
    textColor: "{colors.faint}"
    typography: "{typography.label}"
    rounded: "{rounded.sm}"
    height: "30px"
  clock-lg:
    rounded: "{rounded.sm}"
    height: "44px"
  clock-face-you-lit:
    backgroundColor: "{colors.you}"
    textColor: "{colors.you-ink}"
    padding: "0 8px"
  clock-face-them-lit:
    backgroundColor: "{colors.them-soft}"
    textColor: "{colors.them-ink}"
    padding: "0 8px"
  clock-face-flag:
    backgroundColor: "{colors.flag}"
    textColor: "#ffffff"
  clock-stopped:
    textColor: "{colors.faint}"
    rounded: "{rounded.sm}"
    height: "30px"
  pill:
    backgroundColor: "{colors.lane}"
    textColor: "{colors.muted}"
    rounded: "{rounded.pill}"
    padding: "1px 6px"
  pill-on-author:
    backgroundColor: "{colors.you-soft}"
    textColor: "{colors.warn}"
  pill-on-reviewer:
    backgroundColor: "{colors.them-soft}"
    textColor: "{colors.them-ink}"
  notice:
    backgroundColor: "{colors.flag-soft}"
    textColor: "{colors.bad}"
    rounded: "{rounded.md}"
    padding: "10px 12px"
  notice-warn:
    backgroundColor: "{colors.you-soft}"
    textColor: "{colors.warn}"
  inspector:
    backgroundColor: "{colors.card}"
    width: "440px"
  dialog:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.lg}"
    width: "560px"
---

# Design System: PR Monitor

## Overview

**Creative North Star: "The Tournament Clock"**

PR Monitor is a tournament hall seen from the player's chair. A near-black green clock case runs across the top and holds the only thing that matters first: how many games are waiting on your move, and for how long. Below it the board opens onto a pale, board-green ground where every pull request sits as an off-white card with a two-faced chess clock on it, "You" on the left and the other side on the right. The face whose turn it is lights up and shows the running wait; when the wait passes the stale threshold, the flag falls and the face turns red; finished games show a stopped clock with a dashed rim.

The system is dense and quiet, built for a developer checking PRs in rounds on a laptop. It is loud in exactly two places, the user's turn (amber) and fallen flags (red), and calm everywhere else (greens, greys, hairlines). Typography is one system sans with tabular figures so clock digits never jitter. Icons are drawn line glyphs at a 1.75px stroke. The world refuses the default grey kanban of identical cards with emoji badges and a coloured left stripe: state is carried by the clock, not by decoration on the card edge.

Light and dark themes are the same hall under different lighting: in dark mode the case deepens to near-black, the ground and cards become dark felt greens, and the amber lit face keeps its exact value so your clock reads the same in both.

**Key Characteristics:**
- Dark clock case on top, pale board-green ground below; the case holds only the header and the Your move rail.
- A two-faced chess clock on every card; exactly one face is lit, and it carries the wait time.
- Amber means your move; tournament green means theirs; flag red means a fallen flag.
- One system sans, tabular numerals for every time and count, 1.75px stroke line icons, no emoji.
- Flat cards with a hairline border and a whisper of ambient shadow; only overlays lift.

## Colors

A muted tournament-green neutral world with one warm signal (amber) for the user's move and one hot signal (flag red) for overdue games.

### Primary
- **Lit Clock Amber** (`you`): the lit "You" face of a clock, rail tile clocks, the Your move count (the largest number on screen), the action verb under each rail tile, the brand glyph and demo pill on the case. Same value in light and dark.
- **Amber Ink** (`you-ink`): text on any amber fill; near-black brown so the digits read at 8.9:1.
- **Amber Wash** (`you-soft`): soft tint for "waiting on author" pills, the warning notice, and text selection.

### Secondary
- **Tournament Green** (`them`): the opponent's side. Selected-card ring, links inside the inspector and settings, checkbox accent.
- **Green Wash** (`them-soft`): the lit "Them" face and "review requested" pills.
- **Deep Board Green** (`them-ink`): text on the green wash.

### Tertiary
- **Flag Red** (`flag`): a fallen flag. Solid fill on a clock face or rail tile clock past the danger threshold (white text on top), and the active "Flag fell" filter.
- **Flag Wash** (`flag-soft`): background of the active flag filter and the error notice.
- **Pass Green / Fail Red / Caution Ochre** (`ok`, `bad`, `warn`): CI, review-state badges, conflicts, additions and deletions, and the text of warning pills and notices. Status only; never used as surface fills beyond the small review badges.

### Neutral
- **Clock Case** (`case`): header and Your move rail background; also the primary button fill on light ground.
- **Raised Case / Case Hover** (`case-raised`, `case-hover`): rail tiles at rest and on hover, case button hover.
- **Case Line** (`case-line`): borders and the hairline under the case.
- **Case Text / Case Muted** (`case-text`, `case-muted`): primary and secondary text on the case.
- **Board Ground** (`board-ground`): page background below the case; also the sticky lane-head backing.
- **Lane** (`lane`): lane columns, segmented-control track, pill and code backgrounds.
- **Card** (`card`): cards, fields, buttons, inspector, dialog.
- **Line / Line Soft** (`line`, `line-soft`): field and clock borders; card borders and inner dividers.
- **Ink / Muted / Faint** (`text`, `muted`, `faint`): primary text, secondary text, metadata and counts.

Dark mode remaps every neutral and the green/red/status families to darker grounds and lighter inks (values in the sidecar `colorMeta.*.dark`); amber stays `#f2b632`.

### Named Rules
**The Your Move Rule.** Full-strength amber is reserved for the user's turn: the lit You face, the rail tile clocks, the Your move count and verbs. Outside that, amber appears only as a wash (`you-soft`) or as a small mark on the dark case (brand glyph, demo pill). If amber shows up on the light board and it is not your clock, it is wrong.

**The Fallen Flag Rule.** Solid flag red appears only when a wait has passed the danger threshold, and always with the drawn flag icon beside the time. Below the threshold the clock stays amber or green; the warning threshold shows the outline flag icon on the lit face without changing its colour.

**The Case Rule.** The dark case holds the header and the Your move rail and nothing else. Everything the user scans rather than acts on lives on the light ground.

## Typography

**Display Font:** system-ui (with -apple-system, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif)
**Body Font:** the same system sans
**Label/Mono Font:** ui-monospace (with SFMono-Regular, Menlo, Consolas) for code, file paths and token scopes only

**Character:** one plain, native sans used at a handful of sizes, with tabular figures doing the expressive work: the clock digits are the voice of the system.

### Hierarchy
- **Display** (600, 40px, line-height 1, -0.02em, tabular): the Your move count on the case. One per screen.
- **Headline** (600, 22px, -0.01em): the welcome heading.
- **Title** (600, 17px, 1.3): the inspector's PR title; the settings dialog head uses 16px.
- **Title Small** (600, 15px): brand name and the "PRs are on your clock" label.
- **Body** (400, 14px, 1.45): base text; card titles at 14px/1.35 clamped to two lines; rail tile titles at 600. Welcome copy capped at 65ch.
- **Body Small** (400, 13px): inspector facts and lists, notices, form labels (500).
- **Label** (500, 12px): repo#number refs, card metadata, lane descriptions, verbs, counts; pills at 11px.
- **Clock** (600, 13px, tabular): the running time on a lit face and on rail tile clocks; 18px on the large inspector clock.

### Named Rules
**The Tabular Clock Rule.** Every time, count and diff number uses `font-variant-numeric: tabular-nums`. Clock times are 600 weight; everything around them is 400 or 500 so the digits lead.

**The One Voice Rule.** One sans family for everything. Weight carries hierarchy (600 for titles and times, 500 for labels and controls, 400 for prose); no display face, no uppercase labels.

## Layout

Two horizontal zones. The case spans the full width: a 56px header bar, then the Your move rail, a single row of clock tiles laid out as a horizontally scrolling grid of columns at least 260px wide with 8px gaps, longest wait first. Below, on the ground: a wrapping toolbar (segmented role filter with counts, flag filter, repository select, search, group toggle), then a six-lane board (Draft, Awaiting review, Changes requested, Updated, Approved, Done) as a CSS grid with 8px column gaps that scrolls horizontally with snap. Lane heads stick to the top. With grouping on, swimlane heads ("My PRs", "Reviewing") span all lanes and each lane cell becomes its own rounded block.

Spacing runs on a 4px base: 2/4/8/12/16/20/32/48, with 6px and 10px used inside controls (icon gaps, card and tile padding). Page gutter is 20px on desktop and 12px under 720px. Cards stack with 8px gaps inside lanes.

Under 720px the rail tiles stack in one column, status text and username hide, search goes full width, and form rows collapse to one column. At 1200px and wider, opening the inspector (a 440px right-hand panel) pads the main area so the board stays visible beside it; below that the inspector overlays.

## Elevation & Depth

Mostly flat with tonal layering: case → raised case for tiles; ground → lane → card for the board. Cards carry a hairline border plus a barely-there ambient shadow so they sit on the lane like pieces on felt. Real lift is reserved for overlays.

### Shadow Vocabulary
- **Resting** (`box-shadow: 0 1px 2px rgba(20,28,18,.07), 0 2px 8px rgba(20,28,18,.05)`; dark: `0 1px 2px rgba(0,0,0,.35)`): cards, the active segmented option.
- **Overlay** (`box-shadow: 0 8px 32px rgba(15,20,14,.18), 0 2px 6px rgba(15,20,14,.08)`; dark: `0 12px 40px rgba(0,0,0,.55)`): the inspector panel and the settings dialog only.

### Named Rules
**The Felt Table Rule.** Surfaces on the board never lift beyond the resting shadow, including on hover; hover changes the border, not the elevation. Only things that cover the board (inspector, dialog) use the overlay shadow.

## Shapes

Gently squared corners throughout: 6px for cards, buttons, fields, tiles, lanes and notices; 5px for the clock and segmented options (7px on the segmented track); 4px for the small rail tile clock and inline code; 10px for the dialog; full pills for status pills, the demo pill and team tags; circles for avatars and review-state badges. Borders are 1px hairlines. The clock is the one recurring silhouette: a short rounded rectangle split by a vertical hairline into two faces; a stopped clock keeps the silhouette with a dashed border and a transparent fill. Lane heads round only their top corners and lane cells their bottom corners so a lane reads as one column.

## Components

### Buttons
Compact and quiet; the case carries the weight, not the buttons.
- **Shape:** gently squared (6px), 32px tall, 12px horizontal padding, 500 weight, icon + label with a 6px gap.
- **Default:** card fill with a `line` border; hover darkens the border to `faint`; press nudges down 1px.
- **Primary:** clock-case fill with case text (Save in settings); hover lightens to `case-hover`.
- **Ghost:** transparent until hover, then `line-soft`.
- **On the case:** transparent with a `case-line` border; hover fills `case-raised` and lifts the border to `case-muted`.
- **Icon:** 32px square. Refresh spins its icon while loading.

### Chips
- **Segmented filter:** a `lane` track (2px inset) holding 28px options with counts in `faint`; the active option becomes a card-coloured tab with the resting shadow.
- **Flag filter toggle:** button-shaped; when on, it turns flag-red text on the flag wash with a filled flag icon.
- **Pills:** 11px on `lane`; "waiting on author" on the amber wash, "review requested" on the green wash, each with a small icon.

### Cards / Containers
- **Corner Style:** 6px.
- **Background:** `card` on a `lane` column.
- **Shadow Strategy:** resting shadow (see Elevation).
- **Border:** `line-soft` hairline; `line` on hover; selected card gets a `them` border plus a 1px `them` ring.
- **Internal Padding:** 10px 12px, 8px between rows: ref + author, two-line title, clock, then metadata (threads, CI, conflict, +/−) with overlapping reviewer avatars carrying state badges at the right.

### Inputs / Fields
- **Style:** 32px tall (36px in the dialog), card fill, `line` border, 6px corners, 10px padding; search has a 14px leading icon.
- **Hover:** border darkens to `faint`.
- **Checkboxes:** native, accented in tournament green.

### Navigation
The header bar is the only navigation: brand glyph and name, update status, demo pill, spacer, avatar, refresh and settings buttons, all on the case. On mobile the status, username and demo pill hide.

### Chess Clock (signature)
Two faces, "You" and the other side (a reviewer, "Reviewers", "Others" or the author). Exactly one face is lit: amber with amber ink when it is your move, green wash with deep green ink when it is theirs. The lit face shows the wait in `1d 04h` / `5h 00m` form at 600 tabular. Past the warning threshold the outline flag icon joins the time; past the danger threshold the face turns solid flag red with white text and a filled flag. Drafts and finished PRs show a single-face stopped clock with a dashed border, an icon, a label and an age. Faces cross-fade background and colour over 200ms. The inspector uses a 44px large clock with 18px digits.

### Your Move Rail Tile (signature)
A raised-case button: repo#number in `case-muted`, a two-line title, and the action verb (Review, Re-review, Address feedback, Merge) in amber; on the right a small amber clock block (4px corners) with the wait, which turns flag red with a filled flag when overdue. The selected tile gets an amber border. Overflow collapses into an underlined "Show N more" link.

### Inspector
A 440px right-hand panel on `card` with a sticky header (ref, title, large clock) and sections of facts and hairline-separated lists for reviewers and threads. Slides in over 220ms on `cubic-bezier(.16, 1, .3, 1)`.

## Do's and Don'ts

### Do:
- **Do** put the user's turn on the dark case: the Your move count at 40px amber, and one rail tile per PR, longest wait first.
- **Do** give every open PR card a two-faced clock with exactly one face lit, and show the wait on the lit face only.
- **Do** use tabular numerals for every time, count and diff figure.
- **Do** draw icons as inline line glyphs on a 24px grid with a 1.75px stroke, round caps and joins, at 14/16/20px.
- **Do** show finished and draft PRs with a dashed, stopped clock instead of a lit one.
- **Do** keep board surfaces at the resting shadow and change the border on hover.
- **Do** honour `prefers-reduced-motion` by removing all transitions and animations.

### Don't:
- **Don't** use emoji anywhere: in badges, states, labels or empty states.
- **Don't** mark state with a coloured left stripe or edge band on cards; the clock carries state.
- **Don't** use full-strength amber on the light board for anything that is not the user's clock.
- **Don't** use solid flag red for anything but a fallen flag (past the danger threshold) and the active flag filter.
- **Don't** add a second typeface or uppercase tracked labels.
- **Don't** put lanes, filters or secondary information on the dark case.
