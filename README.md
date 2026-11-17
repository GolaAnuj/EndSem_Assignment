# AITR Lab 02: Citation Metadata Consistency Study

**Topic:** Experimental verification of citation metadata under formatting variation and controlled bibliographic errors.  
**Source:** Earlier narrative review, *The Influence of Citation Formatting on Human Trust in Fabricated References* (supplied by the student).  
**Research pathway:** **B — Controlled comparative computational study**, not a participant-based experiment or a replication of a specific published implementation.

## Read first

1. `QUICK_START.md` — fast local / Google Colab execution.
2. `notebooks/Citation_Metadata_Verification_Colab.ipynb` — **standalone Colab notebook**: contains its own seed records and code, no upload required.
3. `paper/main.pdf` — compiled 6+ page IEEE-style research manuscript (also in `main.tex` and `references.bib`).
4. `ALL_18_PROMPTS_SOLUTIONS.pdf` and `prompts/Prompt_01.md` ... `Prompt_18.md` — prompt-by-prompt research work.
5. `results/` — *actual locally executed* CSVs, figures, manifests, unit-test and experiment logs.
6. `docs/` — one-page research brief, baseline validation, data verification, peer review and viva support.

## Exact research question

Can a field-aware check that compares DOI, title, first-author surname and year against a small frozen bibliographic catalog better distinguish **consistent metadata** from **synthetically inconsistent metadata** than exact-string matching and title-only fuzzy matching, without rejecting harmless formatting changes?

This measures **catalog metadata agreement**, **NOT** whether a cited scientific claim is true, whether the paper exists outside the catalog, or how humans trust citations.

## Reproduce the locally observed experiment

From the **project root** in a Python environment:

```bash
python -m pip install -r requirements.txt
python -m unittest discover -s tests -v
python scripts/run_experiment.py
python scripts/run_stress_test.py
```

The commands above were executed in the authoring environment with the exception of the first installation command, which is **[TEST REQUIRED] on your machine** (libraries were already installed locally). Every main experiment output is regenerated in `results/`. The stress test is a separate **post-hoc exploratory diagnostic**, not part of the frozen primary result.

## Locally observed findings

13 reviewed source records × 5 seeds × (5 consistent + 5 inconsistent variants) = **650 cases**, evaluated by **7 methods**, yielding **4,550 predictions**. Five original references are held out at the *source ID* level (250 test cases with repeated perturbations). On this simplified holdout:

| Method | F1 ↑ | Recall ↑ | False acceptance ↓ |
|---|---:|---:|---:|
| Strict exact | 0.333 | 0.200 | 0.000 |
| Title fuzzy | 0.667 | 1.000 | 1.000 |
| Metadata-aware | 1.000 | 1.000 | 0.000 |

The perfect primary score results partly from the deliberately simple test generator and small closed catalog; **it is not evidence of perfect citation verification in practice**. The separate, post-hoc changed-title stress test produced **5/13 false acceptances** (38.5%) for metadata-aware matching. No participant ratings, real AI hallucination rates, or statistical significance claims are presented.

## Data and rights

`data/seed_references.csv` contains bibliographic metadata of 13 works cited in the student's own review; it does not contain article full texts. Three entries were independently spot-checked against public primary/publisher or PubMed records; **the remaining ten are review transcriptions requiring independent verification**. Constructed DOI test strings are not claims about DOI registry nonexistence. Review original copyright, dataset terms, third-party bibliographic metadata terms and campus research policies before redistribution or expansion. The source code is released under the permissive MIT license (see `LICENSE`); third-party sources retain their own terms.

## Repository structure

```
configs/     frozen research protocol
src/         reproducible experiment source
scripts/     local execution entrypoints
notebooks/   standalone Google Colab notebook
data/        review-derived seed metadata and source provenance
results/     measured predictions, metrics, plots, unit tests, run manifest
paper/       main.tex, references.bib, figure PDFs and compiled PDF
prompts/     all eighteen prompt responses
reviews/     not used (internal review is in docs/)
docs/        research brief, validation, viva, technical review
```

## AI assistance and ownership

ChatGPT/GPT-6 was used to draft the study design, code, experimental scripts, figure generation, prompt responses and manuscript, and to run and verify the code **in the present workspace**. No Git commits, Google Colab cloud runs, human participants, human judgments or student independent verification have been invented. See `ai_assistance_log.md` and `research_decisions.md`. The student should inspect the sources, understand and rerun the code and decide whether to adopt these experimental conclusions before submission.

## Reproduction checklist

- [x] Actual local unit-test run (8 tests pass).
- [x] Actual local baseline and comparison execution; predictions and plots exported.
- [x] Fixed parameters, 5 seeds, source-ID partition and documented generator.
- [x] Critical ablation and additional exploratory stress test.
- [x] Compiled IEEE-style manuscript and BibTeX file.
- [ ] **[TEST REQUIRED]** Re-execute on the student's own Google Colab account.
- [ ] **[VERIFY]** Cross-check remaining ten source-record DOI/title/author/year details against original registry or publisher entries.
- [ ] **[STUDENT ACTION]** Create a GitHub repository if the instructor requires its URL; no GitHub publication is claimed.
- [ ] **[STUDENT ACTION]** Read and defend all source and methodological choices.
