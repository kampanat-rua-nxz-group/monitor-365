# 🗂️ PR Monitor

A Kanban-style board (like Jira) for tracking GitHub pull requests you **authored** or were **asked to review / assigned to**.
It's a single HTML file (`index.html`) with nothing to install: just open it in a browser.

## Getting started

1. Open `index.html` in your browser (double-click it, or host it on GitHub Pages).
2. Click **⚙️ Settings** and paste a GitHub Personal Access Token.
   - Create one at <https://github.com/settings/tokens/new?scopes=repo&description=PR%20Monitor> (classic token, `repo` scope).
   - If your org uses SSO, click **Configure SSO → Authorize** for the token.
3. (Optional) Add an extra filter such as `org:my-company` to limit the board to your work org.

To try it without a token, click **Try the demo** or open `index.html?demo`.

> The token is stored only in that browser's `localStorage` and is sent only to `api.github.com`.

## Lanes

| Lane | Meaning |
|---|---|
| 📝 Draft | The PR is still a draft |
| 👀 Awaiting review | No review yet, or waiting on reviewers |
| 🔧 Changes requested | A reviewer requested changes or left unresolved comments, and the author hasn't updated yet |
| 🔁 Updated, re-review | The author pushed code, replied, or re-requested review after getting feedback |
| ✅ Approved | Approved with no open comments, ready to merge |
| 🎉 Done | Merged / closed in the last N days (configurable) |

The board has two rows (swimlanes): **My PRs** and **PRs I need to review / have reviewed**.
For PRs you review, the lane is from your point of view. For example, if you requested changes and the author hasn't pushed yet, the PR sits in "Changes requested" (waiting on the author). Once the author pushes, it moves to "Updated, re-review" and shows **🔥 Your turn**.

## What each card shows

- **🔥 Your turn / ⏳ Waiting on …**: who needs to act next
- **⏱ waiting Xd**: how long the PR has been in its current state (turns yellow/red past your thresholds, 24h / 72h by default)
- **📅**: how long the PR has been open
- **💬 2/5 resolved**: resolved review threads out of the total
- CI status, merge conflicts, and lines changed
- Reviewer avatars with their state: ✅ approved, ❌ changes requested, 💬 commented, ⏳ review pending

Click a card for details: last push and review times, each reviewer's status, and the **list of unresolved comments**, showing whether each is waiting on the author or the author replied and it's waiting on the reviewer.

## Other features

- Filter by role, repo, or search text. The **🔥 Your turn** chip shows only PRs waiting on you.
- Auto-refresh (every 5 minutes by default). Press `R` to refresh.
- The number of PRs waiting on you shows in the browser tab title, and you can turn on browser notifications.
- Reviews from bots (Copilot, CodeRabbit, etc.) are ignored when picking lanes (can be turned off in Settings).
- Dark mode and mobile layout.

## Limitations

- Uses the GitHub Search API: up to 100 PRs per search type.
- Review requests sent to a **team** you belong to count as yours.
- "Last push" is based on commit times and force-push events.
