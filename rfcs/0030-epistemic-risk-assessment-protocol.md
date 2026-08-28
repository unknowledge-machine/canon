---
rfc: "0030"
title: "Epistemic Risk Assessment Protocol (ERAP)"
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
see_also: [1, 5, 7, 16, 17, 23, 24, 27, 28]
keywords: [epistemic-risk, risk-assessment, leadership-appointment,
  operational-competence, knowledge-continuity, pre-deployment-checklist,
  epistemic-risk-assessment]
abstract: |
  This document specifies the Epistemic Risk Assessment Protocol (ERAP),
  a formal pre-deployment checklist for leadership appointments in
  operational domains. ERAP quantifies epistemic risk by measuring
  Trench Intelligence, Knowledge Gravity distortion, Epistemic Capture
  susceptibility, Knowledge Half-Life exposure, and Cognitive Bias
  amplification. ERAP produces a quantified Epistemic Risk Score (ERS)
  with mandatory intervention thresholds. ERAP is designed for use in
  board appointments, ministerial appointments, C-suite hiring, and any
  leadership role where epistemic distance from operational ground truth
  creates systemic risk.
dual_layer: true
satire_notice: "satire"
---

# RFC-0030 — Epistemic Risk Assessment Protocol (ERAP)

## Abstract

This document specifies the Epistemic Risk Assessment Protocol (ERAP),
a formal pre-deployment checklist for leadership appointments in
operational domains. ERAP quantifies epistemic risk by measuring
Trench Intelligence (RFC-0024), Knowledge Gravity distortion (RFC-0005),
Epistemic Capture susceptibility (RFC-0001), Knowledge Half-Life
exposure (RFC-0007), and Cognitive Bias amplification (RFC-0027).
ERAP produces a quantified Epistemic Risk Score (ERS) with mandatory
intervention thresholds. ERAP is designed for use in board appointments,
ministerial appointments, C-suite hiring, and any leadership role where
epistemic distance from operational ground truth creates systemic risk.

> **Satire Notice**: This document is published in the **Standards Track**
> stream. While technically coherent, its primary purpose is satirical
> illumination of organizational pathologies. The OSC does not recommend
> deploying ERAP without IRB approval and a very large mirror.

## 1. Introduction

Organizations routinely appoint leaders to operational domains where
they possess zero ground-truth access. The Minister of Education who
never corrected an exam. The CTO who never deployed to production. The
VP of Engineering who never debugged a production incident. The
Director of Nursing who never worked a night shift.

These appointments are not accidents — they are structural features of
hierarchical organizations. RFC-0001 (HOP) proves that hierarchical
position generates epistemic capture. RFC-0024 (TIP) proves that
Command Distance destroys Trench Intelligence. RFC-0007 (OAPP) proves
that Knowledge Half-Life collapses without explicit continuity
protocols.

The Epistemic Risk Assessment Protocol (ERAP) makes these risks
quantifiable and actionable *before* the appointment is made.

## 2. ERAP Scope and Applicability

### 1.1 Scope

ERAP applies to any leadership appointment where:

- The role has decision authority over operational domains
- The appointee lacks current, direct ground-truth access to the
  operational domain
- The domain has non-zero Knowledge Half-Life (RFC-0007)
- The domain has non-zero Turnover Entropy (RFC-0016)
- Failure would produce measurable harm (operational, financial,
  reputational, or human)

### 1.2 Applicability Matrix

| Role Type | ERAP Required? | Tier |
|-----------|----------------|------|
| Minister/Secretary of operational portfolio | **MANDATORY** | Tier 1 |
| C-suite operational roles (COO, CTO, CIO,
  CMO, CHRO) | **MANDATORY** | Tier 1 |
| VP/Director of operational domains | **MANDATORY** | Tier 1 |
| Board members with operational oversight | **RECOMMENDED** | Tier 2 |
| Project managers of knowledge-intensive projects | **RECOMMENDED** | Tier 2 |
| Team leads of knowledge-intensive teams | **OPTIONAL** | Tier 3 |

## 2. ERAP Assessment Framework

### 2.1 The Five Epistemic Risk Dimensions

ERAP computes an Epistemic Risk Score (ERS) across five dimensions:

| Dimension | RFC Source | Symbol | Weight | Range |
|-----------|------------|--------|--------|-------|
| Trench Intelligence Deficit | RFC-0024 | TID | 0.25 | [0, 1] |
| Knowledge Gravity Distortion | RFC-0005 | KGD | 0.20 | [0, 1] |
| Epistemic Capture Susceptibility | RFC-0001 | ECS | 0.20 | [0, 1] |
| Knowledge Half-Life Exposure | RFC-0007 | KHE | 0.20 | [0, 1] |
| Cognitive Bias Amplification | RFC-0027 | CBA | 0.15 | [0, 1] |

**ERS = 0.25×TID + 0.20×KGD + 0.20×ECS + 0.20×KHE + 0.15×CBA**

Each dimension scored [0, 1]; ERS ∈ [0, 1].

### 2.2 Dimension Definitions and Measurement

#### 2.2.1 Trench Intelligence Deficit (TID)

**Definition**: The degree to which the appointee lacks current,
direct, hands-on experience in the operational domain they will govern.

**Measurement Protocol**:
```
TID = 1 - (Current_Ground_Truth_Access / Maximum_Possible_Access)

Current_Ground_Truth_Access =
  Σ (Experience_Weight_i × Recency_Decay_i × Relevance_i)

Where:
- Experience_Weight_i = 1.0 for hands-on execution, 0.5 for direct supervision,
  0.25 for adjacent role, 0 for unrelated
- Recency_Decay_i = e^(-λ × years_since) where λ = ln(2)/2 (half-life 2 years)
- Relevance_i = 1.0 for core domain, 0.5 for adjacent, 0.1 for tangential
```

**Scoring Guide**:
| TID Range | Classification | Example |
|-----------|----------------|---------|
| 0.0 - 0.2 | **Grounded** | Current practitioner, active in domain |
| 0.2 - 0.4 | **Adjacent** | Recent direct supervision, same domain |
| 0.4 - 0.6 | **Distant** | Adjacent domain, or >3 years removed |
| 0.6 - 0.8 | **Remote** | No direct experience, or >7 years removed |
| 0.8 - 1.0 | **Blind** | Zero relevant experience
  (political appointee, academic, consultant) |

**Evidence Sources**: CV, LinkedIn, portfolio, references,
  skills assessment, simulation exercise.

#### 2.2.2 Knowledge Gravity Distortion (KGD)

**Definition**: The degree to which the appointee's decision-making will be
distorted by power-knowledge gravity wells (RFC-0005).

**Measurement Protocol**:
```
KGD = (Power_Centrality_Score - Truth_Centrality_Score) / max(Power, Truth)

Where:
- Power_Centrality_Score = weighted centrality in formal authority network
- Truth_Centrality_Score = weighted centrality in operational knowledge network
```

**Scoring Guide**:
| KGD Range | Classification | Indicators |
|-----------|----------------|------------|
| < -0.3 | **Truth-Dominant** | Practitioner, engineer, clinician |
| -0.3 to 0.1 | **Balanced** | Technical leader with management scope |
| 0.1 to 0.4 | **Power-Drifting** | Manager with fading technical currency |
| 0.4 to 0.7 | **Power-Dominant** | Pure manager, no recent technical work |
| > 0.7 | **Gravity Well** | Pure executive, no operational contact |

**Evidence Sources**: Org chart position, meeting patterns, calendar analysis,
GitHub/Jira activity, code review history, incident response participation.

#### 2.2.3 Epistemic Capture Susceptibility (ECS)

**Definition**: The likelihood that hierarchical position will generate
unwarranted confidence in operational knowledge (RFC-0001 HOP).

**Measurement Protocol**:
```
ECS = α × Hierarchical_Level + β × Tenure_in_Position +
  γ × Authority_Span + δ × Insulation_Index

Where:
- Hierarchical_Level = distance from operational frontline
  (0 = frontline, 1 = CEO)
- Tenure_in_Position = years in current role (capped at 5)
- Authority_Span = log10(number of indirect reports + 1)
- Insulation_Index = 1 - (direct_operational_interactions
  _per_week / max_possible)
```

**Calibration**: α=0.3, β=0.2, γ=0.2, δ=0.3 (normalized to [0,1])

**Scoring Guide**:
| ECS Range | Classification |
|-----------|----------------|
| 0.0 - 0.3 | **Low** - Frontline, short tenure, small span, high contact |
| 0.3 - 0.5 | **Moderate** - Mid-management, 2-3 years, moderate span |
| 0.5 - 0.7 | **High** - Senior management, 3+ years, wide span |
| 0.7 - 1.0 | **Critical** - C-suite/Minister, 5+ years, large span, insulated |

#### 2.2.4 Knowledge Half-Life Exposure (KHE)

**Definition**: The risk that critical knowledge will decay before it can
be transferred or operationalized (RFC-0007).

**Measurement Protocol**:
```
KHE = max_i (Criticality_i × (1 - Retention_Probability_i))

Where for each critical knowledge domain i:
- Criticality_i = [0,1] business impact if lost
- Retention_Probability_i = probability knowledge survives next 18 months
  = f(documentation_quality, holder_retention_risk, transfer_plan_maturity)
```

**Criticality Levels**:
| Level | Definition | Weight |
|-------|------------|--------|
| 0 (Existential) | Org survival depends on it | 1.0 |
| 1 (Critical) | Severe operational/regulatory impact | 0.8 |
| 2 (High) | Significant degradation | 0.6 |
| 3 (Important) | Measurable degradation | 0.4 |
| 4 (Useful) | Minor inconvenience | 0.2 |

**Retention Probability Factors**:
- Documentation quality (0-1)
- Holder retention probability (0-1)
- Transfer plan maturity (0-1)
- Redundancy (number of holders)

**KHE Scoring**:
| KHE Range | Classification |
|-----------|----------------|
| 0.0 - 0.2 | **Low** - All critical knowledge documented,
  redundant, transferrable |
| 0.2 - 0.4 | **Moderate** - Some gaps, but mitigated |
| 0.4 - 0.6 | **High** - Critical knowledge at risk |
| 0.6 - 0.8 | **Severe** - Existential knowledge at risk |
| 0.8 - 1.0 | **Catastrophic** - Existential knowledge will be lost |

#### 2.2.5 Cognitive Bias Amplification (CBA)

**Definition**: The degree to which the appointee's cognitive biases will
be amplified by position and stress (RFC-0027 CBQP).

**Measurement Protocol**:
```
CBA = (DKC + FCI + TDI + BCIC) / 4

Where each component ∈ [0,1] assessed via:
- DKC: Self-assessment vs peer assessment gap (validated instrument)
- FCI: Estimated agreement vs actual agreement (validated instrument)
- TDI: Ambiguity tolerance × decision urgency / explicit guidance
- BCIC: -Corr(bias_score, competence_proxy)
```

**Scoring Guide**:
| CBA Range | Classification |
|-----------|----------------|
| 0.0 - 0.2 | **Low** - High self-awareness, seeks disconfirmation |
| 0.2 - 0.4 | **Moderate** - Some blind spots, open to feedback |
| 0.4 - 0.6 | **High** - Significant blind spots, defensive |
| 0.6 - 1.0 | **Critical** - Severe blind spots, dismisses disconfirmation |

**Assessment Methods**: Validated instruments (Kruger-Dunning scale,
False Consensus scale, ambiguity tolerance scale), 360-degree review,
simulation exercises.

## 3. Epistemic Risk Score (ERS) and Thresholds

### 3.1 ERS Computation

```
ERS = 0.25×TID + 0.20×KGD + 0.20×ECS + 0.20×KHE + 0.15×CBA
```

### 3.2 Risk Classification and Mandatory Actions

| ERS Range | Risk Level | Mandatory Action | Timeline |
|-----------|------------|------------------|----------|
| 0.00 - 0.20 | **LOW** | Standard onboarding | N/A |
| 0.20 - 0.40 | **MODERATE** | Enhanced onboarding +
  mentor assignment | 30 days |
| 0.40 - 0.60 | **HIGH** | Mandatory Trench Immersion + Mentor + KCP | 60 days |
| 0.60 - 0.80 | **CRITICAL** | Trench Immersion + Shadow Cabinet
  + KCP + External Auditor | 90 days |
| 0.80 - 1.00 | **EXISTENTIAL** | **APPOINTMENT BLOCKED**
  pending remediation | N/A |

### 3.2.1 Mandatory Intervention Protocols

#### ERS ≥ 0.80 (EXISTENTIAL) — APPOINTMENT BLOCKED
**Required Remediation Before Appointment**:
- [ ] TID < 0.6: Demonstrable ground-truth acquisition (simulation,
  shadowing, residency ≥ 30 days)
- [ ] KHE < 0.6: Documented KCP with ≥80% critical knowledge
  coverage and transfer plan
- [ ] CBA < 0.7: Completed cognitive bias assessment with
  improvement plan
- [ ] Board sign-off on residual risk acceptance

#### ERS 0.60-0.80 (CRITICAL) — CONDITIONAL APPOINTMENT
**Required Within 90 Days**:
- [ ] Trench Immersion Program: ≥ 20 days in operational trenches
- [ ] Shadow Cabinet: Assigned epistemic partner with ground-truth access
- [ ] KCP: Knowledge Continuity Plan for all critical domains
- [ ] Monthly ERS re-evaluation for first 6 months
- [ ] External Auditor: Quarterly epistemic audit for first year

#### ERS 0.40-0.60 (HIGH) — ENHANCED ONBOARDING
**Required Within 60 Days**:
- [ ] Trench Immersion: ≥ 10 days in operational trenches
- [ ] Assigned Epistemic Mentor: Ground-truth holder, weekly sync
- [ ] KCP: Knowledge Continuity Plan for critical domains
- [ ] Quarterly ERS re-evaluation for first year

#### ERS 0.20-0.40 (MODERATE) — ENHANCED ONBOARDING
**Required Within 30 Days**:
- [ ] Assigned Epistemic Mentor
- [ ] Knowledge mapping workshop
- [ ] Quarterly ERS re-evaluation for first 6 months

### 3.3 Automatic Disqualifiers (Veto Conditions)

Regardless of composite ERS, the following trigger **automatic
appointment block**:

| Veto Condition | Rationale |
|----------------|-----------|
| TID = 1.0 (zero relevant experience) | No ground-truth access possible |
| KHE = 1.0 (existential knowledge loss certain) | Organizational suicide |
| CBA ≥ 0.9 (critical bias) | Uncorrectable epistemic distortion |
| TID > 0.8 AND KHE > 0.6 | Blind leader of decaying knowledge system |
| KGD > 0.8 AND ECS > 0.7 | Pure gravity well with epistemic capture |

## 4. ERAP Assessment Process

### 4.1 Assessment Timeline

| Phase | Activity | Duration | Owner |
|-------|----------|----------|-------|
| **Pre-Assessment** | Data gathering (CV, references,
  simulations, assessments) | 2 weeks | ERAP Analyst |
| **Assessment** | Dimension scoring, ERS calculation,
  threshold mapping | 1 week | ERAP Panel |
| **Deliberation** | Panel review, veto check,
  intervention design | 3 days | ERAP Panel |
| **Decision** | Appoint / Conditional / Block | 1 day | Appointing Authority |
| **Onboarding** | Intervention protocol execution
  | Per threshold | Appointee + Mentor |

### 4.2 ERAP Panel Composition

| Role | Count | Qualifications |
|------|-------|----------------|
| Epistemology Auditor (Chair) | 1 | Certified ERAP Auditor, 5+ years |
| Domain Practitioner | 1 | Current practitioner in target domain |
| Cognitive Psychologist | 1 | PhD, bias assessment expertise |
| Knowledge Management Expert | 1 | RFC-0007/0016 certified |
| Independent Board Member | 1 | No conflict of interest |

**Quorum**: 4/5. **Veto Power**: Any member may trigger veto review.

### 4.3 Evidence Requirements

| Dimension | Required Evidence |
|-----------|-------------------|
| TID | CV, portfolio, simulations, reference interviews, skills assessment |
| KGD | Org chart, calendar analysis, Git/Jira data, meeting patterns |
| ECS | Org chart, tenure records, span of control, calendar analysis |
| KHE | Knowledge audit, documentation review, retention data, transfer plans |
| CBA | Validated instruments (Kruger-Dunning, FCI,
  ambiguity tolerance), 360-review |

## 5. ERAP Report Template

```
ERAP ASSESSMENT REPORT
======================

CANDIDATE: [Name, Role, Organization]
ASSESSMENT DATE: [Date]
ERAP VERSION: 1.0
PANEL: [Names, Roles]

DIMENSION SCORES:
-----------------
TID (Trench Intelligence Deficit):     [0.00-1.00]  [Classification]
KGD (Knowledge Gravity Distortion):    [0.00-1.00]  [Classification]
ECS (Epistemic Capture Susceptibility):[0.00-1.00]  [Classification]
KHE (Knowledge Half-Life Exposure):    [0.00-1.00]  [Classification]
CBA (Cognitive Bias Amplification):    [0.00-1.00]  [Classification]

COMPOSITE ERS: [0.00-1.00] [RISK LEVEL]

VETO CHECK: [PASS / FAIL - Details if FAIL]

THRESHOLD CLASSIFICATION: [LOW / MODERATE / HIGH / CRITICAL / EXISTENTIAL]

MANDATORY INTERVENTIONS:
[ ] Trench Immersion: [days required]
[ ] Shadow Cabinet: [assigned mentor]
[ ] KCP: [required coverage %]
[ ] Shadow Cabinet: [assigned]
[ ] External Auditor: [assigned]
[ ] Re-evaluation Schedule: [frequency]

EVIDENCE SUMMARY:
- TID Evidence: [list]
- KGD Evidence: [list]
- ECS Evidence: [list]
- KHE Evidence: [list]
- CBA Evidence: [list]

PANEL DECISION: [APPOINT / CONDITIONAL / BLOCK]
CHAIR SIGNATURE: _________________ DATE: __________

DISSENTING OPINIONS: [if any]
```

## 6. Case Study: Minister of Education (Applied Retrospectively)

### Input Data
- **Role**: Minister of Education
- **Background**: Academic (university professor), political career
- **Operational Experience**: Zero exam administration,
  zero IT procurement, zero large-scale logistics
- **Tenure**: New appointment
- **Domain**: National exam administration (500K+ students, 50K+ teachers)

### Dimension Scores

| Dimension | Score | Evidence |
|-----------|-------|----------|
| TID | 1.0 | Zero relevant operational experience |
| KGD | 0.85 | Pure authority position, zero operational centrality |
| ECS | 0.92 | Ministerial level, insulated, wide span |
| KHE | 0.75 | Exam system knowledge held by retiring staff, no KCP |
| CBA | 0.65 | Academic background + political confidence = DKC risk |

**ERS = 0.25×1.0 + 0.20×0.85 + 0.20×0.92 + 0.20×0.75 + 0.15×0.65 = 0.82**

**Classification: EXISTENTIAL → APPOINTMENT BLOCKED**

### Required Remediation (Would Have Been Mandatory)
- [ ] TID < 0.6: 30-day residency in exam correction centers
- [ ] KHE < 0.6: Documented KCP with 80% critical knowledge coverage
- [ ] CBA < 0.7: Cognitive bias assessment + improvement plan
- [ ] Board sign-off on residual risk

**Outcome**: Appointment would have been **BLOCKED** pending remediation.

## 7. Implementation Guidance

### 7.1 Organizational Adoption

| Phase | Activities | Timeline |
|-------|------------|----------|
| **Pilot** | Apply to 3-5 upcoming appointments | Months 1-3 |
| **Calibration** | Adjust weights/thresholds based on outcomes | Months 3-6 |
| **Standardize** | Embed in HR/appointment policies | Months 6-12 |
| **Automate** | Build ERAP tooling (CV parser, calendar analysis, simulation) | Year 2 |

### 7.2 Tooling Requirements

| Capability | Status |
|------------|--------|
| CV/LinkedIn parser for TID | Build |
| Calendar/email analysis for KGD/ECS | Build |
| Knowledge audit tool for KHE | Build |
| Bias assessment integration (Qualtrics/Typeform) | Integrate |
| ERS calculator dashboard | Build |
| Simulation engine for Trench Immersion | Build |

## 8. References

### 8.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001.
[RFC-0005] Matos, R.
"Knowledge Gravity Measurement Framework (KGMF)." RFC 0005.
[RFC-0007] Matos, R.M.
"Organizational Amnesia Prevention Protocol (OAPP)." RFC 0007.
[RFC-0016] Matos, R.
"Institutional Memory Backup Specification (IMBP)." RFC 0016.
[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017.
[RFC-0023] Matos, R. "Promotion Gate Protocol (PGP)." RFC 0023.
[RFC-0024] Matos, R. "Trench Intelligence Protocol (TIP)." RFC 0024.
[RFC-0027] Matos, R.
"Cognitive Bias Quantification Protocol (CBQP)." RFC 0027.
[RFC-0028] Matos, R.
"Mandatory Presence Enforcement Protocol (MPEP)." RFC 0028.
[RFC-0029] Matos, R. "Epistemic Failure Mode Taxonomy (EFMT)." RFC 0029.

### 8.2 Informative References

Kahneman, D. 2011. *Thinking, Fast and Slow*. Farrar, Straus and Giroux.

Kruger, J., and Dunning, D. 1999. "Unskilled and Unaware of It: How Difficulties
in Recognizing One's Own Incompetence Lead to Inflated Self-Assessments."
*Journal of Personality and Social Psychology* 77 (6): 1121–1134.

Ross, L., Greene, D., and House, P. 1977. "The 'False Consensus Effect': An
Egocentric Bias in Social Perception and Attribution Processes." *Journal of
Experimental Social Psychology* 13 (3): 279–301.

---

## Appendix A: Quick Reference Card

```
ERAP QUICK REFERENCE
====================

DIMENSIONS & WEIGHTS:
  TID  0.25  |  KGD  0.20  |  ECS  0.20  |  KHE  0.20  |  CBA  0.15

THRESHOLDS:
  < 0.20  LOW          → Standard onboarding
  0.20-0.40 MODERATE   → Enhanced onboarding + mentor (30d)
  0.40-0.60 HIGH       → Trench immersion + mentor + KCP (60d)
  0.60-0.80 CRITICAL   → Trench + Shadow + KCP + Auditor (90d)
  > 0.80  EXISTENTIAL  → BLOCKED until remediation

VETO TRIGGERS (ANY BLOCKS):
  ☐ TID = 1.0
  ☐ KHE = 1.0
  ☐ CBA ≥ 0.9
  ☐ TID > 0.8 AND KHE > 0.6
  ☐ KGD > 0.8 AND ECS > 0.7

INTERVENTIONS BY LEVEL:
  MODERATE:  Mentor + quarterly re-eval (30d)
  HIGH:      Trench (10d) + Mentor + KCP (60d)
  CRITICAL:  Trench (20d) + Shadow + KCP + Auditor (90d)
  EXISTENTIAL: BLOCKED until remediation complete

EVIDENCE REQUIREMENTS:
  TID: CV + portfolio + simulation + refs
  KGD: Org chart + calendar + Git/Jira + meetings
  ECS: Org chart + tenure + span + calendar
  KHE: Knowledge audit + docs + retention + transfer plan
  CBA: Validated instruments + 360 + simulation
```

## 9. Colophon

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs published under the OSC imprint are satirical artifacts
> that encode genuine organizational science. All citations of real scholars
> (Kahneman, Tversky, Kruger, Dunning, Ross, etc.) are accurate. The risk,
> however, is real — and your next leadership appointment is currently
> unassessed.