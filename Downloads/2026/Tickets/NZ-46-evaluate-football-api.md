---
id: NZ-46
title: Evaluate a free football API for squad stats and fixtures
category: project
project: manchester-united-site
milestone: player stats page
status: backlog
estimate: 60
visibility: public
done_when: one API is chosen with a working key, and a written note records its free-tier request limit, how far behind live its score updates actually run, whether per-player season stats are on the free tier at all, and whether its terms allow displaying the data on a public site
blocks: [NZ-47]
created: 2026-08-12
---
A spike, deliberately ahead of both the stats page and the live layer, because the
answer changes what those milestones can promise.

Free football APIs commonly gate per-player stats behind a paid tier while advertising
"free squad data", and live scores often lag by minutes rather than seconds. Both are
worth knowing before building a page whose whole premise is live data. The terms check
matters because this site is public.
