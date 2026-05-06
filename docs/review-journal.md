# Review Journal

The cases below are the review handles I would use before changing the implementation.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its cli tools focus without claiming live deployment or external usage.

## Cases

- `baseline`: `file span`, score 188, lane `ship`
- `stress`: `terminal width`, score 97, lane `hold`
- `edge`: `argument risk`, score 220, lane `ship`
- `recovery`: `report density`, score 205, lane `ship`
- `stale`: `file span`, score 213, lane `ship`

## Note

A future change should add new cases before it changes the scoring rule.
