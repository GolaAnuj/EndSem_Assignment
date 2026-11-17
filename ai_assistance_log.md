# Research provenance and AI assistance log

**Tool:** ChatGPT (GPT-6 conversation, 2026-11-17) with Python interpreter/container, pytest, matplotlib, LaTeX and web lookup. Actual model-assisted development only; this is not a fabricated commit history. **No GitHub commits or repository publication have been made.** User supplied the 10-page literature review and 11-page assignment sheet.

| Work phase | AI suggestion/code | Decision & actual verification | Evidence | Outcome |
|---|---|---|---|---|
| Review-to-gap, prompts 01–05 | Narrowed human-trust review to verifiable citation metadata | Automated check cannot substitute for people; kept domain link and marked trust out of scope | Review sec 5.1, 7, original sources | Narrow feasible computational question |
| Corpus, prompts 06–07 | Curated 12 bibliographic records and 11 controlled transformations | Compared DOI metadata against original landing pages; froze protocol JSON | `evidence/sources_checked.md`, CSV, manifest hashes | Fixed, reproducible closed-world benchmark |
| Coding, prompts 08–10 | Created registry matcher, three heuristics, generator and 11 tests | Executed test suite and experiment in local environment | `results/pytest.log`, `results/run_console.log` | 11 passed; actual saved predictions |
| Debug review, prompt 11 | Requested examination of real failures | No genuine runtime exception observed in the final run; therefore **no imaginary bug/fix was logged** | Executed test/output files | Prompt 11 recorded as 'not triggered by a crash' |
| Comparison and ablation, prompts 12–14 | Generated four method comparisons and four ablations | Computed scores from CSV and produced figures; inspected failure modes | `results/results.csv`, `ablation.csv`, `per_condition.csv` | 0.906 macro-F1 (full) with documented shortened-title false rejects |
| Writing, prompts 15–16 | Drafted paper with limitations and evidence checklist | Tables/figures grounded in run outputs; static peer review and revisions logged | `paper/main.tex`, paper PDF, `evidence/technical_peer_review.md` | Manuscript and audit prepared; instructor review pending |
| Reproduce and audit, prompts 17–18 | Wrote runnable README, manifest and viva notes | Local environment and rerun commands validated; other systems NOT tested | README and logs | Portable artifact, NOT a published GitHub repo |

## Three real limitations / checks (not invented experiences)

1. **Research-scope check:** literature addresses *people’s trust*; code produces no participant outcomes. Correction: explicitly frame study as citation **metadata consistency**, not a trust-impact experiment.
2. **False rejection discovered:** truncating a title is labelled noncontradictory but the strict multi-field checker flags it as conflicting. Correction: preserve and explain the **60** cases rather than improve the threshold after viewing results.
3. **Uninformative uncertainty:** resampling the 12 identical per-source case patterns generates degenerate bootstrap intervals. Correction: treat CI files as descriptive diagnostics, **not** inferential confidence about external populations.
4. **Corpus dependency:** local environment cannot query Crossref; correction: maintain original landing-page URLs and say verification is against the **frozen local registry**, not live internet.

**Human ownership boundary:** The assistant made and executed these choices; they are not represented as independent actions performed by the student. The submitting student must read the code, recheck the sources and explain decisions before claiming ownership in the viva. No human-subject data, ethical approval, GitHub upload, manual student verification or independent student rerun is claimed.
