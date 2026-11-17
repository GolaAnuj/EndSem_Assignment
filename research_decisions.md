# Portable Research Decision and Evidence Log

All decisions below were generated/documented during this AI-assisted project work. They are not attributed to the student's personal decisions without review.

| Stage | Decision | Evidence/reason | Status | Next human action |
|---|---|---|---|---|
| Review scope | Citation cues, fabricated metadata, human trust | Uploaded seven-page narrative review §§1–8 | VERIFIED from uploaded file | Read and confirm interpretation |
| Gap | Format tolerance versus incorrect bibliographic fields | Review §§3,5–7 motivates metadata checks | INFERRED: computational design not a direct result of review | Confirm the bridge is acceptable to instructor |
| Pathway | Controlled computational comparison (B) | No participant data; CPU feasibility; assignment allows non-ML | VERIFIED choice for this generated project | Confirm research pathway |
| Data | 13 DOI-bearing citations manually transcribed | Review reference page; 3 spot-checked primary sources | PARTLY VERIFIED | Independently check remaining 10 citations |
| Comparator B1 | Strict exact four-field equality | Transparent and lightweight baseline, not published reproduction | VERIFIED as code and local behavior | Explain its brittleness |
| Comparator B2 | Title-only normalized fuzzy matching | Transparent weaker baseline ignoring identifiers | VERIFIED as code and local behavior | Explain its false acceptance |
| Main method | DOI-first, then title+surname+year | Principle of cross-field consistency from review | VERIFIED code, unverified real-world accuracy | Explain not an external DOI lookup |
| Freeze | `configs/frozen_protocol.json`, seeds and thresholds | Created before first study run | VERIFIED local creation sequence | Avoid revising as though preregistered |
| Execution | 8 tests, 650 cases, 4,550 predictions | Actual local executed scripts/logs | VERIFIED | Re-run notebook in own Colab account |
| Primary inference | Perfect holdout F1 on synthetic generator only | Measured values from results.csv | VERIFIED numerical, LIMITED generalizability | Refrain from universal accuracy claims |
| Post-hoc challenge | Altered title prefix check | Added AFTER observing primary perfect score | VERIFIED as exploratory (not preregistered) | Discuss observed 5/13 false accepts |
| Paper | IEEE-style compiled manuscript | Actual LaTeX + bibliography + measured plots | VERIFIED artifact creation | Review source content and meet instructor formatting |
| Github | Repository structure provided, not pushed | No user GitHub authorization | UNKNOWN publication | Publish using student's own account if required |
