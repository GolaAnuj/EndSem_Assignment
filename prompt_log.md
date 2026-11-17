# Prompt Log — Week Checkpoint (Prompts 01 and 02 only)

This log records the two assignment prompts used for this checkpoint and the work products produced. It does not claim that later prompts, code generation, experiments, or results were completed.

## Prompt 01 — Set up an accountable research workspace

**Assignment prompt, adapted to the available project:**

> I am a postgraduate student converting my completed literature review into an implementation-based research paper. My topic is **The Influence of Citation Formatting on Human Trust in Fabricated References**. Act as a critical research mentor and technical pair programmer. Guide me in stages: evidence-based gap identification, literature-to-experiment mapping, feasibility, research questions, verified baseline, coding, experimental evaluation, manuscript and reproducibility. Mark statements as VERIFIED, INFERRED or UNKNOWN, and explicitly request source files or outputs when evidence is missing. Help me create a portable `research_decisions.md` log containing decisions, reasons, source/evidence and next actions. Start by asking me to attach my existing review and summarize its scope without assuming unseen content.

**Input available:** The prior review paper and source project were already available in this conversation/workspace from the previous review-paper milestone. They are preserved under `review_basis/`; I therefore used those supplied files rather than assuming the content of an unseen manuscript.

**Output created:** `research_decisions.md`, including review scope, key evidence, verified/inferred/unknown ledger, decisions, reasons, supporting evidence, and next actions.

## Prompt 02 — Extract evidence-based research gaps

**Assignment prompt, adapted to the available project:**

> Analyze my attached literature review (`review_basis/ACM_Final_Review_Paper.pdf`, its LaTeX source and bibliography). Identify central methods, datasets, measured findings, author-reported limitations and unresolved questions. Propose five computationally testable research gaps. For each, cite the specific passage or reference in my review; clearly distinguish a limitation reported in the original paper from your own inference; state the experimental question it suggests and what evidence would test it. Flag any claims needing verification against the original publications. Rank three gaps by research significance, available resources and implementation feasibility. Do not claim novelty without a separate literature search.

**Output created:** `gap_matrix.md` with five gaps, cited review sections, reported limitations versus inferences, candidate questions, potential measurements, confounds/risks, and a qualitative ranking of the top three. `source_verification_register.md` records primary-source checks and adjacent newer studies that need full-text review.

**Verification boundary:** A limited, targeted web check was performed for key primary-source abstracts and adjacent 2025–2026 work. It is not a complete novelty search. No code was run, no participants were recruited, no experiment was conducted, and no experimental result was generated in this checkpoint.
