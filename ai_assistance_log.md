# Human-AI Assistance and Integrity Log

**Tool and disclosure:** ChatGPT/GPT-6 assisted in designing the controlled study, generating code, testing locally, creating figures, interpreting logs, drafting report and preparing the ZIP. User provided the prior review, the course instruction PDF and the request to complete the project. This file does **not** assert that the user authored the AI-created code or independently checked each source. The final scientific judgment, verification and submission remain the student's responsibility.

| Task / actual prompt context | AI proposal / artifact | Evidence of execution or source | Human verification status |
|---|---|---|---|
| Interpret 18-part assignment | Deliverables and milestone folders | Uploaded instruction PDF, 11 pages | Student has not independently confirmed in this chat |
| Convert review to testable topic | Computerized bibliographic metadata consistency | Uploaded 7-page review; source references extracted | Student choice of narrower method not confirmed |
| Specify study | Frozen 13-source, 5-seed controlled comparison | `configs/frozen_protocol.json`, generated before first local run | Student should inspect thresholds and assumptions |
| Generate code and unit tests | `src/study.py`, 8 tests | Actual `results/unit_test_console_log.txt`; local pass | Student needs code walkthrough |
| Execute main experiment | 650 cases; 4550 predictions; metrics, figures | Actual `results/experiment_console_log.txt`, CSVs, PDFs | Student cloud rerun pending |
| Assess weakness of perfect initial metric | Separate changed-title stress diagnostic | Actual `exploratory_stress_test.csv` + stdout: 5/13 metadata-aware false accepts | Added post-hoc, labeled exploratory |
| Draft IEEE-style manuscript | `paper/main.tex`, `references.bib` and PDF | LaTeX locally compiled; primary output traceable | Student should read and approve claims |
| Generate notebook and documentation | Self-contained notebook, README, logs, viva | Notebook locally execution-tested if `docs/notebook_run_report.md` is present | Student Colab execution pending |

## Three genuine, documented limitations/verification interventions

1. **Source provenance:** Only R04, R12 and R13 were independently spot-checked through publisher/PubMed during generation. The other ten were kept explicitly `review_transcribed`, instead of falsely claiming every DOI was verified.
2. **Scope correction:** The review's human trust question was narrowed to offline metadata agreement because no human experimental data were supplied or generated. The manuscript explicitly excludes human trust claims.
3. **Overly good benchmark signal:** Initial field-aware F1 was 1.000 on easy synthetic cases; a separately labeled post-hoc prefix alteration was executed and caused 5/13 false acceptances. This failure is reported, not hidden.

## Missing real events — NOT fabricated

No personal student debugging tracebacks, Git commit hashes, user-run Colab logs, human participant recruitment, participant consent, real AI citation hallucination samples, or instructor feedback have been supplied. The generated code and verification logs are authentic local tool outputs; they are not represented as the student's prior history.
