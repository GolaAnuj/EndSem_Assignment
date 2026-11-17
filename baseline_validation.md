# G2 Baseline validation report

## Baseline identity and provenance

These are **controlled baseline heuristics devised for this study**, not faithful reimplementations of an algorithm published by Putnam & Phelps, Walters & Wilder, or Bhattacharyya et al. Their published studies supply the research motivation and manual checking concepts, not the code. Thus: *published-method reproduction NOT CLAIMED*.

1. **Appearance-only:** accept if reference has title, surname, four-digit year and a plausible DOI pattern. It checks surface form, not publication accuracy.
2. **DOI-existence:** accept if its DOI appears in the frozen 12-record registry. A wrong DOI copied from another valid paper still passes.
3. **Title-existence:** accept if normalized title appears anywhere in local registry. A title swapped from another existing paper passes.
4. **Multi-field:** find candidate by DOI (or uniquely matching title if no DOI), then compare title, first-author surname, year and venue after controlled normalization.

## Executed tests

`python -m pytest tests -q` → **11 passed** (see `results/pytest.log`). Controlled unit tests check canonical acceptance, DOI parsing, source-key uniqueness, no-DOI positive, switched-author and switched-DOI negatives, short-title failure and seed-label consistency. Full experiment logged to `results/run_console.log`.

## Validation status

- **VERIFIED:** all 12 clean references accepted by multi-field method; all 12 missing-DOI references accepted when other metadata is consistent; all changed-author and changed-DOI examples flagged as conflicts; five-seed runs executed.
- **VERIFIED:** title truncation is a documented **false rejection** case, not a bug to hide; 12 cases × 5 seeds = 60 false rejections.
- **VERIFIED:** the appearance and DOI baselines have identical predictions in this designed benchmark; this is a property of case construction, not proof they are generally equivalent.
- **UNCERTAIN:** whether a shortened title should always be labelled noncontradictory; the operational definition is explicit but could be contested.
- **UNCERTAIN:** external metadata conventions for multilingual titles, author disambiguation, multiple DOI aliases, corrections and preprints.
- **NOT VALIDATED:** live Crossref search, unrestricted global DOI validity, claim entailment or reader behavior, accuracy on external data.

## Discrepancy checks

Unlike a learning baseline, no published target accuracy can be used. Verification means the heuristic agrees with its specification and responds to known positive/negative controls; it does **not** mean it matches a published study's numeric results. The paper includes the actual implementation restrictions.
