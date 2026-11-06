# Metro Pulse

Prototype for the Hot Takes Junior Product and AI Engineer assignment, Challenge 1A.

Three conventional metro survey questions rebuilt as three short games. Everything is in one file, `index.html`, with no build step. Open it in any browser, or host it as a static page.

## The three questions and their games

| Original question | Game | What it captures that the original misses |
| --- | --- | --- |
| How satisfied are you with station cleanliness? | Clean-up crew: tap the areas used on the last trip, spend 3 cleaning visits, name the problem at each | Which areas were actually used, the order of problems when resources are limited, the type of dirt |
| How crowded are the trains on your commute? | Skip or board: pick the carriage picture that matches a stated trip, then the fullest carriage you would board with a 3 min and a 10 min wait | Real density by time slot, how much crowding people accept as the wait changes |
| Do you think metro fares are reasonable? | Trade-off tickets: four rounds choosing between an express ticket and a local ticket, with an adaptive extra fare | Willingness to pay per hour saved, from choices instead of an opinion |

The Design notes tab in the page gives the rationale for each redesign and answers the three questions in Part A.

## Quality and engagement logging

Every tap, change of mind and commit is logged with timing (see the Live data tab). `score(events)` in `index.html` computes:

- Quality (0 to 100) = 40 pace + 40 consistency + 20 pattern
- Engagement (0 to 100) = 40 completion + 30 deliberation + 30 depth

Flags: rushed steps, tap-all, inconsistent thresholds, failed attention round, same side every round.

## Run locally

Open `index.html` in a browser. Fonts load from Google Fonts and fall back to system fonts when offline.

## Playable link

https://khushi-h.github.io/Metro-Pulse/
