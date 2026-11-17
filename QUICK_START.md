# QUICK START FOR COLAB AND VIVA

## Google Colab (standalone notebook)

1. Go to https://colab.research.google.com/ and choose **File → Upload notebook**.
2. Upload `notebooks/Citation_Metadata_Verification_Colab.ipynb`.
3. Click **Runtime → Run all** (CPU runtime is sufficient; no GPU, no API key and no external data download).
4. At the bottom, review the comparison table, figures and zipped `CitationAudit_Colab_Output.zip` (download will be attempted inside Colab).
5. Check your result: on the frozen synthetic benchmark the F1 values should be **0.333 / 0.667 / 1.000**, in the order strict / title-only / metadata-aware. These values are a *sanity check*, not real-world accuracy.

The standalone notebook also contains the post-hoc stress evaluation. A working internet connection is only necessary if Colab lacks a required Python package. Colab-installed versions may differ from this local environment; the notebook prints version information.

## Local reproduction

```bash
python -m pip install -r requirements.txt  # TEST REQUIRED on your system
python -m unittest discover -s tests -v
python scripts/run_experiment.py
python scripts/run_stress_test.py
```

## Overleaf

Create a new blank project and upload the contents of `paper/` including `main.tex`, `references.bib` and the `figures/` directory. Set `main.tex` as the main file; compiler **pdfLaTeX**, bibliography tool **BibTeX**. The PDF included in this ZIP was already compiled locally. **No external figures need uploading.**

## Important viva correction

The problem studied is **metadata consistency**, not human belief. The 650 cases are **algorithmically constructed variations of 13 real bibliographic records**. No participants were recruited; no real model-generated references were audited. A score of 1.0 here does not demonstrate universal accuracy; the extra stress test found 5/13 metadata-aware false acceptances after an altered title prefix.

## Key files

- `paper/main.pdf`: paper to inspect/submit as appropriate.
- `ALL_18_PROMPTS_SOLUTIONS.pdf`: complete 18-prompt written deliverable.
- `notebooks/Citation_Metadata_Verification_Colab.ipynb`: runnable Colab notebook.
- `results/results.csv`: real primary metrics.
- `results/figures/`: source-generated plots.
- `docs/viva_guide.md`: explanation questions and answers.
