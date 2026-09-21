# Drug Candidate Ranking Method

## Purpose

This file documents the transparent prioritization framework used in **BUBR1-RESCUE 3.0** to compare candidate rescue strategies for BUB1B/BUBR1-associated Mosaic Variegated Aneuploidy (MVA).

The score is a **project prioritization tool**, not a validated clinical score, not a treatment recommendation, and not evidence that any candidate rescues the patient's N1002K variant.

## Scoring framework

Each candidate receives a maximum of 100 points:

| Criterion | Max points | Question |
|---|---:|---|
| Direct BUBR1 evidence | 25 | Is there direct evidence that the candidate or pathway changes BUBR1 abundance, stability, or function? |
| N1002K mechanistic fit | 20 | Would the mechanism make sense if N1002K produces a full-length but unstable or partially functional protein? |
| Mechanistic evidence | 15 | Is the direction of the molecular mechanism supported by experimental evidence? |
| Functional/cellular evidence | 15 | Is there cellular or in vivo evidence of a relevant biological effect? |
| Repurposing feasibility | 10 | Is the compound realistic for drug repurposing or translational follow-up? |
| Clinical/safety knowledge | 10 | Is there meaningful human-use or safety information? |
| Orthogonality | 5 | Does the compound provide a complementary mechanism rather than simply duplicate another candidate? |

**Total = 100 points**

## Interpretation bands

- **80-100:** high-priority hypothesis or mechanistic benchmark
- **65-79:** strong backup or orthogonal hypothesis
- **45-64:** exploratory candidate or comparator
- **<45:** low priority, drop, research-only tool, or negative control

## Current prioritization logic

### Primary repurposing hypothesis: Niacin

Niacin is prioritized because it is a clinically established molecule that can support cellular NAD+ pools, creating a plausible route to the **NAD+–SIRT2–BUBR1 stabilization axis**.

The project does **not** claim that niacin has been shown to rescue N1002K or treat MVA.

### Mechanistic benchmark: NMN

NMN receives the strongest direct BUBR1 mechanistic support because prior work linked NAD+/SIRT2 biology to increased BubR1 abundance. It is used as a mechanistic benchmark rather than automatically treated as the best repurposing candidate.

### Orthogonal lead: Arimoclomol

Arimoclomol provides a distinct hypothesis based on proteostasis and the heat-shock response. This route is relevant because MVA-associated BUBR1 missense proteins can show reduced stability and dependence on chaperone machinery.

The project does **not** claim that arimoclomol rescues N1002K.

## Why negative candidates are retained

The ranking intentionally includes candidates that score poorly or are mechanistically unfavorable. This demonstrates that the framework can reject superficially attractive compounds.

For example, HSP90 inhibition is considered unfavorable because unstable BUBR1 missense proteins can depend on HSP90 for stability.

## Reproducibility

All individual scores are stored in:

`data/drug_candidate_ranking.csv`

Any future score changes should be accompanied by:
1. the new evidence,
2. the reason for changing a criterion,
3. the date/commit documenting the revision.

## Key references

- North BJ, et al. SIRT2 induces the checkpoint kinase BubR1 to increase lifespan. *EMBO J.* 2014. PMID: 24825348.
- Hara N, et al. Elevation of cellular NAD levels by nicotinic acid and involvement of nicotinic acid phosphoribosyltransferase in human cells. *J Biol Chem.* 2007. PMID: 17604275.
- Molecular causes for BUBR1 dysfunction in Mosaic Variegated Aneuploidy. PMCID: PMC2887387.
- U.S. FDA. Miplyffa (arimoclomol) approval for Niemann-Pick disease type C, 2024.
