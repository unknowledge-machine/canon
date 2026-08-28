---
rfc: "0029"
title: "Epistemic Failure Mode Taxonomy (EFMT)"
stream: "Standards Track"
status: "DRAFT"
category: "Informational"
area: "epistemology"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-19"
updated: "2026-07-19"
obsoletes: []
obsoleted_by: []
see_also: [1, 2, 3, 4, 5, 6, 7, 9, 10, 14, 16, 17, 23, 24, 25, 26, 27, 28]
keywords: [failure-mode, taxonomy, epistemic-capture,
  cognitive-bias, narcissism, knowledge-loss,
  organizational-pathology]
abstract: |
  This document specifies the Epistemic Failure Mode Taxonomy (EFMT),
  a formal classification system for organizational epistemic
  pathologies. EFMT defines 7 primary failure categories, 23
  specific failure modes, detection metrics with thresholds,
  and intervention protocols mapped to the OEP canon. EFMT
  operationalizes the Organizational Epistemology Project's
  diagnostic apparatus for use in governance, audit, and
  organizational design. The taxonomy is grounded in empirical
  cases documented in Paper-011 and validated against the
  RFC canon.
dual_layer: true
satire_notice: "satire"
---

# RFC-0029 — Epistemic Failure Mode Taxonomy (EFMT)

## Abstract

This document specifies the Epistemic Failure Mode Taxonomy (EFMT),
a formal classification system for organizational epistemic
pathologies. EFMT defines 7 primary failure categories, 23
specific failure modes, detection metrics with thresholds,
and intervention protocols mapped to the OEP canon. EFMT
operationalizes the Organizational Epistemology Project's
diagnostic apparatus for use in governance, audit, and
organizational design. The taxonomy is grounded in empirical
cases documented in Paper-011 and validated against the
RFC canon.

> **Satire Notice**: This document is published in the
> **Standards Track** stream. While technically coherent,
> its primary purpose is satirical illumination of
> organizational pathologies. The OSC does not recommend
> deploying EFMT without IRB approval and a very large
> taxonomy of organizational sins.

## 1. Introduction

Organizations fail to know what they need to know. They
forget what they knew. They decide on the basis of status
signals rather than operational evidence. These are not
isolated incidents — they are instances of recurring
epistemic failure modes that follow predictable patterns.

The Epistemic Failure Mode Taxonomy (EFMT) provides a
standardized classification system for these pathologies.
Each failure mode is defined by:

- **Mechanism**: The structural or cognitive process
  producing the failure
- **Detection Metrics**: Quantifiable indicators with
  thresholds
- **Intervention Protocols**: Mapped to OEP RFCs
- **Severity**: CRITICAL / MAJOR / MINOR
- **Prevalence**: Estimated from field observations

EFMT is designed for use in:
- Organizational audits (pre-transformation, post-incident)
- Governance design (embedding detection in decision
  gates)
- Leadership assessment (screening for failure-mode
  propensity)
- Organizational design (structuring to avoid known
  failure modes)

## 2. Taxonomy Structure

EFMT organizes failure modes into 7 primary categories:

| Code | Category | Description |
|------|----------|-------------|
| **FM-EC** | Epistemic Capture | Position confers perceived epistemic authority that overrides evidence |
| **FM-CB** | Cognitive Bias | Systematic deviations from rational epistemic processing |
| **FM-NP** | Narcissistic Proximity | Leadership narcissism manifests as proximity control |
| **FM-KH** | Knowledge Hoarding | Incentives drive withholding of knowledge |
| **FM-KL** | Knowledge Loss | Structural conditions cause irreversible knowledge decay |
| **FM-CT** | Committee Theater | Decision-making bodies perform deliberation without genuine judgment |
| **FM-PT** | Presence Theater | Physical presence mandated without productivity justification |

Each category contains specific failure modes (FM-XXX-XX)
with unique codes, detection metrics, and interventions.

## 3. Category Definitions

### 3.1 FM-EC: Epistemic Capture

**Definition:** Organizational positions confer perceived
epistemic authority that systematically overrides
operational evidence. The holder of the position
believes they know better than those doing the work,
and the organization acts as if this belief is true.

**Primary Failure Modes:**

| Code | Name | Description |
|------|------|-------------|
| FM-EC-01 | Status Signal Override | Symbolic threat (missing honorific, title, seating) overrides all operational evidence of success |
| FM-EC-02 | Credential Epistemic Capture | Formal credential (degree, certification) overrides demonstrated competence |
| FM-EC-03 | Founder/Early-Staff Epistemic Erasure | New leader dismisses founding/early knowledge as obsolete |
| FM-EC-04 | Hierarchical Epistemic Gradient | Epistemic authority increases with hierarchical distance from operations |

**Detection Metrics:**
| Metric | Threshold | Source |
|--------|-----------|--------|
| ECI (RFC-0001) | ECI > 50 | RFC-0001 |
| NPCC (RFC-0028) | NPCC > 0.5 | RFC-0028 |
| DKC (RFC-0027) | DKC > 0.4 | RFC-0027 |
| Credential Gap | Gap > 1 level | RFC-0010 |

**Interventions:**
- RFC-0001: ECI monitoring with mandatory shadowing at ECI > 50
- RFC-0023: Promotion Gate requires tacit knowledge demonstration
- RFC-0010: EIRP panel for credential-based credibility discounting
- RFC-0023: Narcissism screening (NPI-16) for leadership roles

### 3.2 FM-CB: Cognitive Bias

**Definition:** Systematic deviations from rational epistemic
processing that are amplified by organizational structures
and incentives.

**Primary Failure Modes:**

| Code | Name | Description |
|------|------|-------------|
| FM-CB-01 | Dunning-Kruger Epistemic Capture | Incompetence prevents recognition of incompetence; leader cannot evaluate subordinate expertise |
| FM-CB-02 | False Consensus Effect | Leader overestimates agreement; dissent suppressed as "misalignment" |
| FM-CB-03 | Telepathy Demand | Subordinates expected to infer unstated intent; explicit guidance absent |
| FM-CB-04 | Confirmation Bias in Governance | Information filtered to confirm leader's prior beliefs |
| FM-CB-05 | Sunk Cost in Epistemic Commitments | Failed initiatives continued because leader committed to them |

**Detection Metrics:**
| Metric | Threshold | Source |
|--------|-----------|--------|
| DKC (RFC-0027) | DKC > 0.4 | RFC-0027 |
| FCI (RFC-0027) | FCI > 0.3 | RFC-0027 |
| TDI (RFC-0027) | TDI > 5 | RFC-0027 |
| BAF (RFC-0027) | BAF > 1.5 | RFC-0027 |

**Interventions:**
- RFC-0027: CBQP quarterly measurement with BAF stress-testing
- RFC-0023: Promotion Gate requires bias screening
- RFC-0010: EIRP panel for bias-related epistemic injustice
- RFC-0017: CBP as debiasing channel (protected from monitoring)

### 3.3 FM-NP: Narcissistic Proximity

**Definition:** Leadership narcissism manifests as mandatory
physical proximity requirements that serve narcissistic
supply (visual dominance, real-time admiration, compliance
performances, mirror-gazing) rather than productivity.

**Primary Failure Modes:**

| FM-NP-01 | Narcissistic Proximity Control | Mandates driven by leader's supply need, not productivity |
| FM-NP-02 | Supply Disruption Retaliation | Remote work adoption triggers punitive presence mandates |
| FM-NP-03 | Mirror-Gazing Escalation | Leader time allocation shifts from value-adding to visibility-seeking |
| FM-NP-04 | **Architecture Theater** | Leaders perform Supply Architecture Redesign without genuine channel shift (e.g., renaming channels, cosmetic dashboard changes) |

**Detection Metrics:**
| Metric | Threshold | Source |
|--------|-----------|--------|
| NPCC (RFC-0028) | NPCC > 0.5 | RFC-0028 |
| PTI (RFC-0028) | PTI > 1.5 | RFC-0028 |
| MGI (RFC-0028) | MGI > 2.0 | RFC-0028 |
| ASM (RFC-0028) | ASM > 0.3 | RFC-0028 |
| **G(O) trend (RFC-0006)** | **No improvement for 2 quarters** | **RFC-0006** |
| **CCR Coverage (RFC-0032)** | **< 0.7** | **RFC-0032** |
| **CCR Outcome Correlation** | **< 0.5** | **RFC-0032 §4.3** |

**Interventions:**
- RFC-0028: MPCC monitoring with board alerts at NPCC > 0.5
- RFC-0023: Narcissism screening (NPI-16) for leadership
- RFC-0017: CBP channels as narcissism-free zones
- RFC-0024: Trench Intelligence channels must bypass proximity mandates
- RFC-0032: PTDP activation for Architecture Theater
- RFC-0031: NSST Level 3 (Supply Architecture Redesign) with independent audit

### 3.4 FM-KH: Knowledge Hoarding

**Definition:** Incentive structures systematically reward
withholding knowledge when sharing would benefit the
organization.

**Primary Failure Modes:**

| Code | Name | Description |
|------|------|-------------|
| FM-KH-01 | Single Point of Knowledge Failure | Unique competency not externalized; no redundancy |
| FM-KH-02 | Hoarding as Career Strategy | Unique knowledge = job security; sharing = replaceability |
| FM-KH-03 | Hoarding Theater | Performative sharing without substantive transfer |

**Detection Metrics:**
| Metric | Threshold | Source |
|--------|-----------|--------|
| KHI (RFC-0009) | KHI > 0.4 | RFC-0009 |
| TEC_multiplier (RFC-0016) | Any role > 4× | RFC-0016 |
| CBP Avoidance (RFC-0009) | CBP avoidance > 30% | RFC-0009 |

**Interventions:**
- RFC-0009: Incentive restructuring (Career > Status > Social > Monetary)
- RFC-0007: KHL monitoring with mandatory KCP for TEC > 4
- RFC-0016: TEC_aggregate monitoring with emergency backup
- RFC-0017: CBP exclusion from KHI (CBP = debiasing channel)

### 3.5 FM-KL: Knowledge Loss

**Definition:** Structural conditions cause irreversible
decay or loss of institutional knowledge.

**Primary Failure Modes:**

| Code | Name | Description |
|------|------|-------------|
| FM-KL-01 | Succession Knowledge Erasure | Leadership transition without knowledge transfer |
| FM-KL-02 | Tool Migration Amnesia | Migration abandons untagged knowledge (RFC-0007) |
| FM-KL-03 | Procurement Knowledge Loss | External replacement fails; internal knowledge gone |
| FM-KL-04 | Restructuring Amnesia | Reorg without KCP (RFC-0007) |

**Detection Metrics:**
| Metric | Threshold | Source |
|--------|-----------|--------|
| KHL (RFC-0007) | KHL < 12 months (Existential/Critical) | RFC-0007 |
| TEC_multiplier (RFC-0016) | Any role > 8× | RFC-0016 |
| KCP absent (RFC-0007) | Reorg without KCP | RFC-0007 |
| KDR (RFC-0016) | KDR drops < 0.3 | RFC-0016 |

**Interventions:**
- RFC-0007: Mandatory KCP for reorgs ≥ 5 people / ≥ 2 teams
- RFC-0016: TEC monitoring with emergency backup trigger
- RFC-0016: Tagged-only migration with abandonment register
- RFC-0017: CBP edges as amnesia-resistant sync channels

### 3.6 FM-CT: Committee Theater

**Definition:** Decision-making bodies perform deliberation
without genuine judgment; outcomes are predetermined by
power dynamics, not evidence.

**Primary Failure Modes:**

| Code | Name | Description |
|------|------|-------------|
| FM-CT-01 | Compensation Committee Theater | Generic policy applied to unique knowledge asset |
| FM-CT-02 | Governance Theater | Steering committee rubber-stamps executive decisions |
| FM-CT-03 | Consensus Theater | Dissent suppressed; performative agreement |
| FM-CT-04 | Homogeneous Committee on Heterogeneous Asset | Committee lacks diversity to evaluate unique asset |

**Detection Metrics:**
| Metric | Threshold | Source |
|--------|-----------|--------|
| Committee Homogeneity Index (CHI) | CHI > 0.7 | RFC-0014 |
| Decision Avoidance Index (DAI) | DAI > 0.6 | RFC-0011 |
| Dissent Suppression Index (DSI) | DSI > 0.5 | RFC-0014 |
| Committee Entropy Score (CES) | CES > 0.5 | Paper-007 |

**Interventions:**
- RFC-0014: DSI monitoring with mandatory dissent periods
- RFC-0004: Decision Theater intervention (structured dissent, anonymous voting)
- RFC-0023: Promotion Gate requires heterogeneous committee composition
- Theorem-002: Committee size cap at 9 for genuine deliberation

### 3.7 FM-PT: Presence Theater

**Definition:** Physical presence mandated without
productivity justification; attendance decoupled from
output.

**Primary Failure Modes:**

| Code | Name | Description |
|------|------|-------------|
| FM-PT-01 | Presence Theater | Mandated attendance decoupled from productivity |
| FM-PT-02 | Surveillance Escalation | Badge tracking → cameras → keystroke logging |
| FM-PT-03 | Compliance Theater | Badge in / Slack green / mental absence |

**Detection Metrics:**
| Metric | Threshold | Source |
|--------|-----------|--------|
| PTI (RFC-0028) | PTI > 1.5 | RFC-0028 |
| PCS escalation | > 1 level/quarter | RFC-0028 |
| Badge/productivity correlation | < 0.2 | RFC-0028 |

**Interventions:**
- RFC-0028: MPCC monitoring with board alerts
- RFC-0017: CBP protection (no executive surveillance)
- RFC-0024: Trench Intelligence channels bypass proximity
- RFC-0023: Narcissism screening before leadership

## 4. Detection and Intervention Matrix

### 4.1 Unified Detection Dashboard

| Metric | Category | Frequency | Alert Threshold | Auto-Escalation |
|--------|----------|-----------|-----------------|-----------------|
| ECI | FM-EC | Monthly | > 50 | Board |
| NPCC | FM-NP | Quarterly | > 0.5 | Board |
| DKC | FM-CB | Quarterly | > 0.4 | Audit |
| PTI | FM-NP/FM-PT | Quarterly | > 1.5 | CTO/CEO |
| KHI | FM-KH | Quarterly | > 0.4 | CTO |
| TEC_multiplier | FM-KL | Continuous | > 4 | CTO/Board |
| CHI | FM-CT | Per decision | > 0.7 | Decision owner |
| PTI | FM-PT | Quarterly | > 1.5 | CTO/CEO |

### 4.2 Intervention Mapping

| Failure Mode | Primary Protocol | Supporting Protocols | Escalation Path |
|--------------|------------------|----------------------|-----------------|
| FM-EC-01 | RFC-0001 (ECI reduction) | RFC-0023, RFC-0017 | Board |
| FM-EC-02 | RFC-0023 (PGP) | RFC-0010, RFC-0017 | EIRP Panel |
| FM-EC-03 | RFC-0025 (SEP) | RFC-0023, RFC-0024 | Board |
| FM-CB-01 | RFC-0027 (CBQP) | RFC-0023, RFC-0010 | Audit |
| FM-CB-03 | RFC-0027 (TDI) | RFC-0023, RFC-0024 | CTO |
| FM-NP-01 | RFC-0028 (MPCC) | RFC-0017, RFC-0023, RFC-0024 | Board |
| FM-KH-01 | RFC-0016 (Emergency backup) | RFC-0007, RFC-0009 | CTO/Board |
| FM-KL-01 | RFC-0007 (KCP) | RFC-0016, RFC-0025 | Board |
| FM-KL-03 | RFC-0016 (Emergency backup) | RFC-0007 | CTO/Board |
| FM-CT-01 | RFC-0014 (DTS) | RFC-0004, RFC-0023 | Decision owner |
| FM-NP-01 | RFC-0028 (MPCC) | RFC-0017, RFC-0023, RFC-0024 | Board |
| FM-PT-01 | RFC-0028 (MPCC) | RFC-0017, RFC-0024 | CTO/CEO |

## 5. Case Mapping (Paper-011)

| Case | Primary FM | Secondary FMs | Paper-011 Section |
|------|------------|---------------|-------------------|
| FM-001 (Honorific Cancellation) | FM-EC-01 | FM-DT-03 | 2.1 |
| FM-002 (Doctorate Deficit) | FM-EC-02 | FM-CB-01 | 2.2 |
| FM-003 (Specialists Directive) | FM-EC-03 | FM-CB-01, FM-NP-01 | 2.3 |
| FM-004 (10% Technician) | FM-KH-01 | FM-CT-01, FM-KL-03 | 2.4 |
| FM-005 (Mandatory Presence) | FM-NP-01 | FM-PT-01 | 2.5 |

## 6. Implementation Guidance

### 6.1 Organizational Audit Protocol

1. **Baseline Measurement**: Compute all detection metrics
   for current state
2. **Threshold Mapping**: Identify which failure modes
   exceed thresholds
3. **Root Cause Analysis**: Map each active failure
   mode to its structural cause (RFC mapping)
4. **Intervention Sequencing**: Prioritize by severity
   (CRITICAL → MAJOR → MINOR) and dependency order
5. **Governance Embedding**: Add detection metrics to
   board dashboards; intervention protocols to
   decision gates

### 6.2 Governance Integration

| Governance Body | EFMT Integration |
|-----------------|------------------|
| Board | Quarterly EFMT dashboard; NPCC > 0.5 auto-alert |
| Audit Committee | Annual EFMT audit; TEC_multiplier > 4 review |
| CTO/Technology | Monthly PTI, TDI, KHI; TEC_multiplier > 4 alert |
| HR/Compensation | KHI quarterly; TEC_multiplier for retention decisions |
| Legal/Compliance | KHL tracking for regulatory knowledge domains |

## 7. Open Issues

1. **Calibration**: Thresholds derived from limited
   samples; cross-organization calibration needed.
2. **Cultural Moderation**: High-power-distance
   cultures may show different baseline metrics.
3. **Remote-First Organizations**: Metrics may
   invert (e.g., PTI < 1.0 may indicate disconnection).
4. **AI-Mediated Leadership**: Does AI decision
   support reduce or amplify failure modes?
5. **Longitudinal Validation**: Do interventions
   sustain failure mode reduction over 24+ months?

## 8. References

### 8.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001.
[RFC-0004] Matos, R. "Decision Theater Specification (DTS)." RFC 0004.
[RFC-0005] Matos, R. "Knowledge Gravity Measurement Framework (KGMF)." RFC 0005.
[RFC-0007] Matos, R.M. "Organizational Amnesia Prevention Protocol (OAPP)." RFC 0007.
[RFC-0009] Matos, R.M. "Knowledge Hoarding Incentive Structure (KHIS)." RFC 0009.
[RFC-0010] Matos, R.M. "Epistemic Injustice Remediation Protocol (EIRP)." RFC 0010.
[RFC-0011] Matos, R. "Meeting Entropy Acceleration Protocol (MEAP)." RFC 0011.
[RFC-0014] Matos, R. "Consensus Theater Choreography." RFC 0014.
[RFC-0016] Matos, R. "Institutional Memory Backup Specification (IMBP)." RFC 0016.
[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017.
[RFC-0023] Matos, R. "Promotion Gate Protocol (PGP)." RFC 0023.
[RFC-0024] Matos, R. "Trench Intelligence Protocol (TIP)." RFC 0024.
[RFC-0025] Matos, R. "Succession Entropy Protocol (SEP)." RFC 0025.
[RFC-0026] Matos, R. "Wernham Hogg Protocol (WHP)." RFC 0026.
[RFC-0027] Matos, R. "Cognitive Bias Quantification Protocol (CBQP)." RFC 0027.
[RFC-0028] Matos, R. "Mandatory Presence Enforcement Protocol (MPEP)." RFC 0028.

### 8.2 Informative References

[Paper-011] Matos, R.M. "Organizational Epistemology
Failure Modes: A Case Compendium." Paper 011,
OSC, 2026.
[Theorem-001] Matos, R. "Coffee Machine Theorem." Theorem 1.
[Theorem-002] Matos, R. "Committee Entropy Theorem." Theorem 2.
[Theorem-003] Matos, R. "Knowledge Gravity Theorem." Theorem 3.
[Theorem-004] Matos, R. "Epistemic Fragmentation Bound." Theorem 4.
[Theorem-005] Matos, R. "Tacit Knowledge Inexpressibility Theorem." Theorem 5.

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs published under the OSC imprint are satirical artifacts
> that encode genuine organizational science. The taxonomy, however, is real
> — and your organization is currently exhibiting at least three of these
> failure modes.