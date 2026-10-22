# 🗂️ PR Monitor

A Kanban-style board (like Jira) for tracking GitHub pull requests you **authored** or were **asked to review / assigned to**.
It's a single HTML file (`index.html`) with nothing to install: just open it in a browser.

## Getting started

1. Open `index.html` in your browser (double-click it, or host it on GitHub Pages).
2. Click **⚙️ Settings** and paste a GitHub Personal Access Token.
   - Create one at <https://github.com/settings/tokens/new?scopes=repo&description=PR%20Monitor> (classic token, `repo` scope).
   - If your org uses SSO, click **Configure SSO → Authorize** for the token.
3. (Optional) Add an extra filter such as `org:my-company` to limit the board to your work org.

To try it without a token, click **Try with demo data** or open `index.html?demo`.

> The token is stored only in that browser's `localStorage` and is sent only to `api.github.com`.

## How it works

The top of the page shows **Your move**: every PR where you are the one who needs to act (review, re-review, address feedback, merge), longest wait first.

Below it is the board. Each lane is a review state:

| Lane | Meaning |
|---|---|
| Draft | The PR is still a draft |
| Awaiting review | No review yet, or waiting on reviewers |
| Changes requested | A reviewer requested changes or left unresolved comments, and the author hasn't updated yet |
| Updated | The author pushed code, replied, or re-requested review after getting feedback |
| Approved | Approved with no open comments, ready to merge |
| Done | Merged or closed in the last N days (configurable) |

The board has two rows: **My PRs** and **Reviewing**. For PRs you review, the lane is from your point of view. If you requested changes and the author hasn't pushed yet, the PR sits in "Changes requested" with the clock on the author. Once they push, it moves to "Updated" and the clock switches to you.

## The clock

Every card has a two-sided chess clock: **You** on the left, the other side (author, a reviewer, or "Reviewers") on the right.

- The side whose turn it is lights up and shows how long it has been waiting in the current state.
- A flag appears once the wait passes the first threshold (24h by default). After the second threshold (72h) the flag falls and the face turns red.
- Merged and closed PRs show a stopped clock.

Cards also show resolved review threads, CI status, merge conflicts, lines changed, and reviewer avatars with their state (approved, requested changes, commented, or review pending).

Click a card to open the details panel: last push and feedback times, each reviewer's status, and every unresolved thread, marked as waiting on the author or answered and waiting on the reviewer.

## Other features

- Filter by All / Mine / Reviewing, by repo, or by search text (`/` focuses search). **Flag fell** shows only stale PRs.
- Auto-refresh (every 5 minutes by default). Press `R` to refresh, `Esc` to close the details panel.
- The number of PRs on your clock shows in the browser tab title, and you can turn on browser notifications.
- Reviews from bots (Copilot, CodeRabbit, etc.) are ignored when deciding whose turn it is (can be turned off in Settings).
- Light and dark mode, and a phone layout.

## Limitations

- Uses the GitHub Search API: up to 100 PRs per search type.
- Review requests sent to a **team** you belong to count as yours.
- "Last push" is based on commit times and force-push events.
