---
id: NZ-45
title: Build the music page with Spotify embeds and reveal-on-click annotations
category: project
project: manchester-united-site
milestone: the music page
status: backlog
estimate: 90
visibility: public
done_when: every song from NZ-44 renders as a Spotify embed, clicking one reveals its lyric lines and note, and the page is verified to still render the annotations when embeds are blocked by a tracker blocker or offline
blocks: []
created: 2026-08-12
---
Closes milestone 3. The Spotify iframe embed needs no API key or auth, which keeps
this a front-end ticket.

The blocked-embed check is in `done_when` because third-party iframes are commonly
blocked, and if the writing only exists inside the embed's shadow the page silently
becomes empty for those visitors. The annotations are yours, so they should survive
Spotify being unavailable.
