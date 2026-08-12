---
type: project
slug: manchester-united-site
title: Manchester United Fan Site
---
# Manchester United Fan Site

A dedicated site for Manchester United — separate from [[old-trafford]] (which is the
stadium scroll-story) but linked from it.

Built with React. This is a deliberate departure from Old Trafford's vanilla JS and
Three.js: that site is one scroll-driven 3D scene, this one is several distinct pages
with real state (timeline, music, stats, live scores).

## Milestones (in order)

1. **the letter opens** — the opening scroll experience exists: a letter that unfolds
   as you scroll, starting "Dear Manchester United," pouring out genuine love for the
   club. `done_when`: scrolling through the intro on a fresh load plays the full
   letter-opening animation with real (not placeholder) text.
2. **history timeline teaches a newcomer** — an interactive timeline of United's
   history someone with zero context could scroll through and come away actually
   understanding the club.
3. **the music page** — embedded Spotify playlists; clicking a song reveals the
   specific lyric lines that remind me of United.
4. **player stats page** — current squad stats, browsable.
5. **live match layer** — real-time score/fixture updates for United games.
6. **linked up** — a visible link over to [[old-trafford]], and Old Trafford links back.

Milestone 1 is active (NZ-17, the letter text, is all that remains of it). Milestones
2–6 are ticketed as NZ-41 through NZ-49 but sit in `backlog`, so the board still shows
one active milestone's worth of open work.

## Data sources

- **Timeline and music content is written by hand.** Lyric annotations especially: the
  point of the music page is what the lines mean to me, which no API supplies, and
  hand-writing them avoids the licensing question around displaying full lyrics.
- **Squad stats and live scores come from a free football API**, chosen in NZ-46. That
  spike gates both milestone 4 and milestone 5, because free tiers routinely put
  per-player stats behind a paywall and run minutes behind on live scores. What it
  finds decides what those two milestones can honestly promise.
