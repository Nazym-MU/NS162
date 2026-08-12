---
id: NZ-48
title: Add the live match layer for fixtures and in-progress scores
category: project
project: manchester-united-site
milestone: live match layer
status: backlog
estimate: 90
visibility: public
done_when: the next fixture shows when no match is on and the current score shows during one, polling only while a match is actually in progress, with the real update lag measured against a live match and stated on the page rather than implied to be real time
blocks: [NZ-49]
created: 2026-08-12
---
Closes milestone 5. Polling only during a match is what keeps this inside a free tier;
a fixed interval running all week would exhaust the quota on nothing.

Stating the lag is honesty about what the free tier can do. A score that is two minutes
behind is genuinely useful, but presenting it as live is the kind of thing that gets
noticed during a match.
