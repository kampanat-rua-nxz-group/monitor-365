# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Single static HTML file (`index.html`) with inline CSS and JS, no build step. Talks to the GitHub GraphQL API directly from the browser with a personal access token stored in localStorage. Chosen by the user.

## Users

One developer (the owner) who authors pull requests and is asked to review other people's pull requests on GitHub.com. Personal tool, not shared with a team. They open it in checks a few times a day on a laptop (morning, after meetings, before leaving) and work through it one PR at a time.

## Product Purpose

Show every open pull request the user is involved in, as author, requested reviewer, past reviewer, or assignee, sorted into lanes by review state, so the user knows what needs them right now and what is stuck. Success: in a few seconds the user can see which PRs are their turn and act on each one.

## Positioning

GitHub's own lists show PRs, not whose turn it is. This board derives turn from review history: who reviewed, whether the author pushed or replied after feedback, which threads are still unresolved, and how long the PR has sat in its current state.

## Operating Context

- Checked in rounds on a laptop browser; a phone layout must still work.
- Most important thing on open: PRs where it is the user's turn (review, re-review, address feedback, merge).
- Secondary: how long each PR has waited in its current state, thread resolution, reviewer states, CI, conflicts.
- Lanes: Draft, Awaiting review, Changes requested, Updated / re-review, Approved, Done (recent).
- Two groups: PRs I authored, PRs I review.

## Capabilities and Constraints

- GitHub.com only. Search API, up to 100 PRs per search type.
- Auto-refresh on an interval; manual refresh; browser notifications optional.
- Bot reviews can be excluded from lane logic.
- Demo mode with synthetic data (`?demo`).
- UI copy in English.

## Evidence on Hand

No real user data ships with the app. Demo data is synthetic and labelled as demo.

## Product Principles

1. Whose turn it is comes first; everything else supports that.
2. Time waiting is a first-class fact, not a footnote.
3. Every card links straight to the place on GitHub where the action happens.
4. Quiet when nothing needs the user; loud only for their turn and for stale PRs.
