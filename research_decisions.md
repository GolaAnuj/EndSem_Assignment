# Research decision ledger — 2026-11-17

Labels: **VERIFIED** = checked in provided source/real execution; **INFERRED** = interpretation needing wider validation; **UNKNOWN** = unverified/not performed.

| Decision | Reason | Evidence/status | Next check / responsible action |
|---|---|---|---|
| Keep original citation/trust area | Assignment requires continuity | VERIFIED review pages 1, 6–10 | Student can explain review argument |
| Study metadata accuracy rather than actual readers' trust | No participant sample or ethics/time available | VERIFIED no participant data; INFERRED scope is feasible | Never generalize to trust; future HCI experiment |
| Select pathway B: controlled comparison | Published manual verifications and source-checking motivate executable study | VERIFIED review sec 5.1, section 7; verified original Walters and Bhattacharyya pages | Explain not reproduction of published code |
| Use 12 listed records in frozen local registry | No network access needed for benchmark | VERIFIED CSV + web landing pages, evidence ledger | Student re-check fields/venue as needed |
| Predefine 11 transformations and five seeds | Prevent selecting favorable conditions after seeing results | VERIFIED config snapshot hash in manifest | Any updates require version bump and rerun |
| Use 'no contradictory metadata' binary label | Missing DOI is not necessarily evidence of a false work | INFERRED reasonable but contestable labeling | Document truncation ambiguity |
| Include 3 baseline checks | Separate superficial appearance / DOI existence / title existence from field consistency | VERIFIED code/tests | Discuss baseline scope and fairness |
| Add four field ablations | Isolate which supplied metadata fields catch which controlled corruptions | VERIFIED `results/ablation.csv` | Consider independent test samples |
| Do not use a train/test split | Model has no fitting; same source registry is required for local lookup | VERIFIED implementation | Report closed-world limitation prominently |
| Do not report novelty or statistical p-values | Deterministic fixed set and repetitions are not independent human outcomes | VERIFIED bootstrap intervals degenerate; INFERRED external validity unknown | Future work needs independent data |
| Log tools genuinely used | Course asks AI audit and code-origin tracing | VERIFIED this assistant created code and ran Python / pytest / pdflatex | Student must check and take ownership |

## G1 gate — one-page decision brief

- **Original topic:** Citation-format cues, fabricated references and human trust (prior review, pp. 1–10).
- **Original papers:** Putnam & Phelps (2017); Walters & Wilder (2023); Bhattacharyya et al. (2023); Kim et al. (2025); Kubiszewski et al. (2011).
- **Computational limitation from review:** A DOI or complete-looking citation is not equivalent to checking metadata agreement (review sec 5.1 and 7.4); review specifically separates existence, accuracy and claim-level support.
- **Primary question:** Does a multi-field metadata check reduce false acceptance of controlled citation conflicts relative to appearance/identifier/title existence checks?
- **RQ2:** Which fields matter in the controlled corruption benchmark? **RQ3:** What kinds of noncontradictory incomplete citations are falsely rejected?
- **Pathway:** B — controlled comparative study, not algorithmic novelty.
- **Data:** 12 real publication records from review; 11 variants/source; five seeds; no restricted raw data.
- **Comparators:** appearance-only, DOI-in-local-registry, title-in-local-registry, field-consistency method.
- **Primary:** macro-F1; **Secondary:** conflict recall, false accepts/rejects, time, per-corruption analysis.
- **Compute:** small CPU, standard Python; no GPU required. Risk: small closed-world benchmark and synthetic corruptions.
- **First runnable gate:** `pytest` and `run_experiment.py`, successful logs in `results/`.
