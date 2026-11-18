# Turkey_PM output (placeholder folder)

This folder is organizational/student-facing only - it does not hold
any real output files yet, the same as every other country's
`output/README.md` in the Canada blueprint structure. Nothing should be
copied into it.

## Real output locations (once real Turkey_PM research has run)

- `data/processed/turkey_pm_assignment1/` - full staging-schema audit
  trail for a real research run.
- `data/processed/turkey_pm_pm_approval_main.csv` / `..._review.csv` -
  the visualization-ready APPROVED/REVIEW datasets (local run) that
  `python/resolve_assignment_dataset.py` and
  `python/build_country_assignment_snapshot.py` look for by default.
  These default filenames currently assume a Prime-Minister-shaped
  pipeline (a convention inherited from the Canada blueprint) - if
  Turkey_PM's office is not a Prime Minister, pass that script's
  explicit `--*-input`/`--local-path`/`--tracked-path` overrides
  instead of assuming the default names apply.
- `countries/turkey_pm/data/turkey_pm_assignment1_approved.csv` /
  `..._review.csv` - tracked worked-example snapshot, once built by
  `python/build_country_assignment_snapshot.py`.
- `data/processed/visualizations/` - generated charts.

`python/resolve_assignment_dataset.py --country Turkey_PM --purpose
approved` (and `--purpose review`) is the single deterministic decider
for which file answers a student's question, exactly as it is for every
other country.
