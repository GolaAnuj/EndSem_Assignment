# AI Tools for Research - Prompt 01 and Prompt 02

## Checkpoint: Prompt 01 and Prompt 02

**Research topic:** The Influence of Citation Formatting on Human Trust in Fabricated References  
**Scope of this package:** Accountable research workspace and evidence-based research-gap extraction only.

This report uses the previously supplied review paper and its LaTeX/BibTeX source. No code or experiment was run for this checkpoint, no participants were recruited, and no new experimental results are reported. Novelty is **not claimed**; newer adjacent studies found in a targeted search must be examined in full before the research question is frozen.

\newpage
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

\newpage

# Evidence-Based Research-Gap Matrix — Prompt 02

**Review topic:** *The Influence of Citation Formatting on Human Trust in Fabricated References*  
**Purpose:** Identify five computationally testable candidate gaps from the supplied review, distinguishing the review's stated limitations from further inferences. This is a candidate-gap analysis, not a novelty claim and not an experimental result.

## How to read this matrix

- **Review evidence** points to a section/subsection in the supplied prior review, included in `review_basis/`.
- **Reported limitation** means the review explicitly states or summarizes the limitation.
- **Inference** is the proposed interpretation/question derived from that evidence. It requires further literature review and testing.
- **Evidence needed** identifies a possible future measurement; no such measurements have been collected for this assignment.

## GAP 01 — Do metadata completeness and identifiers independently affect trust?

**Priority:** 1 (leading candidate, conditional on novelty, participant, and ethics feasibility)  
**Type:** Controlled comparative study / small human-computer interaction experiment

**Review evidence**

- Section 2.2 reports Putnam and Phelps (2017): six experiments compared claims with and without in-text citations. The reported effect was small (`d = 0.13`, 95% CI `[0.06, 0.20]`). This manipulates citation presence rather than the full format of the citation.
- Section 3.1 distinguishes three dimensions: presence, completeness, and identifier specificity.
- Section 5 says the existing evidence largely manipulates citation presence/absence and does not isolate formatting details as independent variables.
- Section 6 explicitly recommends experiments varying completeness, DOI/PMID inclusion, and citation style while controlling other features.

**Reported limitation:** The review states that the specific causal contribution of citation completeness and identifier presence is not isolated by the set of studies it synthesizes.

**Inference / candidate question:** *When the surrounding claim and presentation are controlled, how do (a) author-year-only references, (b) complete references without an identifier, and (c) complete references with a DOI/PMID affect perceived credibility and the rate at which fabricated references are accepted as genuine?*

**Possible test and evidence:** Build a small browser-based randomized survey/task. Use real references and documented fabricated references selected and verified against the primary reports. Randomize formatting condition; record credibility ratings, real/fabricated judgments, confidence, and—if included in the approved protocol—verification actions. Analyze authenticity and format as separate factors and report uncertainty, exclusions, and stimulus-level variation. A matched/counterbalanced item design is needed because different source titles and author reputations can otherwise confound the result.

**Critical controls / risks:** The stimulus's true existence must be verified manually from primary sources; never manufacture fake data or invent a DOI. Avoid changing content and format together. The question involves human participants, so recruitment, consent, and any institute ethics review must be checked before collection. A small class convenience sample may not support broad population conclusions.

**Novelty check:** A targeted search found Ding et al. (2025), which experimentally studied citation count and relevance in LLM-generated responses, and Cho and Lim (2026), which studies source-attribution visualization. These make it important to define the gap narrowly: *metadata completeness/DOI/PMID visibility crossed with source authenticity*, not the broader claim that citation presentation has never been studied. Full-text comparison and a systematic search are required before any novelty claim.

**Feasibility:** Medium. Compute demands are low, but participant recruitment and ethics are gating constraints.

## GAP 02 — Do actionable sources change verification behavior beyond static formatting?

**Priority:** 2  
**Type:** Controlled interface study with interaction logging

**Review evidence**

- Section 3.3 summarizes Kim et al. (2025): in a preregistered controlled study (`N = 308`), sources and explanations influenced users' reliance on LLM responses; sources reduced reliance on incorrect responses.
- Section 4.2 discusses source-linking and retrieval-augmented generation, while noting that a link's existence does not ensure that its contents support the adjacent claim.
- Section 5 warns that the presence of a link or identifier should not be treated as equivalent to actual verification.
- Section 6 recommends measuring whether people click identifiers, search titles, or compare metadata.

**Reported limitation:** The review identifies the distinction between source availability and actual verification behavior, and calls for citation-specific study of this relationship.

**Inference / candidate question:** *Compared with a complete but static reference, does a clickable link to an independently verified bibliographic record improve detection of fabricated or mismatched references and reduce false acceptance?*

**Possible test and evidence:** Implement a simple web task with identical reference text shown in static and actionable conditions. Log user clicks/searches and compare correct identification, false acceptance of fabricated/mismatched references, time, trust/confidence, and verification completion. Use the same task items across conditions or counterbalance them.

**Critical controls / risks:** This overlaps with existing source/citation-trust experiments, especially Ding et al. (2025) and Kim et al. (2025). The contribution must be a citation-specific comparison of actionable bibliographic verification rather than merely repeating a sources-present/sources-absent experiment. Broken links, irrelevant links, and inconsistent metadata are separate conditions and must not be mixed silently.

**Feasibility:** Medium. The interface and logging are manageable, but participant recruitment and precise source-status labels are required.

## GAP 03 — Does citation trust transfer from short trivia tasks to scholarly reading?

**Priority:** 4  
**Type:** Context-generalization study

**Review evidence**

- Section 5 says citation-effect/truthiness studies often use short trivia statements and controlled judgment tasks, which may not generalize to long-form scholarly documents, professional settings, or high-stakes decisions.
- Section 2.2 describes the citation effect in trivia judgments; Section 2.4 describes the separate literature on LLM-fabricated references in research or medical writing.
- Section 6 recommends research on fabricated references using stimuli drawn from real AI-hallucinated citations rather than only researcher-constructed trivia statements.

**Reported limitation:** The review explicitly identifies the external-validity gap between short experimental claims and longer scholarly/professional material.

**Inference / candidate question:** *Does a citation's apparent completeness influence acceptance of fabricated references similarly when the reference appears beside a short claim versus inside a short literature-review paragraph?*

**Possible test and evidence:** Create two carefully matched presentation contexts (short claim and short scholarly paragraph) and vary citation authenticity/format while keeping the substantive statement as comparable as practical. Measure perceived credibility and authenticity classification. Analyze whether presentation context interacts with format and authenticity.

**Critical controls / risks:** Longer passages introduce more confounds (topic, writing quality, prior knowledge, source relevance, and reading time). Stimuli must be counterbalanced and checked by a human; do not write a fabricated passage and call it an original published stimulus. This may need more participants than a simple within-subject comparison.

**Feasibility:** Medium to low, depending on the number of stimuli and available participants.

## GAP 04 — Does citation-specific lateral-reading instruction improve detection?

**Priority:** 3  
**Type:** Small intervention study (pre/post or randomized instructional comparison)

**Review evidence**

- Section 4.3 reviews Wineburg and McGrew (2019), where professional fact-checkers used lateral reading more effectively than historians and students in evaluating unfamiliar online sources.
- Section 5 notes that domain expertise does not automatically imply effective verification habits.
- Section 6 recommends adapting and testing lateral-reading-style interventions specifically for citation verification.

**Reported limitation:** The review identifies a transfer question: general online-credibility training has not been established by the review as a citation-specific intervention for detecting fabricated references.

**Inference / candidate question:** *Does a short instruction that teaches readers to independently search a citation's title/DOI and compare bibliographic metadata improve fabricated-reference detection and confidence calibration relative to a no-instruction or generic-checking condition?*

**Possible test and evidence:** A short pre-test, instruction, and post-test with fresh items; measure accuracy, false-acceptance rate, time, confidence calibration, and transfer to a different subject domain. If feasible, use a comparison group and report baseline differences.

**Critical controls / risks:** General lateral-reading evidence must not be described as proof that a citation-specific tutorial works. Learning may be due to repeated exposure to the same examples, so post-test items should be new. Obtain consent/approval if required.

**Feasibility:** Medium. The instructional material and analysis code are modest, but credible outcome interpretation still requires enough participants and fresh stimulus items.

## GAP 05 — Does domain familiarity moderate susceptibility to formatting cues?

**Priority:** 5  
**Type:** Stratified or interaction analysis in a controlled task

**Review evidence**

- Section 2.4 reports that citation-fabrication estimates vary across model, prompt, and domain in the reviewed literature.
- Section 5 states that domains differ and that laboratory convenience samples may have varying baseline familiarity with citation conventions.
- Section 5 also notes that subject expertise does not necessarily translate to independent source-checking skill, using Wineburg and McGrew (2019) as broader context.

**Reported limitation:** The review describes domain/sample differences as a generalization concern; it does not establish that domain familiarity causes the format-trust effect to change.

**Inference / candidate question:** *Does self-reported or measured domain/citation literacy moderate the effect of citation completeness and identifier visibility on credibility judgments and fake-reference detection?*

**Possible test and evidence:** Collect a brief domain-familiarity measure and citation-literacy measure alongside the controlled judgment task. Prespecify a small number of groups or use continuous scores; report interaction estimates and uncertainty. Keep claims modest if the sample is small.

**Critical controls / risks:** Self-reported expertise is noisy, and recruiting sufficiently large expert/novice groups can be difficult. It should not be added as a speculative subgroup comparison after looking at results.

**Feasibility:** Low to medium for a dedicated study; more feasible as a prespecified exploratory moderator within GAP 01 if recruitment supports it.

## Ranking of the top three candidates

The rankings are qualitative planning judgments, not empirical scores. Because the available hardware, project time, participant access, and institutional approval status were not supplied, resource and feasibility ratings are provisional and must be confirmed before selecting a study.

### Rank 1 — Metadata completeness / DOI-PMID cues crossed with authenticity (GAP 01)

- **Significance:** High.
- **Resource need:** Low compute; medium human-study effort.
- **Feasibility:** Medium, conditional on participants and ethics requirements.
- **Reason for rank:** Most directly addresses the specific unresolved variable highlighted by the review. It needs a careful update search because adjacent work already studies citation count, relevance, and source presentation.

### Rank 2 — Actionable verification versus static references (GAP 02)

- **Significance:** High.
- **Resource need:** Medium.
- **Feasibility:** Medium.
- **Reason for rank:** Has a clear implementation component and observable behaviors, but prior source-reliance/citation-checking studies require a sharply differentiated research question.

### Rank 3 — Citation-specific lateral-reading intervention (GAP 04)

- **Significance:** Medium-high.
- **Resource need:** Low-to-medium.
- **Feasibility:** Medium.
- **Reason for rank:** Practical, interpretable and connected to the review's countermeasure discussion; the key uncertainty is whether general lateral-reading results transfer to fabricated references.

GAP 03 is also important but likely needs more careful stimulus construction and participants. GAP 05 is best treated as a moderator only if the sample is large and appropriately varied.

## Recommendation at this checkpoint

Carry **GAP 01** forward as the leading candidate for feasibility checking, not as a final approved research question. Before coding or data collection, conduct a more systematic search for experiments manipulating bibliographic completeness, DOI/PMID visibility, source authenticity, and trust; inspect Ding et al. (2025) and Cho and Lim (2026) closely; and confirm participant/ethics access. If human participation is infeasible, a citation-verification pipeline can be considered as a fallback, but it would test bibliographic verifiability—not human trust—and the research question must be changed accordingly.

## References and leads

- Ding, Y. et al. (2025). “Citations and Trust in LLM Generated Responses.” *Proceedings of the AAAI Conference on Artificial Intelligence*, 39(22), 23787–23795. https://doi.org/10.1609/aaai.v39i22.34550
- Cho, J. & Lim, D. (2026). “How Source Attribution Visualization Shapes User Attention and Preference: An Eye-Tracking Study of Four AI Chatbot Layouts.” *Journal of Eye Movement Research*, 19(4), 89. https://doi.org/10.3390/jemr19040089
- Kim, S. S. Y. et al. (2025). “Fostering Appropriate Reliance on Large Language Models: The Role of Explanations, Sources, and Inconsistencies.” CHI 2025. https://doi.org/10.1145/3706598.3714020
- Putnam, A. L. & Phelps, R. J. (2017). “The citation effect: In-text citations moderately increase belief in trivia claims.” *Acta Psychologica*, 179, 114–123. https://doi.org/10.1016/j.actpsy.2017.07.010
- Walters, W. H. & Wilder, E. I. (2023). “Fabrication and errors in the bibliographic citations generated by ChatGPT.” *Scientific Reports*, 13, 14045. https://doi.org/10.1038/s41598-023-41032-5
- Bhattacharyya, M. et al. (2023). “High rates of fabricated and inaccurate references in ChatGPT-generated medical content.” *Cureus*, 15(5), e39238. https://doi.org/10.7759/cureus.39238
- Wineburg, S. & McGrew, S. (2019). “Lateral Reading and the Nature of Expertise: Reading Less and Learning More When Evaluating Digital Information.” *Teachers College Record*, 121(11), 1–40. https://doi.org/10.1177/016146811912101102
