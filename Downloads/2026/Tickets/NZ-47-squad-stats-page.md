---
id: NZ-47
title: Build the squad stats page against the chosen API
category: project
project: manchester-united-site
milestone: player stats page
status: backlog
estimate: 90
visibility: public
done_when: the current squad renders with per-player stats from the NZ-46 API, responses are cached so a page refresh does not spend a fresh request, and the page shows a readable fallback rather than a blank grid when the API errors or the rate limit is hit
blocks: [NZ-48]
created: 2026-08-12
---
Closes milestone 4. Scope depends on what NZ-46 found: if per-player stats are not on
the free tier, this narrows to squad list plus whatever is available, which is a
finding rather than a failure.

Caching is in `done_when` because a free tier burns through its daily quota fast if
every visitor triggers live calls, and the failure mode is the page dying for everyone
until the window resets.
