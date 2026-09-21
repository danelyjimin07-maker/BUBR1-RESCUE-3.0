# BUBR1-RESCUE 3.0 — Summary Results

## Purpose

This file summarizes the current computational and literature-guided results of **BUBR1-RESCUE 3.0**, a second-submission candidate for the Rare Disease Real Kid Hackathon 2026 (Track 2).

No original wet-lab rescue experiment was completed. All conclusions below distinguish between:

- **established evidence**,
- **mechanistic inference**,
- **project prioritization**,
- and **future experimental validation**.

---

## 1. Variant-level interpretation

### p.Leu737Ter

**Current interpretation:** established pathogenic loss-of-function allele.

Expected consequence:

- reduced or absent functional BUBR1 product,
- loss of the C-terminal region if a truncated protein is produced,
- contribution to BUB1B-associated Mosaic Variegated Aneuploidy (MVA).

**Project confidence:** HIGH.

### p.Asn1002Lys (N1002K)

**Current interpretation:** ultra-rare candidate missense variant with unresolved pathogenicity.

Evidence supporting prioritization:

- located in the C-terminal kinase-like/pseudokinase region,
- occurs in a structurally ordered region,
- changes a neutral polar residue to a positively charged residue,
- lies near a region where other MVA-associated BUBR1 missense variants have shown reduced stability,
- remains compatible with production of a full-length protein.

Important uncertainty:

- pathogenicity is unresolved,
- phase relative to p.Leu737Ter is unresolved,
- no patient-specific protein assay was performed,
- no N1002K rescue assay was performed.

**Project confidence in pathogenicity:** UNRESOLVED.  
**Project confidence that N1002K is worth rescue testing:** MODERATE-HIGH.

---

## 2. Structural interpretation

The project does **not** claim that N1002K is experimentally destabilizing.

The structural hypothesis is:

**N1002K may alter local packing, electrostatics, or hydrogen-bonding in the BUBR1 C-terminal region, creating a possible stability or partial-function defect.**

This is supported by:

- high local model confidence around N1002,
- the chemistry of the Asn→Lys substitution,
- the location of N1002 within a functionally relevant C-terminal region,
- precedent from MVA-associated BUBR1 missense variants such as I909T and L1012P that can show reduced protein abundance or stability.

### Structural classification used in this project

- **Stability-defect candidate:** MODERATE SUPPORT
- **Intrinsic functional-defect candidate:** UNRESOLVED
- **Benign/no major structural effect:** CANNOT BE EXCLUDED

---

## 3. Variant–Rescue framework result

BUBR1-RESCUE 3.0 separates:

### A. Variant causality

> How strong is the evidence that the variant contributes to disease?

### B. Molecular rescuability

> If the variant is biologically relevant, is there evidence that residual BUBR1 could be stabilized or functionally rescued?

For N1002K:

- **Causality confidence:** unresolved / intermediate
- **Rescuability plausibility:** mechanistically plausible

This distinction is central to the project.

---

## 4. Systematic drug-screen result

Twenty candidate compounds or strategies were evaluated with a transparent 100-point prioritization framework.

The current top candidates are:

| Rank | Candidate | Role | Score |
|---:|---|---|---:|
| 1 | Niacin | Primary repurposing hypothesis | 84 |
| 2 | NMN | Mechanistic benchmark | 83 |
| 3 | Arimoclomol | Orthogonal repurposing hypothesis | 79 |
| 4 | Nicotinamide riboside (NR) | Backup NAD+ strategy | 75 |
| 5 | Geranylgeranylacetone / teprenone | Backup HSP strategy | 64 |
| 6 | Bimoclomol | Backup proteostasis strategy | 63 |
| 7 | TUDCA | Exploratory proteostasis candidate | 59 |
| 8 | 4-PBA | Comparator | 55 |

The full ranking is available in:

`data/drug_candidate_ranking.csv`

The scoring method is available in:

`docs/drug_ranking_method.md`

These scores are **not clinical efficacy scores**.

---

## 5. Primary rescue hypothesis

### Niacin — NAD+–SIRT2–BUBR1 stabilization

**Why it was prioritized:**

- niacin can support cellular NAD+ production,
- SIRT2 is NAD+-dependent,
- prior work links SIRT2 to BUBR1 stability and abundance,
- the strategy is compatible with a hypothesis in which N1002K produces a full-length but unstable protein,
- niacin has extensive clinical-use knowledge compared with many experimental compounds.

### Working mechanistic chain

**Niacin**  
→ increased NAD+ availability  
→ support of SIRT2-dependent BUBR1 stabilization  
→ potential increase in functional BUBR1 abundance  
→ potential improvement in spindle assembly checkpoint function

### Critical limitation

No study currently demonstrates:

**niacin → rescue of N1002K**

Therefore, niacin remains a **testable repurposing hypothesis**, not a demonstrated treatment.

---

## 6. Mechanistic benchmark

### NMN

NMN remains the strongest mechanistic benchmark because prior experimental work linked NAD+/SIRT2 biology to increased BubR1 abundance.

Its role in BUBR1-RESCUE 3.0 is:

**positive mechanistic benchmark**

rather than:

**automatic therapeutic lead**

This separation improves translational rigor.

---

## 7. Orthogonal rescue hypothesis

### Arimoclomol — proteostasis / heat-shock response

Arimoclomol was retained as the strongest orthogonal candidate because:

- MVA-associated BUBR1 missense variants can show reduced protein stability,
- unstable BUBR1 variants can depend on heat-shock machinery,
- arimoclomol acts through a proteostasis/heat-shock-response strategy,
- it provides a mechanistically independent route from NAD+ metabolism.

### Working mechanistic chain

**Arimoclomol**  
→ heat-shock / proteostasis response  
→ improved handling of unstable BUBR1 protein  
→ potential increase in functional BUBR1

### Critical limitation

No study currently demonstrates:

**arimoclomol → rescue of N1002K**

Therefore, arimoclomol is an **orthogonal rescue hypothesis**, not a demonstrated therapy for MVA.

---

## 8. Negative and low-priority findings

The screen intentionally identified candidates that should **not** be prioritized.

### Geldanamycin

Classified as:

**CONTRA-MECHANISTIC**

Reason:

- HSP90 inhibition is expected to worsen the stability of unstable BUBR1 missense proteins.

This provides an important negative-control concept.

### MG132

Classified as:

**RESEARCH ONLY**

Reason:

- useful as a proteasome research tool,
- not appropriate as a repurposing candidate.

### Nicotinamide

Classified as:

**DROP**

Reason:

- although related to NAD+ metabolism,
- nicotinamide can inhibit sirtuin activity,
- making it mechanistically conflicted for a SIRT2-dependent rescue strategy.

### 4-PBA

Classified as:

**COMPARATOR**

Reason:

- useful for proteostasis comparison,
- but weaker target specificity and uncertainty around its classical “chemical chaperone” interpretation.

---

## 9. Dual-pathway result

The final architecture of BUBR1-RESCUE 3.0 is a **dual-pathway rescue strategy**.

### Route A — NAD+–SIRT2 stabilization

Lead:
- Niacin

Benchmark:
- NMN

Backup:
- NR

### Route B — Proteostasis support

Lead:
- Arimoclomol

Backups:
- GGA / teprenone
- Bimoclomol
- TUDCA

Both routes converge on the same desired outcome:

**increased functional BUBR1**

followed by:

**improved spindle assembly checkpoint function**

and ultimately:

**reduced chromosome missegregation**

---

## 10. Go / No-Go experimental decision framework

A future experiment should not advance a candidate based on protein abundance alone.

### GO

A candidate advances only if it produces:

1. increased BUBR1 abundance or stability, **and**
2. improved checkpoint/chromosome-segregation function.

### NO-GO

A candidate does not advance if:

- BUBR1 abundance rises but function does not improve,
- no molecular rescue occurs,
- or chromosome-segregation defects worsen.

---

## 11. Current project conclusion

BUBR1-RESCUE 3.0 does **not** claim to have identified a treatment for MVA.

Instead, it provides:

- a transparent variant-level rescue framework,
- a reproducible drug-prioritization method,
- a dual-pathway strategy,
- explicit negative controls,
- explicit uncertainty,
- and a falsifiable path to experimental validation.

### Current primary conclusion

**Niacin is the leading drug-repurposing hypothesis, NMN is the strongest mechanistic benchmark, and arimoclomol is the strongest orthogonal rescue hypothesis.**

This conclusion is intended to guide future validation rather than clinical use.

---

## 12. Next required steps before Submission 2

1. Finalize the visual decision framework.
2. Convert this result summary into the final scientific report.
3. Cross-check all claims against primary literature and current regulatory sources.
4. Add final references and AI-use disclosure.
5. Produce the 3-minute pitch.
6. Compare the complete 3.0 package against the original submission.
7. Submit only if BUBR1-RESCUE 3.0 is clearly stronger.
