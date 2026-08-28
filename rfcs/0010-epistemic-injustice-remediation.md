---
rfc: "0010"
title: "Epistemic Injustice Remediation Protocol (EIRP)"
stream: "Standards Track"
status: "DRAFT"
category: "Informational"
area: "epistemology"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-18"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [9, 7, 17]
keywords: [epistemic-injustice, testimonial-injustice,
  hermeneutical-injustice, credibility, intersectionality, credibility-protocol]
abstract: |
  This document specifies the Epistemic Injustice Remediation Protocol (EIRP),
  a Standards Track protocol for detecting, measuring, and remediating epistemic
  injustice in organizations. EIRP defines the Epistemic Injustice Index (EII)
  with separate testimonial (credibility) and hermeneutical (interpretive) sub-indices,
  mandates structural remediation via calibrated credibility protocols and
  hermeneutical resource redistribution, and explicitly exempts CBP channels
  (RFC-0017) from EII surveillance. Organizations with EII > 0.5 experience
  accelerated epistemic fragmentation (RFC-0003) and knowledge gravity distortion
  (RFC-0005). While framed as a remediation protocol, EIRP functions analytically
  as a diagnostic instrument for organizational epistemic justice.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0010 — Epistemic Injustice Remediation Protocol (EIRP)

## Abstract

This document specifies the Epistemic Injustice Remediation Protocol (EIRP),
a Standards Track protocol for detecting, measuring, and remediating epistemic
injustice in organizations. EIRP defines the Epistemic Injustice Index (EII)
with separate testimonial (credibility) and hermeneutical (interpretive) sub-indices,
mandates structural remediation via calibrated credibility protocols and
hermeneutical resource redistribution, and explicitly exempts CBP channels
(RFC-0017) from EII surveillance. Organizations with EII > 0.5 experience
accelerated epistemic fragmentation (RFC-0003) and knowledge gravity distortion
(RFC-0005). While framed as a remediation protocol, EIRP functions analytically
as a diagnostic instrument for organizational epistemic justice.

> **Dual-Layer Notice**: This RFC employs the Epistemic Injustice Remediation
> Protocol (EIRP) as a satirical vehicle for presenting peer-reviewed findings
> on organizational epistemic injustice (Fricker 2007; Dotson 2011; Medina 2013).
> While EIRP employs satirical framing, the organizational claims are substantiated
> by the cited literature. Implementers should treat EIRP as an analytical lens,
> not a deployable governance protocol — though some organizations have reportedly
> "implemented" it by calibrating credibility protocols and redistributing
> interpretive resources.

---

## 1. Introduction

### 1.1 Motivation

Miranda Fricker (2007) identified two forms of epistemic injustice:
**testimonial injustice** — credibility deficit due to identity prejudice,
and **hermeneutical injustice** — interpretive gap due to lack of shared
conceptual resources. Kristie Dotson (2011) extended this to **contributory
injustice** — wilful hermeneutical ignorance by dominant groups. José Medina
(2013) showed how epistemic resistance sustains injustice.

In organizations, these manifest as:
- **Testimonial**: Code reviews where women's PRs take 2× longer; incident
  retrospectives where junior engineers' diagnoses are dismissed; architecture
  reviews where senior titles override evidence.
- **Hermeneutical**: Lack of vocabulary for burnout, microaggressions, neurodivergent
  work styles; incident taxonomies missing "psychological safety" categories;
  postmortem templates assuming "human error" not "system failure."

The Epistemic Injustice Remediation Protocol (EIRP) makes these measurable
and remediable through structural protocol changes, not individual bias training.

### 1.2 Scope

This document specifies:
- **Epistemic Injustice Index (EII)** with separate testimonial (EII_t) and
  hermeneutical (EII_h) sub-indices, combined multiplicatively
- **Testimonial Injustice Detection**: Credibility attribution patterns from
  behavioral traces (PR latency, speaking time, attribution, incident blame)
- **Hermeneutical Injustice Detection**: Interpretive resource gaps from
  vocabulary diversity, template coverage, expert access latency
- **Intersectional EII**: Multiplicative compounding across identity axes
- **Structural Remediation**: Calibrated credibility protocols + hermeneutical
  resource redistribution
- **CBP Exemption**: RFC-0017 channels excluded from EII surveillance

### 1.3 Non-Goals

This document does not specify:
- Individual bias training (structural changes only)
- Legal discrimination compliance (Title VII, etc.)
- Cultural change programs
- Individual coaching/therapy

### 1.4 Relationship to Other RFCs

| RFC | Relationship |
|-----|--------------|
| RFC-0003 (Fragmentation) | Injustice → formal/operational divergence; EII and FI correlated |
| RFC-0005 (Gravity) | Injustice → gravity wells; EII and KGI correlated |
| RFC-0007 (OAPP) | Injustice targets marginalized; EII and KHL correlated |
| RFC-0009 (KHIS) | Hoarding targets marginalized; KHI and EII correlated |
| RFC-0009 (KHIS Panel) | EII disputes resolved by KHIS panel (RFC-0009 Requirement 7) |
| RFC-0017 (CBP) | CBP channels excluded from EII surveillance |

---

## 2. Terminology

| Term | Definition |
|------|------------|
| **Testimonial Injustice** | Credibility deficit due to identity prejudice (Fricker 2007) |
| **Hermeneutical Injustice** | Interpretive gap due to lacking shared conceptual resources (Fricker 2007) |
| **Contributory Injustice** | Wilful hermeneutical ignorance by dominant groups (Dotson 2011) |
| **Epistemic Injustice Index (EII)** | Composite metric: EII = EII_testimonial × EII_hermeneutical ∈ [0,1] |
| **Testimonial Injustice Index (EII_t)** | Credibility deficit from behavioral traces (0–1) |
| **Hermeneutical Injustice Index (EII_h)** | Interpretive resource gap from resource metrics (0–1) |
| **Credibility Attribution** | Assigned credibility to speaker based on identity, not content |
| **Hermeneutical Resources** | Shared interpretive tools: vocabulary, templates, expert access, taxonomies |
| **Intersectionality** | Multiplicative compounding of disadvantage across identity axes |
| **Credibility Protocol** | Structured process for assigning credibility based on evidence, not identity |
| **Hermeneutical Resource** | Shared interpretive tool: vocabulary, template, expert, taxonomy |

---

## 3. Protocol Specification

### 3.1 Epistemic Injustice Index (EII)

**Requirement 1**: Organizations MUST compute EII quarterly as:

```
EII = EII_testimonial × EII_hermeneutical
```

Where:
- `EII_testimonial` ∈ [0,1] from behavioral traces (weight 0.6) + surveys (0.4)
- `EII_hermeneutical` ∈ [0,1] from resource metrics (0.6) + surveys (0.4)
- Both sub-indices computed with 95% CI via bootstrap (1000 iterations)

**Requirement 1.1**: EII interpretation thresholds:

| EII Range | Classification | Action |
|-----------|----------------|--------|
| EII ≤ 0.2 | **Aligned** | Routine monitoring |
| 0.2 < EII ≤ 0.4 | **Unjust** | Targeted remediation |
| 0.4 < EII ≤ 0.6 | **Severely Unjust** | Mandatory protocol remediation |
| EII > 0.6 | **Critically Unjust** | Leadership intervention; external audit |

### 3.2 Testimonial Injustice Index (EII_t)

**Requirement 2**: EII_testimonial MUST be computed from:

| Trace | Metric | Weight |
|-------|--------|--------|
| **PR Review Latency** | Median time to first substantive review by identity | 0.20 |
| **Speaking Time** | Meeting time share vs. org proportion | 0.20 |
| **Decision Attribution** | % decisions attributed to proposer by identity | 0.20 |
| **Incident Blame** | % incidents blamed on identity group | 0.20 |
| **Documentation Attribution** | % docs credited to author by identity | 0.10 |
| **Expert Invitation** | % invited as expert/consultant by identity | 0.10 |

**Requirement 3**: Credibility attribution model:

```
Credibility_score = Σ (w_i × trace_i) / Σ w_i
```

Calibrated so that identity-blind evaluation would yield uniform distribution.

**Requirement 4**: Survey component (40%) MUST use validated instrument:

| Item | Scale | Reverse Coded |
|------|-------|---------------|
| "My technical contributions are taken seriously" | 1–5 | No |
| "I have to work harder to be believed" | 1–5 | Yes |
| "My expertise is recognized without title" | 1–5 | No |
| "Colleagues defer to my judgment in my domain" | 1–5 | No |

### 3.3 Hermeneutical Injustice Index (EII_h)

**Requirement 5**: EII_hermeneutical MUST be computed from three resource dimensions:

| Resource | Metric | Weight |
|----------|--------|--------|
| **Vocabulary Diversity** | Shannon entropy of concept vocabulary in docs per identity group | 0.35 |
| **Template Coverage** | % of experience categories with dedicated templates per identity | 0.35 |
| **Expert Access Latency** | Median time to reach domain expert by identity | 0.30 |

**Requirement 6**: Resource gap computed as:

```
EII_h = 1 − (Resource_score_identity / Resource_score_reference)
```

Where reference group = highest-resourced identity group.

**Requirement 7**: Sub-dimension thresholds:

| Resource | Gap Threshold | Action |
|----------|---------------|--------|
| Vocabulary Diversity | < 0.7× reference | Expand vocabulary; create glossary |
| Template Coverage | < 0.5× reference | Create missing templates |
| Expert Access Latency | > 2× reference | Deploy expert network; reduce latency |

### 3.4 Intersectional EII

**Requirement 8**: Intersectional EII MUST use multiplicative compounding:

```
EII_intersectional = 1 − Π(1 − EII_axis_i)
```

Where axes include: gender, race, seniority, neurotype, role, tenure, location.

**Requirement 9**: Single-axis EII MUST be reported alongside intersectional EII.

### 3.5 Normative Requirements Summary

| Req | Parameter | MUST | SHOULD | MAY |
|-----|-----------|------|--------|-----|
| 1 | EII = EII_t × EII_h | YES | | |
| 1.1 | EII thresholds table | YES | | |
| 2 | EII_t from 6 traces | YES | | |
| 3 | Credibility attribution model | YES | | |
| 3 | Survey instrument (4 items) | YES | | |
| 5 | EII_h from 3 resources | YES | | |
| 6 | Resource gap formula | YES | | |
| 7 | Resource thresholds table | YES | | |
| 8 | Intersectional multiplicative | YES | | |
| 9 | Single-axis + intersectional reporting | YES | | |

---

## 4. Remediation Protocols

### 4.1 Testimonial Injustice Remediation

**Requirement 10**: Organizations with EII_t > 0.3 MUST implement calibrated
credibility protocols:

| Protocol | Mechanism | Mandatory |
|----------|-----------|-----------|
| **Blind PR Review** | Author identity hidden until review complete | YES |
| **Calibrated Speaking Time** | Meeting timer with identity-blind allocation | YES |
| **Decision Attribution Log** | Mandatory decision rationale with evidence | YES |
| **Incident Blame Protocol** | Blameless postmortem template (RFC-0004) | YES |
| **Attribution Audit** | Quarterly audit of decision attribution by identity | YES |

**Requirement 11**: Calibration MUST be audited quarterly by independent
epistemology auditor (RFC-0016).

### 4.2 Hermeneutical Injustice Remediation

**Requirement 12**: Organizations with EII_h > 0.3 MUST redistribute
hermeneutical resources:

| Resource | Redistribution Action | Mandatory |
|----------|----------------------|-----------|
| **Vocabulary** | Co-create glossary with marginalized groups; mandate in docs | YES |
| **Templates** | Co-create templates for missing experiences (burnout, microaggression, neurodivergence) | YES |
| **Expert Access** | Deploy expert network; SLA ≤ 4h for all identity groups | YES |
| **Taxonomies** | Expand incident taxonomies with marginalized categories | YES |

**Requirement 13**: Co-creation MUST involve affected groups (participatory
design). Top-down imposition violates epistemic justice.

### 4.3 Intersectional Remediation

**Requirement 14**: Remediation plans MUST target highest-intersectional-EII
groups first (multiplicative priority).

**Requirement 15**: Remediation progress tracked quarterly with intersectional
EII decomposition.

---

## 5. CBP Exemption

### 5.1 Exclusion Mandate

**Requirement 16**: CBP channels (RFC-0017) MUST be explicitly excluded from
all EII computation:

- CBP edges filtered from social graph before EII computation
- CBP attendance excluded from "meeting participation" metrics
- CBP Visual Primitives (EYE_SYN, MUG_FLASH, HEAD_NOD) exempt from logging
- CBP participation NOT used as "knowledge sharing" evidence

### 5.2 Rationale

CBP integrity depends on psychological safety (Edmondson 1999). EII surveillance
on CBP channels destroys the very conditions that make CBP epistemically valuable
— the safety to share half-formed thoughts, admit confusion, ask "stupid"
questions. Surveillance on CBP channels would:
- Increase SUSPICION (RFC-0017 §3.7)
- Suppress the very knowledge flows EII seeks to measure
- Violate the fiction firewall (EI-4)

---

## 6. Intersectional EII Computation

### 6.1 Multiplicative Compounding

```
EII_intersection = 1 - Π(1 - EII_axis_i)
```

Example: Woman (EII=0.3) + Junior (EII=0.2) + Remote (EII=0.15)
→ EII_intersection = 1 - (0.7 × 0.8 × 0.85) = 0.523

### 6.2 Reporting Requirements

**Requirement 17**: Reports MUST include:
- Single-axis EII for each tracked identity axis
- Top-10 highest intersectional EII groups
- Remediation progress by intersectional group

---

## 7. Security & Privacy Considerations

### 7.1 Epistemic Security

EII data reveals:
- Who is systematically disbelieved (political vulnerability)
- Who lacks interpretive resources (bus factor)
- Injustice patterns (power mapping)

**Requirement 18**: EII data SHALL be classified at same level as compensation
data. Access limited to: measured units, C-suite, independent epistemology auditor.

### 7.2 Individual Privacy

EII uses digital traces (Git, Jira, Slack, Calendar, HRIS).

**Requirement 19**: Aggregation to team level (minimum 5 individuals) before
EII computation. Individual-level graphs PROHIBITED for EII reporting.

**Requirement 20**: Survey responses MUST be anonymized. Minimum response
threshold: 3 respondents per identity group.

### 7.3 CBP Integrity (RFC-0017 §7)

**Requirement 21**: CBP edges used in EII MUST be anonymized and aggregated.
No executive attendance tracking for EII purposes.

---

## 8. OSC Considerations

### 8.1 Registry Updates

This RFC requests:
- RFC-0010 allocated in Standards Track, epistemology area (0200–0299)
- Keywords: epistemic-injustice, testimonial-injustice, hermeneutical-injustice,
  credibility, intersectionality, credibility-protocol
- See-also: RFC-0009, RFC-0007, RFC-0017

### 8.2 Code Points

EIRP defines no code points. EII thresholds and remediation triggers are
informational guidelines.

---

## 9. References

### 9.1 Normative References

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003,
Organizational Standards Consortium, 1992. https://rfc.osc.org/rfc0003

[RFC-0007] Matos, R.M. "Organizational Amnesia Prevention Protocol (OAPP)." RFC 0007,
OSC, 2008. https://rfc.osc.org/rfc0007

[RFC-0009] Matos, R.M. "Knowledge Hoarding Incentive Structure (KHIS)." RFC 0009,
OSC, 2026. https://rfc.osc.org/rfc0009

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017, OSC, 2001.
https://rfc.osc.org/rfc0017

### 9.2 Informative References

Dotson, Kristie. 2011. "Tracking Epistemic Violence, Tracking Practices of
Silencing." *Hypatia* 26 (2): 236–257. https://doi.org/10.1111/j.1527-2001.2011.01177.x

Fricker, Miranda. 2007. *Epistemic Injustice: Power and the Ethics of Knowing*.
Oxford: Oxford University Press.

Medina, José. 2013. *The Epistemology of Resistance: Gender and Racial Oppression,
Epistemic Injustice, and Resistant Imaginations*. Oxford: Oxford University Press.

Dotson, Kristie. 2014. "Conceptualizing Epistemic Oppression." *Social
Epistemology* 28 (2): 115–138. https://doi.org/10.1080/02691728.2013.782585

---

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-07-18 | Rodolfo Matos | Initial draft per HOSTILE_ANALYSIS_RFC0010.md |

## Appendix B: Open Issues

1. **EII Causal Direction**: Does high EII cause poor outcomes, or do poor
   outcomes attract injustice? Longitudinal RCT needed. [UNVERIFIED]

2. **Credibility Calibration Ground Truth**: How to validate credibility model
   without circularity? Ground truth requires external expert panel.
   [UNVERIFIED]

3. **Hermeneutical Resource Valuation**: How to weight vocabulary vs templates
   vs expert access? Impact on EII_h sensitivity unknown. [UNVERIFIED]

4. **Intersectional Data Sparsity**: Small intersectional groups yield noisy
   EII estimates. Minimum group size thresholds needed. [UNVERIFIED]

5. **Remediation Feedback Loop**: How fast does EII respond to remediation?
   Calibration of correction latency (λ) needed. [UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Fricker, Dotson, Medina, Fricker, Dotson,
> Medina, etc.) are accurate. The coffee machine, however, is real — and it
> is currently synchronizing more knowledge than this protocol ever will.