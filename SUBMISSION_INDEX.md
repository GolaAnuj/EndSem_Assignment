# Submission index — AITR Lab 02, citation metadata study

This archive includes the original course instruction PDF and earlier narrative review for provenance. The supplied study is a controlled **metadata consistency** pilot; it does **not** measure human trust. Its inputs and experimental error cases are clearly distinguished.

## Deliverables mapped to the course submission checklist

A. **Research paper:** `paper/main.pdf` (6 IEEE-style pages), `paper/main.tex`, `paper/references.bib`, `paper/figures/*.pdf`. All original figure files preserved.

B. **Code repository:** `src/study.py`, `scripts/*.py`, `tests/test_study.py`, `requirements.txt`, `configs/frozen_protocol.json`, `README.md`, `LICENSE`. Self-contained notebook at `notebooks/Citation_Metadata_Verification_Colab.ipynb`.

C. **Experimental evidence:** `results/results.csv`, `metrics_by_seed.csv`, `predictions.csv`, `synthetic_test_cases.csv`, PNG/PDF figures, run manifest, actual stdout and local unit-test log, post-hoc challenge results.

D. **Research provenance:** `docs/one_page_research_brief.md`, `docs/baseline_validation.md`, `research_decisions.md`, `ai_assistance_log.md`, `data/README.md`, source metadata statuses.

E. **Demonstration:** `docs/viva_guide.md`, `docs/google_colab_how_to.md`, `QUICK_START.md`.

F. **Every AI prompt:** `prompts/Prompt_01.md` through `Prompt_18.md`, `ALL_18_PROMPTS_SOLUTIONS.pdf` and `.md`.

## Verified locally

- 8 passing Python unit tests, 650 deterministic controlled cases.
- 7 methods x 650 cases = 4550 genuine predictions.
- Source-level holdout F1 (strict 0.333, title fuzzy 0.667, metadata-aware 1.000), with correctly scoped limitations.
- Extra post-hoc altered-title stress test: 5/13 metadata-aware false accepts.
- Notebook locally executed end-to-end; actual result figures regenerated.
- Research paper locally compiled; 6 pages; all-prompt PDF rendered; 19 pages.

## Items that cannot be honestly represented as complete

- The student must independently verify the ten review-transcribed source entries and review/own the conclusions.
- Notebook execution in the student's hosted Google Colab account and GitHub publication on the student's account are not claimed.
- No human participants, human trust ratings, external corpus labels or API-resolved DOI tests were performed.

**Suggested first action:** review `QUICK_START.md` and run the standalone notebook in Colab. Keep all output and technical rationale for the viva.
