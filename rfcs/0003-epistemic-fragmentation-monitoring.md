---
rfc: "0003"
title: "Epistemic Fragmentation Monitoring Protocol"
stream: "Standards Track"
status: "DRAFT"
category: "Informational"
area: "process"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "1992-03-14"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [1, 16]
keywords: [fragmentation, monitoring, metrics, jensen-shannon, embeddings, knowledge-divergence]
abstract: |
  This document specifies the Epistemic Fragmentation Monitoring Protocol (EFMP),
  a protocol for measuring the divergence between formal knowledge representations
  (documentation, wikis, specifications, code) and operational knowledge (what
  people do). EFMP defines the Fragmentation Index (FI) as Jensen-Shannon
  divergence between formal and operational knowledge distributions, with directional
  KL-diagnostics. Organizations with FI > 0.3 experience accelerated knowledge
  decay; FI > 0.5 indicates critical epistemic disconnect. While framed as a
  monitoring protocol, EFMP functions analytically as a diagnostic instrument
  for organizational epistemology.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0003 — Epistemic Fragmentation Monitoring Protocol (EFMP)

## Abstract

This document specifies the Epistemic Fragmentation Monitoring Protocol (EFMP),
a protocol for measuring the divergence between formal knowledge representations
(documentation, wikis, specifications, code) and operational knowledge (what
people do). EFMP defines the Fragmentation Index (FI) as Jensen-Shannon
divergence between formal and operational knowledge distributions, with
directional KL-diagnostics. Organizations with FI > 0.3 experience accelerated
knowledge decay; FI > 0.5 indicates critical epistemic disconnect. While framed
as a monitoring protocol, EFMP functions analytically as a diagnostic instrument
for organizational epistemology.

> **Dual-Layer Notice**: This RFC employs the Epistemic Fragmentation Monitoring
> Protocol (EFMP) as a satirical vehicle for presenting peer-reviewed findings
> on organizational knowledge divergence (Simon 1947; Nonaka & Takeuchi 1995;
> Wenger 1998; Edmondson 2019). While EFMP employs satirical framing, the
> organizational claims are substantiated by the cited literature. Implementers
> should treat EFMP as an analytical lens, not a deployable monitoring
> protocol — though some organizations have reportedly "implemented" it by
> requiring quarterly documentation audits.

## 1. Introduction

### 1.1 Motivation

Organizations invest heavily in knowledge management systems — wikis, documentation
portals, architecture decision records, runbooks. Yet practitioners consistently
report that "the docs are wrong," "the wiki is stale," "nobody reads the runbooks."
This is not negligence; it is structural. Formal knowledge representations are
written for auditors and onboarding; operational knowledge lives in muscles,
habits, and coffee-break conversations (RFC-0017).

The Epistemic Fragmentation Monitoring Protocol (EFMP) makes this divergence
measurable. By quantifying the distance between what is written and what is done,
EFMP transforms a vague complaint ("the docs are out of date") into a tractable
metric: the Fragmentation Index (FI).

**Intuitive gloss (for readers who skip formalisms):** think of two lists of
words. One list is drawn from the documentation; the other from what people
truly do. If the lists match, the organization is aligned (FI ≈ 0). If
they describe two different companies, it is fragmented (FI → 1). The
Jensen-Shannon divergence is the distance between the two lists' probability
distributions — counting both directions (what the docs claim that nobody
does, and what people do that the docs never mention) and landing on a scale
of 0 to 1. Chapters point to this paragraph instead of restating the formula.

### 1.2 Scope

This document specifies:
- The Fragmentation Index (FI) as Jensen-Shannon divergence between formal
  and operational knowledge distributions
- Directional KL-diagnostics: D_KL(Operational || Formal) and D_KL(Formal || Operational)
- Knowledge representation via concept embeddings over documents, code, and tickets
- Operational ground truth capture via digital trace + quarterly survey triangulation
- Alerting thresholds: Alert at FI > 0.3, Critical at FI > 0.5
- Integration with RFC-0001 (HOP), RFC-0002 (Conway), RFC-0016 (Memory Backup)

### 1.3 Non-Goals

This document does not specify:
- Automated tooling for embedding generation (see BCP-XXXX)
- Remediation procedures (see RFC-0016 Institutional Memory Backup)
- Tacit knowledge extraction methodology (RFC-0008 OBSOLETE; see RFC-0017 CBP)
- Theorem-004 proof (separate artifact)

### 1.4 Relationship to Other RFCs

| RFC | Relationship |
|-----|--------------|
| RFC-0001 (HOP) | Executive delusion quantified: high FI + high HOP ECI = systemic epistemic capture |
| RFC-0002 (Conway) | Low MFM → high FI pathway; structural
misalignment causes formal/operational divergence |
| RFC-0016 (Memory Backup) | FI > 0.3 triggers backup protocol; FI > 0.5 mandates full knowledge audit |
| RFC-0017 (CBP) | CBP edges in operational knowledge graph reduce FI by synchronizing weak ties |
| Theorem-004 | Formal bound: FI ≥ c × log(d) where d = hierarchy depth |

## 2. Terminology

| Term | Definition |
|------|------------|
| **Formal Knowledge (K_formal)** | Documented knowledge: wikis, specs, ADRs, runbooks, code comments, API docs, architecture diagrams |
| **Operational Knowledge (K_operational)** | What people do: habits, workarounds, unwritten rules, muscle memory, coffee-break wisdom (RFC-0017) |
| **Tacit Knowledge** | Knowledge that cannot be fully codified (Polanyi; Theorem-005). Operational knowledge is largely — but not entirely — tacit: some of what people do could be documented, and some documented knowledge is tacit in practice. Use "tacit" for the inexpressibility property, "operational" for the behavior itself |
| **Fragmentation Index (FI)** | Jensen-Shannon divergence between formal and operational knowledge distributions; range [0, 1] |
| **Concept Space (C)** | Semantic space of organizational concepts; each concept c ∈ C is a point in embedding space |
| **Knowledge Distribution** | Probability distribution P(c) over concept space representing knowledge prevalence |
| **Sync Event** | Moment when formal and operational knowledge align (rare, usually accidental) |
| **Embedding Model** | Sentence transformer mapping text chunks to vectors in ℝ^d (d=384–768) |
| **Directional Diagnostics** | D_KL(Op || Form) = what ops knows that formal misses; D_KL(Form || Op) = what formal claims that ops doesn't do |

## 3. Protocol Specification

### 3.1 Knowledge Representation

**Requirement 1**: The concept space C MUST be constructed from the union of
three corpora:

- **Documents**: Wiki pages, Confluence spaces, Notion, SharePoint, Google Docs
- **Code**: Repository files (source, tests, configs, Dockerfiles, CI/CD)
- **Tickets**: Jira, GitHub Issues, Linear, Asana — titles, descriptions, comments

**Requirement 2**: Each corpus MUST be chunked into semantic units (512 tokens
max, 20% overlap) and embedded using a sentence transformer model
(e.g., `all-MiniLM-L6-v2`, 384 dimensions; or `all-mpnet-base-v2`, 768 dimensions).

**Requirement 3**: The formal knowledge distribution P_formal(c) for concept c
MUST be estimated as:

```
P_formal(c) = (1/Z) × Σ_{chunk ∈ formal_corpus}
  exp(-||emb(chunk) - emb(c)||² / 2σ²)
```

where σ controls semantic bandwidth (default: 0.5), Z normalizes to unit sum.

**Requirement 4**: The operational knowledge distribution P_operational(c) MUST
be estimated by combining digital trace and survey evidence through a
hierarchical Bayesian model:

```
P_operational(c) = Normalize( P_digital(c)^α × P_survey(c)^(1-α) )
```

where:
- P_digital(c) = normalized frequency of concept c in digital traces
  (Slack, Git, CI/CD logs, IDE telemetry) over concept space C
- P_survey(c) = normalized quarterly survey responses mapped to [0,1]
  via "How often do you use/encounter [concept]?" (1=never...5=daily)
- α = 0.7 (default; higher weight to continuous digital trace)
- Normalize() = L1 normalization to unit sum over C
- Product-of-powers combines evidence on probability scale; log-space addition
  corresponds to Bayesian evidence combination under independence assumption

**Requirement 4.1**: Both P_digital and P_survey MUST be L1-normalized to
unit sum over C before combination. Survey responses MUST be mapped to
[0,1] via (response - 1) / 4.

**Note (trace reliability):** Slack-derived traces are NOT a privileged source
of operational truth. The same channel that carries knowledge also buries it:
context dies in long threads, answers hide in unindexed DMs, and the channel
archive is a graveyard of decisions nobody recorded. Implementers SHOULD treat
Slack as a noisy signal requiring corroboration (survey, ethnographic
spot-checks per §4.2), not as the ground truth of what the organization
knows. A thread that a few people watch is not the same as knowledge the
organization can recover.

### 3.2 Fragmentation Index (FI)

**Requirement 6**: The Fragmentation Index FI MUST be computed as Jensen-Shannon
divergence between P_formal and P_operational:

```
FI = JS(P_formal || P_operational)
   = ½ D_KL(P_formal || M) + ½ D_KL(P_operational || M)
   where M = ½ (P_formal + P_operational)
```

**Requirement 6.1**: FI MUST be reported with 95% confidence intervals via
bootstrap resampling (1000 iterations over concept space).

**Requirement 7**: FI interpretation thresholds:

| FI Range | Classification | Interpretation | Action |
|----------|----------------|----------------|--------|
| FI ≤ 0.15 | **Aligned** | Formal ≈ Operational | Routine monitoring |
| 0.15 < FI ≤ 0.30 | **Drifting** | Emerging divergence | Quarterly review; targeted doc updates |
| 0.30 < FI ≤ 0.50 | **Misaligned** | Significant divergence | Mandatory knowledge audit (RFC-0016) |
| FI > 0.50 | **Critical** | Formal/Operational decoupled | Executive review; restructuring indicated |

### 3.3 Directional Diagnostics

**Requirement 8**: Implementations MUST compute and report both directional
KL-divergences alongside FI:

| Metric | Formula | Interpretation |
|--------|---------|----------------|
| **Op→Form** | D_KL(P_operational || P_formal) | What ops knows that formal misses (undocumented workarounds, tribal knowledge) |
| **Form→Op** | D_KL(P_formal || P_operational) | What formal claims that ops doesn't do (stale docs, zombie processes, zombie docs) |

**Requirement 9**: Both metrics MUST be reported per concept (top-20 contributors)
and aggregated (mean ± std).

### 3.4 Temporal Dynamics

**Requirement 10**: FI MUST be computed quarterly with monthly rolling updates
for high-velocity organizations.

**Requirement 11**: Temporal derivative ΔFI/Δt MUST be computed and reported.
Positive derivative indicates accelerating fragmentation.

**Requirement 12**: Sync Events (FI drops > 0.1 in one quarter) MUST be logged
and investigated. Causes: major documentation sprint, restructuring, key hire,
CBP intensification (RFC-0017).

### 3.5 Normative Requirements Summary

| Req | Parameter | MUST | SHOULD | MAY |
|-----|-----------|------|--------|-----|
| 1 | Three-corpus construction | YES | | |
| 2 | Embedding model (MiniLM/mpnet) | YES | | |
| 3 | P_formal estimation | YES | | |
| 4 | P_operational via triangulation | YES | | |
| 5 | Distribution normalization | YES | | |
| 6 | FI = JS divergence | YES | | |
| 6.1 | Bootstrap CIs | YES | | |
| 7 | FI thresholds table | YES | | |
| 8 | Directional KL diagnostics | YES | | |
| 9 | Per-concept + aggregated | YES | | |
| 10 | Quarterly computation | YES | | |
| 11 | Temporal derivative | YES | | |
| 12 | Sync Event logging | YES | | |

## 4. Operational Considerations

### 4.1 Deployment Models

EFMP is a diagnostic, not a documentation enforcement tool. Organizations MAY apply it as:

1. **Quarterly Audit (recommended entry point)**: Survey-only or survey+manual
   estimate of the formal/operational gap, driving targeted documentation
   sprints. Requires no data pipeline — a handful of practitioners, two lists
   of concepts, and an honest comparison. This is the honest default for most
   organizations, which lack the telemetry infra for passive computation.
2. **Passive Radar**: Continuous FI computation from existing data sources.
   Requires parseable corpora plus digital trace pipelines (Slack, Git,
   CI/CD, IDE telemetry). Recommended only for organizations with data
   maturity sufficient to support it.
3. **Executive Dashboard**: FI trends + top-20 divergent concepts reported to
   C-suite. Depends on tier 2 infra.
4. **CBP Integration**: High FI triggers CBP intensification (RFC-0017) —
   more coffee, more sync. Applies at any tier.

### 4.2 Failure Modes

| Failure Mode | Mechanism | Detection | Mitigation |
|--------------|-----------|-----------|------------|
| **Embedding Drift** | Model updates change concept positions | FI jumps without org change | Pin model version; re-baseline |
| **Survey Fatigue** | Response rate drops → P_survey biased | Response rate < 30% | Reduce frequency; incentivize |
| **Digital Trace Blindness** | Shadow IT / offline work invisible | P_digital << P_survey | Ethnographic spot-checks |
| **Concept Space Explosion** | C grows → sparse distributions | | dim reduction (UMAP/PCA) before divergence |
| **Goodhart Gaming** | Teams write docs to lower FI | Form→Op drops, Op→Form rises | Monitor both directions; reward sync events |

### 4.3 Monitoring and Alerting

**Requirement 13**: Organizations computing FI SHALL alert when:
- FI crosses threshold (0.15, 0.30, 0.50) upward
- ΔFI/Δt > 0.05/quarter (accelerating divergence)
- Op→Form > 2× Form→Op (undocumented knowledge explosion)
- Form→Op > 2× Op→Form (zombie documentation proliferation)

## 5. Security & Privacy Considerations

### 5.1 Epistemic Intelligence

FI and directional diagnostics reveal:
- Which teams hold undocumented critical knowledge (Op→Form spikes)
- Which processes are documented but unused (Form→Op spikes)
- Knowledge silos and bus factors

**Requirement 14**: FI data SHALL be classified at same level as org restructuring
plans. Access limited to: measured teams, C-suite, independent epistemology auditor.

### 5.2 Individual Privacy

Digital trace collection (Slack, Git, IDE) may identify individual work patterns.

**Requirement 15**: Aggregation to team level (minimum 5 members) before FI
computation. Individual-level graphs PROHIBITED for FI reporting.

**Requirement 16**: Survey responses MUST be anonymized and aggregated. Minimum
response threshold: 3 respondents per team before inclusion.

### 5.3 CBP Integrity (RFC-0017 §7)

EFMP uses operational knowledge estimates that may include CBP-synchronized
knowledge. If FI monitoring incentivizes executives to attend coffee breaks
for "data collection," CBP's epistemic integrity is compromised.

**Requirement 17**: CBP-derived operational knowledge MUST be anonymized and
aggregated. No executive attendance tracking for FI purposes.

## 6. OSC Considerations

### 6.1 Registry Updates

This RFC requests:
- RFC-0003 allocated in Standards Track, process area (0100–0199)
- Keywords: fragmentation, monitoring, metrics, jensen-shannon, embeddings
- See-also: RFC-0001, RFC-0016

### 6.2 Code Points

EFMP defines no code points. FI thresholds are informational guidelines.

## 7. References

### 7.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001,
Organizational Standards Consortium, 1987. https://rfc.osc.org/rfc0001

[RFC-0002] Matos, R. "Conway's Law Generalization Protocol." RFC 0002,
Organizational Standards Consortium, 1987. https://rfc.osc.org/rfc0002

[RFC-0016] Matos, R. "Institutional Memory Backup Specification." RFC 0016,
Organizational Standards Consortium, 2026. https://rfc.osc.org/rfc0016

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017,
Organizational Standards Consortium, 2001. https://rfc.osc.org/rfc0017

### 7.2 Informative References

Cover, Thomas M., and Joy A. Thomas. 2006. *Elements of Information Theory*.
2nd ed. Hoboken: Wiley.

Endres, Dominik M., and Johannes E. Schindelin. 2003. "A New Metric for
Probability Distributions." *IEEE Transactions on Information Theory* 49 (7):
1858–1860. https://doi.org/10.1109/TIT.2003.813506

Edmondson, Amy C. 2019. *The Fearless Organization: Creating Psychological Safety
in the Workplace for Learning, Innovation, and Growth*. Hoboken: Wiley.

Lin, Jianhua. 1991. "Divergence Measures Based on the Shannon Entropy."
*IEEE Transactions on Information Theory* 37 (1): 145–151.
https://doi.org/10.1109/18.61115

Nonaka, Ikujiro, and Hirotaka Takeuchi. 1995. *The Knowledge-Creating Company:
How Japanese Companies Create the Dynamics of Innovation*. New York: Oxford
University Press.

Reimers, Nils, and Iryna Gurevych. 2019. "Sentence-BERT: Sentence Embeddings
using Siamese BERT-Networks." *Proceedings of EMNLP-IJCNLP*: 3982–3992.
https://doi.org/10.18653/v1/D19-1410

Simon, Herbert A. 1947. *Administrative Behavior: A Study of Decision-Making
Processes in Administrative Organization*. New York: Macmillan.

Wenger, Etienne. 1998. *Communities of Practice: Learning, Meaning, and Identity*.
Cambridge: Cambridge University Press.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 1992-03-14 | R. Matos | Initial draft (OSC founding) |
| 0.2 | 2008-09-15 | R. Matos | Financial crisis: Great Knowledge Loss recognition |
| 0.3 | 2019-12-01 | R. Matos | Pandemic: distributed EFMP; VCP reference |
| 0.4 | 2024-01-20 | R. Matos | Theorem-004 bound integration |
| 1.0 | 2026-07-18 | Rodolfo Matos | OEP canon alignment; JS divergence; embeddings |

## Appendix B: Open Issues

1. **Causal Direction**: Does low MFM cause high FI, or does high FI cause
   low MFM? Granger causality tests needed on longitudinal data.
   [UNVERIFIED]

2. **Embedding Model Selection**: MiniLM (fast, 384d) vs mpnet (slower, 768d)
   vs domain-adapted. Impact on FI stability unknown.
   [UNVERIFIED]

3. **Survey Design Validity**: Self-reported operational frequency subject
   to recall bias. Alternative: experience sampling method (ESM).
   [UNVERIFIED]

4. **Concept Granularity**: 512-token chunks vs sentence-level vs paragraph.
   Impacts concept space resolution and FI sensitivity.
   [UNVERIFIED]

5. **Cross-Cultural Thresholds**: High-power-distance cultures may have
   systematically higher baseline FI (formal ≠ operational is normative).
   [UNVERIFIED]

6. **Sync Event Taxonomy**: Not all FI drops are equal. Documentation sprint
   vs restructuring vs key hire vs CBP intensification have different
   sustainability profiles.
   [UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Wenger, Granovetter, Nonaka, Edmondson, Simon,
> Conway, Cover, Thomas, Lin, Reimers, Gurevych, etc.) are accurate. The coffee
> machine, however, is real — and it is currently synchronizing more knowledge
> than this repository ever will.