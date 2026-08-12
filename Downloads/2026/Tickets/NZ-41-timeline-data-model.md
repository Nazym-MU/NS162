---
id: NZ-41
title: Write the United history timeline content as structured data
category: writing
project: manchester-united-site
milestone: history timeline teaches a newcomer
status: backlog
estimate: 90
visibility: public
done_when: a JSON or JS module holds every timeline entry with date, title, and a written blurb, covering the eras a newcomer needs (Busby Babes, Munich, 68 European Cup, Ferguson, 99 treble, post-Ferguson), with no placeholder text in any entry
blocks: [NZ-42]
created: 2026-08-12
---
Content before component. The milestone is "teaches a newcomer", so the writing is the
deliverable and the scroll behaviour is just how it gets read.

Writing it as data rather than JSX means the timeline component can be rebuilt or
restyled later without touching a word of the prose.
