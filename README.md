# AITR Lab 02 — Citation Metadata Verification (Nov 17, 2026)

**Research topic carried forward:** *The Influence of Citation Formatting on Human Trust in Fabricated References* (previous literature review included in `evidence/`).

**Implementation study:** *From Citation Appearance to Metadata Consistency: A Controlled, Reproducible Benchmark*.

## Key finding from actual local runs

12 scholarly records × 11 labelled variations × 5 deterministic seeds = **660 evaluations per method**. The four classifiers were evaluated on identical cases. Macro-F1: appearance-only **0.267**, DOI-existence **0.267**, title-existence **0.411**, and multi-field comparison **0.906**. The proposed method made **0 false accepts**, but **60 false rejects** (one shortened-title case per paper × 5 seeds). See `results/run_console.log` and `results/all_predictions.csv`.

**Important:** This is a small, closed-world, deterministic **synthetic-error benchmark** based on 12 real cited scholarly records. The errors were constructed by code. We did NOT collect real LLM-fabricated references, recruit readers, measure human trust, check claim-level citation support, or query live Crossref. No result should be described as measuring those outcomes. The benchmark uses source metadata both to generate cases and as the verifier's known registry; it is **not an out-of-sample predictive evaluation**.

## Repo map

| Location | Contents |
|---|---|
| `evidence/` | your review + assignment PDF, `sources_checked.md` |
| `data/primary_records.csv` | manually curated 12 source records; official publisher/PMID source links |
| `configs/frozen_protocol.json` | predeclared questions, methods, labels, seeds and metrics |
| `src/benchmark.py` | 11 deterministic conditions per original citation |
| `src/verification.py` | three baselines, multi-field check and four ablations |
| `scripts/run_experiment.py` | runs experiment, produces raw CSVs, metrics and plots |
| `scripts/demo.py` | small interactive-free viva demonstration |
| `results/` | genuine CSV, CLI log, pytest log, PNG/PDF figures, timings and manifest |
| `paper/main.tex` | editable IEEE-style implementation paper |
| `paper/final_paper.pdf` | compiled manuscript |
| `prompts/01_to_18_execution_workbook.md` | evidence-grounded response to each of all 18 prompts |
| `research_decisions.md` | critical choices and evidence status |
| `baseline_validation.md` | check against specified behavior and limitations |
| `ai_assistance_log.md` | authentic assistance and verification; no invented experiences |
| `viva/` | five-minute outline, example explanations and practice Q&A |
| `tests/` | actual executable sanity/unit tests |

## Reproduce (Linux / macOS / Windows Terminal, Python 3.11+)

```bash
python -m venv .venv
# Linux/macOS: source .venv/bin/activate
# Windows PowerShell: .venv\Scripts\Activate.ps1
pip install -r requirements.txt
python -m pytest tests -q
python scripts/run_experiment.py
python scripts/demo.py
python scripts/compile_paper.py
```

The above `pytest`, experiment and demo **were executed successfully here** on Python 3.13.5 with the versions pinned in `requirements.txt`. Setting up a new environment and running on Google Colab / Windows is **[TEST REQUIRED]**. LaTeX compilation was tested with `pdflatex` and `bibtex.original` (the standard `bibtex` link is broken in this execution environment) on the generated paper; the compile helper handles either available executable. A network connection is **not required** for core experiments.

For one-line check of output integrity, read `results/run_manifest.json` for SHA256 of registry and frozen protocol. Code and research outputs were generated in an AI-assisted environment and require review by the submitting student. No GitHub remote has been created; **you must create and push the repository** if required by the instructor.

## Binary labels and interpretation

* `1` = metadata fields do not contradict the known record. An absent DOI or shortened title may still be a partial, noncontradictory citation.
* `0` = at least one field deliberately conflicts with the known record.
* DOI existence means *exists in this 12-record local index*, not internet-wide validity.
* Authors and titles were reviewed against linked publisher/medical index pages before construction; see evidence ledger. The corpus is deliberately small and topic-concentrated.

No study participants, ethical approval, survey responses or human-effect claims are implied.

## Academic ownership / submission

Use the attached paper, results and logs to study for the viva. You must inspect and take responsibility for the code and should independently check the publication metadata if submitting as your research. Cite the prior work and disclose AI involvement. The current author information carries through from the attached review; replace if needed. Avoid claims of novel algorithms or external generalization.
