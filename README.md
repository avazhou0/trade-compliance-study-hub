# Trade Compliance Study Hub

A self-study site for building trade compliance knowledge one lesson at a time —
import & customs, free trade agreements, export controls, and how to run an
effective compliance program. Each lesson takes about 5–15 minutes: read the
idea, listen to the companion podcast episode, then test yourself (answers are
tucked into tap-to-reveal boxes so you can self-quiz first).

🌐 **Live site:** https://avazhou0.github.io/trade-compliance-study-hub/

## What's inside

- **`index.html`** — the hub itself: all lessons with text, audio players, and paired Q&A.
- **`audio/`** — one podcast MP3 per lesson (`dayN.mp3`), companions to the written lessons.
- **`playbooks/`** — standalone reference editions beyond the lesson sequence, e.g. the
  *Early-Stage Trade Checklist* (10 things trade should weigh in on before design and
  sourcing lock, to save duties).

## How it's built

The site is generated from `files/learning-log.md` (one `## Lesson N` section per lesson)
by `build_study_hub.py` in the goal workspace:

```bash
python3 build_study_hub.py --web-dir ./site
```

New podcast episodes land in `site/audio/dayN.mp3` with their titles recorded in
`hidden_files/episode_titles.json`; the build picks them up automatically.

## Cadence

- A new **lesson** arrives every other morning, with a companion **Trade Talk** podcast
  episode generated the same day. The site refreshes automatically on that schedule.

## Podcast

*Trade Talk* — hosts Alex and Jordan walk through each lesson conversationally
(~4–6 minutes per episode). Episodes live only on this hub; nothing is published
to Spotify or any feed without explicit approval.

## Notes

- Lesson answers shown on the hub are the proper reference versions.
- Audio filenames (`dayN.mp3`) are internal only; everything user-facing uses "Lesson N".
