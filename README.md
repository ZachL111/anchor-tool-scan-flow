# anchor-tool-scan-flow

`anchor-tool-scan-flow` explores cli tools with a small Python codebase and local fixtures. The technical goal is to package a Python local lab for scan analysis with deny and allow fixtures, explainable decision traces, and documented operating limits.

## Use Case

I want this repository to be useful as a quick reading exercise: fixtures first, implementation second, verifier last.

## Anchor Tool Scan Flow Review Notes

The first comparison I would make is `argument risk` against `terminal width` because it shows where the rule is most opinionated.

## Highlights

- `fixtures/domain_review.csv` adds cases for file span and terminal width.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/anchor-tool-scan-walkthrough.md` walks through the case spread.
- The Python code includes a review path for `argument risk` and `terminal width`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Code Layout

The repository has two validation layers: the original compact policy fixture and the domain review fixture. They are separate so one can change without hiding failures in the other.

The Python code keeps the review rule close to the tests.

## Run The Check

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Regression Path

The check exercises the source code and the review fixture. `edge` is the high score at 220; `stress` is the low score at 97.

## Future Work

No external service is required. A deeper version would add more negative cases and a clearer boundary around invalid input.
