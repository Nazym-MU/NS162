---
id: NZ-42
title: Build the scrollable timeline component from the entry data
category: project
project: manchester-united-site
milestone: history timeline teaches a newcomer
status: backlog
estimate: 90
visibility: public
done_when: the timeline renders every entry from NZ-41 in chronological order, is navigable by scroll on both desktop and a phone viewport, and adding a new entry to the data file makes it appear with no component change
blocks: [NZ-43]
created: 2026-08-12
---
Renders whatever NZ-41 wrote. The data-driven check is in `done_when` because a
timeline with entries hardcoded in the markup looks identical on screen and is the
thing that makes every later edit painful.

Phone viewport matters here specifically: a horizontal timeline that works on a laptop
often collapses into something unusable at 390px wide.
