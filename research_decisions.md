# Research Decisions Log — Prompt 01

**Course:** AI Tools for Research  
**Checkpoint:** Prompt 01 — Set up an accountable research workspace  
**Status:** Initial workspace and review-scope summary prepared; implementation and experiments have not started.  
**Research topic:** *The Influence of Citation Formatting on Human Trust in Fabricated References*

## 1. Review basis and scope

The review supplied for this workspace is titled **“The Influence of Citation Formatting on Human Trust in Fabricated References: A Review of Citation Cues, Illusory Credibility, and the Emergence of AI-Fabricated Citations.”** The portable project copy is in `review_basis/`. This scope summary is based on the supplied review; it does not assume that experiments, datasets, or code exist beyond the files provided.

The review brings together two strands of research:

1. **Cognitive and communication research on citation/source cues.** This includes the citation effect, processing fluency, truthiness/illusory truth, peripheral persuasion cues, and online-source credibility.
2. **Empirical work on AI-generated fabricated or inaccurate references.** This includes studies measuring how often LLM-generated bibliographic references are nonexistent or contain incorrect metadata.

It also reviews candidate countermeasures: automated citation verification, clickable or retrieval-grounded sources, lateral reading, cognitive forcing, and editorial/institutional policies.

### Central issue in the review

A reference can look conventionally scholarly without being accurate or even existing. Readers may treat author-year text, complete bibliographic fields, journal names, or identifiers such as DOI/PMID as cues of credibility. The core unresolved issue is whether **specific formatting features**, independently of citation presence and actual source support, change trust in a fabricated reference—and whether readers actually verify the source.

### What the review does and does not contain

- It is a **literature review**, not a report of a new experiment by this student.
- It contains reported findings from prior studies. Those values must remain attributed to their original studies and must not be presented as results from this proposed project.
- It identifies research gaps, but gap statements are not proof of novelty. They need to be checked against relevant work published after and outside the review's search scope.
- The supplied files do not establish a participant pool, ethics approval, data access approval, chosen implementation platform, available compute, or completed code execution.

## 2. Key evidence noted in the review

### Citation effect

Putnam and Phelps (2017) reported six experiments. The review reports a small effect on truth judgments (`d = 0.13`, 95% CI `[0.06, 0.20]`) when claims were presented with citations versus without them. **Status: VERIFIED** against the review and primary-source abstract. This concerns citation presence, not a complete factorial test of DOI/PMID or metadata completeness.

### AI citation fabrication

Walters and Wilder (2023) analyzed 636 citations across 42 multidisciplinary topics. The review reports 55% of GPT-3.5 citations and 18% of GPT-4 citations were fabricated, as well as substantive errors among non-fabricated citations. **Status: VERIFIED** against the primary-source abstract. Exact denominators and definitions for each percentage should be rechecked in the paper's tables before any new quantitative analysis.

### Medical references

Bhattacharyya et al. (2023) analyzed 115 ChatGPT-generated references; the review reports 47% fabricated, 46% authentic but inaccurate, and 7% authentic and accurate. **Status: VERIFIED** against the primary-source abstract. These are generation/reference-accuracy outcomes, not direct measurements of human trust.

### Sources and reliance

Kim et al. (2025) report a preregistered controlled experiment (`N = 308`) on explanations, sources, and inconsistencies in LLM answers; the review summarizes that sources can reduce reliance on incorrect answers. **Status: VERIFIED at the abstract level.** Read the full methods and results before translating it into a citation-format-specific design.

### Lateral reading

Wineburg and McGrew (2019) compare source-evaluation strategies among fact-checkers, historians, and students. The review proposes applying lateral reading to citation verification. The original study supports the general source-evaluation strategy; a citation-specific training effect is still an **INFERENCE** from the review, not an established result.

Primary-source links and remaining verification actions are recorded in `source_verification_register.md`.

## 2A. Methods, data sources, and measurements identified

The reviewed literature uses several different designs; the supplied review does not identify one shared benchmark dataset spanning all of them.

- **Citation-presence experiments:** Putnam and Phelps (2017) used true and false trivia claims presented with or without in-text citations, then collected truth-likelihood judgments across six experiments. Their reported summary effect is `d = 0.13` (95% CI `[0.06, 0.20]`). The input items are study-specific trivia statements, not a general citation-format benchmark.
- **Generated-reference audits:** Walters and Wilder (2023) generated short literature reviews for 42 multidisciplinary topics, then checked 636 references from 84 generated papers. Outcomes included whether a work existed, whether a real reference contained substantive metadata errors, and citation-format adherence.
- **Medical-reference audit:** Bhattacharyya et al. (2023) prompted ChatGPT-3.5 to generate 30 short medical papers and assessed 115 references using bibliographic resources including Medline, Google Scholar, and DOAJ. Outcomes included authenticity and accuracy of reference fields.
- **Other fabrication-rate studies:** The review summarizes Athaluri et al. (2023) and MacDonald (2023) as studying AI-generated references in scientific-writing or psychology contexts. Before using these for a new corpus, inspect their full methods, item-level data, denominators, and supplementary files; the review alone does not establish that their stimuli are downloadable or reusable.
- **Source/reliance experiment:** Kim et al. (2025) studied the effect of explanations, sources, and inconsistencies on user reliance on LLM answers (`N = 308`). This is an HCI/user-study design rather than a reusable dataset of citation-format stimuli.
- **Online-source evaluation:** Wineburg and McGrew (2019) studied how fact-checkers, historians, and students evaluated unfamiliar websites. It provides a theoretical/intervention lead for lateral reading, not direct measurements of trust in fabricated references.
- **Adjacent work located after the prior review:** Ding et al. (2025) varied citation count and relevance in LLM-generated responses and measured user trust/checking. It is an important comparator to inspect in full.

**Dataset conclusion:** The reviewed evidence consists mainly of study-specific claims, generated reference lists, and controlled user tasks. A common, verified public dataset of genuine and fabricated references with ground-truth labels is **not established by the supplied review**. Whether published supplements can be reused, and whether a benchmark exists in newer work, remains **UNKNOWN** pending source-by-source inspection.

## 3. Evidence ledger

### VERIFIED

- The supplied review explicitly distinguishes citation presence from specific citation formatting and identifies limited causal evidence for completeness, identifier presence, and citation style (review Sections 3, 5, and 6; section labels in `review_basis/main.tex`).
- The review reports that much of the AI-fabrication literature measures fabricated/inaccurate-reference rates rather than how humans judge those references (Sections 2.4 and 5).
- The review identifies short trivia tasks and convenience samples as limits on generalizing to long-form scholarly and higher-stakes contexts (Section 5).
- The primary-source pages checked for Putnam and Phelps (2017), Walters and Wilder (2023), Bhattacharyya et al. (2023), Kim et al. (2025), and Wineburg and McGrew (2019) support the broad summaries above.
- A targeted update search located **Ding et al. (2025)**, which studies citation count/relevance and trust in LLM-generated responses; and **Cho and Lim (2026)**, which studies source-attribution visualization. These findings mean that broad claims such as “citation presence and visual source presentation have never been experimentally studied” would be too strong.

### INFERRED

- A focused study that manipulates **metadata completeness and DOI/PMID presence** while also varying actual source status could be a useful extension of the prior review, provided a full literature search confirms that the exact comparison has not already been done.
- Logging actual checking behavior (clicks/searches/verification actions) alongside self-reported trust may help distinguish a visual credibility cue from completed source verification.
- A controlled, browser-based survey or task could make the first study operationally testable with modest computational resources, but this is a design option—not a selected or approved protocol.

### UNKNOWN

- Whether a comprehensive search of ACM, Scopus/Web of Science, Google Scholar, PsycINFO, and relevant HCI/communication venues finds a prior experiment manipulating the same formatting factors.
- Whether the student can recruit participants, whether institutional ethics/consent requirements apply, and whether approval is required before collecting judgments.
- Whether the documented fabricated citation stimuli from earlier studies can be extracted and reused appropriately, including licensing/permissions and stimulus-selection rules.
- The available time, platform, compute budget, sample size, and accessibility of any required datasets or original supplementary material.
- The exact best primary research question and final study pathway; these should be selected only after feasibility/novelty checks.

## 4. Decision log

### D01 — Keep the topic continuous with the prior review

- **Decision:** Keep the project focused on citation formatting and trust in fabricated references.
- **Reason:** The post-mid-semester assignment requires continuity with the completed review.
- **Evidence/status:** **VERIFIED** from the assignment instructions and supplied review.
- **Next action:** Use this topic in the gap matrix; do not pivot to an unrelated ML problem.

### D02 — Use the prior ACM review as the traceable evidence base

- **Decision:** Use the ACM-formatted review and its source LaTeX/BibTeX as the main review basis.
- **Reason:** It preserves the review's sections, citations, and explicit limitations in a portable form.
- **Evidence/status:** Files are included under `review_basis/`.
- **Next action:** Refer to specific section/subsection labels when justifying each gap.

### D03 — Separate source limitations from proposed interpretations

- **Decision:** Label the limitations explicitly stated in the review separately from interpretations proposed here.
- **Reason:** A review's proposed research direction is not proof that no related study exists.
- **Evidence/status:** **VERIFIED** as a research-integrity requirement in Prompt 02.
- **Next action:** Keep separate labels for reported limitation, inference, and evidence needed in every gap entry.

### D04 — Do not claim novelty yet

- **Decision:** Do not claim the topic or exact gap is novel at this stage.
- **Reason:** A targeted search found adjacent studies on citation quantity/relevance and source-visualization layouts.
- **Evidence/status:** **VERIFIED** at search-result/abstract level; full overlap analysis remains **UNKNOWN**.
- **Next action:** Perform a systematic novelty check before freezing the G1 research question.

### D05 — Keep GAP 01 as the leading candidate, conditionally

- **Decision:** Rank a controlled test of metadata completeness/identifier cues as the leading candidate, subject to novelty, participant, and ethics feasibility.
- **Reason:** It most directly addresses the specific unresolved variable highlighted by the review and can use a small experimental interface plus analysis code.
- **Evidence/status:** **INFERRED** candidate; not an approved design.
- **Next action:** Check prior work, participant availability, and ethics requirements before selecting it.

### D06 — Do not report experiment outputs

- **Decision:** Keep empirical outcomes blank/not applicable for this checkpoint.
- **Reason:** No new code or experiment was run for Prompts 01-02.
- **Evidence/status:** **VERIFIED** from work performed in this checkpoint.
- **Next action:** Do not insert assumed sample sizes, metrics, p-values, results, or screenshots.

## 5. Immediate next actions (limited to this checkpoint)

1. Read `gap_matrix.md` and confirm that the five candidate gaps are all genuinely connected to the review.
2. Verify the exact primary-paper methods and tables for any quantitative claims that might inform a future stimulus set.
3. Run a deeper novelty search specifically for experiments that manipulate citation completeness, DOI/PMID visibility, citation style, source authenticity, and human trust.
4. Confirm participant/ethics feasibility before choosing a human-subjects experiment. If participants or approval are not feasible, consider a narrower computational audit of reference verifiability—but do not describe its output as a measure of human trust.

**Out of scope this week:** Prompt 03 and later prompts, finalized experimental protocol, coding, baseline implementation, data collection, experiments, results, and the second research-paper draft.
