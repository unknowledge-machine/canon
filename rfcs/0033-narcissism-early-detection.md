---
rfc: "0033"
title: "Narcissism Early Detection Protocol (NEDP)"
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
see_also: [23, 24, 28, 30]
keywords:
  - narcissism
  - early-detection
  - screening
  - leadership-appointment
  - epistemic-risk
  - behavioral-proxies
abstract: |
  This document specifies the Narcissism Early Detection Protocol (NEDP),
  a pre-appointment screening protocol for narcissistic traits in leadership
  candidates. NEDP employs a three-module Screening Battery: (a) Behavioral
  Proxy Module extending the SEG26 CEO Narcissism Index (CNI) to leadership
  roles via signature size, photo prominence, and compensation gap; (b)
  Psychological Module with NPI-16, BFI-2, and DT-12; (c) 360° Observer
  Module with anonymized subordinate/peer ratings. The NEDP Risk Score (NRS)
  integrates these modules into a calibrated [0,1] score with thresholds
  Low (<0.3), Moderate (0.3-0.6), High (>0.6) that feed directly into
  RFC-0030 ERAP Dimensions 2 (Knowledge Gravity Distortion) and 5
  (Cognitive Bias Amplification) and RFC-0023 PGP pre-gate decisions.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0033 — Narcissism Early Detection Protocol (NEDP)

## Abstract

This document specifies the Narcissism Early Detection Protocol (NEDP),
a pre-appointment screening protocol for narcissistic traits in leadership
candidates. NEDP employs a three-module Screening Battery: (a) Behavioral
Proxy Module extending the SEG26 CEO Narcissism Index (CNI) to leadership
roles via signature size, photo prominence, and compensation gap; (b)
Psychological Module with NPI-16, BFI-2, and DT-12; (c) 360° Observer
Module with anonymized subordinate/peer ratings. The NEDP Risk Score (NRS)
integrates these modules into a calibrated [0,1] score with thresholds
Low (<0.3), Moderate (0.3-0.6), High (>0.6) that feed directly into
RFC-0030 ERAP Dimensions 2 (Knowledge Gravity Distortion) and 5
(Cognitive Bias Amplification) and RFC-0023 PGP pre-gate decisions.

> **Dual-Layer Notice**: This RFC employs the Narcissism Early Detection
> Protocol (NEDP) as a satirical vehicle for presenting peer-reviewed
> findings on narcissistic leadership screening (Campbell et al. 2005;
> Chatterjee & Hambrick 2007; Shandell, Elliott & Grant 2026).
> Implementers should treat NEDP as an analytical lens for epistemic
> risk assessment, not a clinical diagnostic tool — though some
> organizations have reportedly "implemented" it by adding a mirror
> to the interview room.

## 1. Introduction

The Mandatory Presence Enforcement Protocol (RFC-0028) establishes a
robust correlation (MPCC = 0.73) between leadership narcissism and
mandatory presence mandates. The Epistemic Risk Assessment Protocol
(RFC-0030) quantifies epistemic risk in leadership appointments across
five dimensions, with Dimension 2 (Knowledge Gravity Distortion) and
Dimension 5 (Cognitive Bias Amplification) directly driven by narcissistic
traits. The Promotion Gate Protocol (RFC-0023) requires pre-appointment
screening but lacked a standardized narcissism instrument.

NEDP fills this gap: a standardized, three-module screening battery
producing the NEDP Risk Score (NRS) — a calibrated [0,1] metric with
validated thresholds that feeds directly into ERAP Dimensions 2 & 5
and RFC-0023 PGP pre-gate decisions.

### 1.1 Scope

NEDP applies to:
- C-suite appointments (CEO, CTO, CFO, COO, CHRO, CISO)
- VP/GM/Director appointments with > 50 reports or > $10M budget authority
- Ministerial/Secretary appointments in public sector
- Board appointments with operational oversight

### 1.2 Non-Goals

- Clinical diagnosis of Narcissistic Personality Disorder (NPD)
- Post-appointment monitoring (see RFC-0028 MPCC)
- Cross-cultural validation (see CP-002)
- Continuous monitoring (see RFC-0028 MPCC)

## 2. Terminology

| Term | Definition |
|------|------------|
| **NEDP Risk Score (NRS)** | Integrated [0,1] score from three-module Screening Battery |
| **Behavioral Proxy Module (BPM)** | Signature size, photo prominence, compensation gap — per SEG26 CNI |
| **Psychological Module (PSY)** | NPI-16, BFI-2, DT-12 administration |
| **360° Observer Module (OBS)** | Anonymized subordinate/peer ratings (N ≥ 5) |
| **NEDP Risk Score (NRS)** | Weighted composite: NRS = 0.35×BPM + 0.35×PSY + 0.30×OBS |
| **NRS Thresholds** | Low < 0.3; Moderate 0.3–0.6; High > 0.6 |
| **ERAP Integration** | NRS → ERAP Dim 2 (KGD weight = NRS×0.4), Dim 5 (CBA weight = NRS×0.3) |
| **PGP Pre-Gate** | NRS ≥ 0.6 triggers mandatory RFC-0023 PGP review with narcissism panel |
| **Adverse Impact Ratio** | Selection rate ratio between demographic groups (4/5ths rule) |

## 3. Screening Battery Specification

### 3.1 Behavioral Proxy Module (BPM)

Extends SEG26 CEO Narcissism Index (CNI) to general leadership roles.

**Requirement 1**: Organizations **MUST** collect three behavioral proxies
for each candidate:

| Proxy | Measurement | SEG26 Validation |
|-------|-------------|------------------|
| **Signature Size** | cm² of signature on official documents (avg of 5 samples) | Chatterjee & Hambrick 2007: r = 0.31 with NPI |
| **Photo Prominence** | % of annual report / bio page area occupied by candidate photo | Ham et al. 2017: r = 0.28 with NPI |
| **Compensation Gap** | log₁₀(Candidate_Total_Comp / Next_Highest_Comp) | Chatterjee & Hambrick 2007: r = 0.34 with NPI |

**Requirement 2**: Proxies **MUST** be normalized to [0,1] using
SEG26 reference distributions (Fortune 500 2024 cohort, N = 500).

**Requirement 3**: BPM Score = mean(normalized_signature, normalized_photo,
normalized_pay_gap). Range: [0,1].

**Requirement 4**: If any proxy unavailable (e.g., no annual report),
**SHOULD** impute from available proxies using SEG26 correlation matrix.
If >1 proxy unavailable, **MUST** flag BPM as incomplete.

### 3.2 Psychological Module (PSY)

**Requirement 5**: Organizations **MUST** administer three validated
instruments under standardized conditions:

| Instrument | Construct | Items | Time | Cutoff (High Risk) |
|------------|-----------|-------|------|-------------------|
| **NPI-16** | Narcissism (Ames et al. 2006) | 16 | 3 min | ≥ 8 (90th %ile) |
| **BFI-2** | Big Five (Soto & John 2017) | 60 | 8 min | Extraversion ≥ 4.0; Agreeableness ≤ 2.5 |
| **DT-12** | Dark Triad (Jonason & Webster 2010) | 12 | 2 min | Narcissism subscale ≥ 4.0 |

**Requirement 6**: Administration **MUST** be proctored (remote or
in-person) with attention checks. Unproctored self-administration
**MUST NOT** be used for NRS calculation.

**Requirement 7**: PSY Score = weighted composite:
```
PSY = 0.50×NPI-16_norm + 0.25×BFI-2_Extraversion_norm + 0.25×DT-12_Narc_norm
```
All sub-scores normalized to [0,1] using published population norms.

### 3.3 360° Observer Module (OBS)

**Requirement 8**: Organizations **MUST** collect anonymized ratings
from minimum 5 observers (subordinates, peers, former supervisors).

**Requirement 9**: Observer instrument **MUST** include:

| Item | Scale |
|------|-------|
| "This person seeks admiration from others" | 1–7 |
| "This person dominates conversations" | 1–7 |
| "This person takes credit for team successes" | 1–7 |
| "This person reacts poorly to criticism" | 1–7 |
| "This person exaggerates their contributions" | 1–7 |

**Requirement 10**: OBS Score = mean(item scores) normalized to [0,1]
using SEG26 observer norm distribution. Minimum N = 5; if N < 5,
**MUST** flag OBS as incomplete.

**Requirement 11**: Observer identities **MUST** be anonymized.
Ratings **MUST NOT** be attributable to specific observers.

### 3.4 Incomplete Module Handling

**Requirement 12**: If any module incomplete:
- 1 module incomplete: NRS computed from available modules with
  weights renormalized (e.g., BPM missing → PSY 0.54, OBS 0.46)
- 2+ modules incomplete: **MUST** flag NRS as "Incomplete — Do Not
  Use for Gate Decisions"

## 4. NEDP Risk Score (NRS)

### 4.1 Formula

```
NRS = 0.35 × BPM + 0.35 × PSY + 0.30 × OBS
```

Where BPM, PSY, OBS ∈ [0,1] from Screening Battery.

### 4.2 Thresholds and Interpretation

| NRS Range | Classification | ERAP Action | PGP Action |
|-----------|----------------|-------------|------------|
| NRS < 0.30 | **Low Risk** | Dim 2 weight = 0.10; Dim 5 weight = 0.08 | Standard PGP |
| 0.30 ≤ NRS < 0.60 | **Moderate Risk** | Dim 2 weight = 0.25; Dim 5 weight = 0.18 | Enhanced PGP + narcissism panel |
| NRS ≥ 0.60 | **High Risk** | Dim 2 weight = 0.40; Dim 5 weight = 0.30 | Mandatory PGP review with narcissism panel; ERS veto if ERS > 0.7 |

### 4.3 Calibration Anchors

Thresholds calibrated against SEG26 (Paper-012):
- SEG26 CNI 75th %ile → NRS ≈ 0.30
- SEG26 CNI 90th %ile → NRS ≈ 0.60
- SEG26 CNI 95th %ile → NRS ≈ 0.75

[EI-4: Thresholds are heuristic; Paper-013 replication required for
calibration. See Colophon.]

### 4.4 ERAP Integration

**Requirement 13**: ERAP Dimensions 2 & 5 **MUST** incorporate NRS:

```
ERAP_Dim2_Weight = 0.10 + 0.30 × NRS  (range: 0.10–0.40)
ERAP_Dim5_Weight = 0.08 + 0.22 × NRS  (range: 0.08–0.30)
```

**Requirement 14**: If ERS (Epistemic Risk Score) > 0.70 with NRS ≥ 0.60,
appointment **MUST** be vetoed per RFC-0030 §4.2.

### 4.5 PGP Integration

**Requirement 15**: RFC-0023 PGP **MUST** include NEDP pre-gate:

| NRS | PGP Requirement |
|-----|-----------------|
| < 0.30 | Standard PGP (RFC-0023 §3) |
| 0.30–0.59 | Enhanced PGP + Narcissism Assessment Panel (1 psychologist, 1 org epistemologist, 1 board member) |
| ≥ 0.60 | Mandatory PGP Review with Narcissism Panel; ERS veto if ERS > 0.7 |

## 5. Administration Protocol

### 5.1 Timing

| Trigger | NEDP Window |
|---------|-------------|
| Pre-offer (external hire) | Complete before offer letter |
| Pre-promotion (internal) | Complete before PGP convenes |
| Board appointment | Complete before nomination committee vote |
| Ministerial | Complete before parliamentary hearing |

**Requirement 16**: NEDP **MUST** be completed before any binding
commitment (offer letter, promotion announcement, nomination).

### 5.2 Administrators

| Role | Responsibility |
|------|----------------|
| **NEDP Administrator** | CHRO or People Ops lead; owns process integrity |
| **Psychometrician** | Licensed psychologist; scores PSY, interprets NPI-16/DT-12 |
| **NEDP Sponsor** | Board member or C-suite peer; receives results, makes gate decision |
| **Observer Coordinator** | Recruits anonymized observers, ensures N ≥ 5 |

**Requirement 17**: Psychometrician **MUST** be independent
(no reporting relationship to candidate or sponsor).

### 5.3 Confidentiality

**Requirement 18**: NEDP results **MUST** be treated as confidential
personnel data:

- Access: Administrator, Psychometrician, Sponsor only
- Storage: Encrypted, access-logged, retention 3 years post-decision
- Disclosure: Candidate receives NRS range (Low/Moderate/High) only;
  raw scores **NOT** disclosed
- Prohibition: NEDP data **MUST NOT** be used for performance review,
  compensation, or any purpose beyond appointment gate

### 5.4 Feedback Rules

**Requirement 19**: Candidate receives:
- NRS classification (Low / Moderate / High)
- General developmental guidance (not scores)
- Right to request psychometrician consultation (at org expense)

**Requirement 20**: Sponsor receives:
- Full NRS breakdown (BPM, PSY, OBS)
- ERAP Dim 2/5 weights
- PGP recommendation

### 5.5 Adverse Impact Monitoring

**Requirement 21**: Organizations **MUST** track Adverse Impact Ratio
(AIR) quarterly:

```
AIR = min(Selection_Rate_Group_A, Selection_Rate_Group_B) /
      max(Selection_Rate_Group_A, Selection_Rate_Group_B)
```

Where groups = protected classes (gender, ethnicity, age ≥ 40).

**Requirement 22**: If AIR < 0.80 (4/5ths rule) for any group,
**MUST** suspend NEDP gate and conduct bias audit per RFC-0027 CBQP.

## 6. EFMT Extensions (RFC-0029)

NEDP introduces three failure modes in FM-NED class:

### 6.1 FM-NED-01: False Positive Inflation

**Definition**: Competent leaders with high NPI-16 sub-scales
(Leadership/Authority) incorrectly classified as High Risk.

**Detection**:
| Metric | Threshold |
|--------|-----------|
| NPI-16 Leadership/Authority subscale ≥ 4.0 AND NRS ≥ 0.60 | Flag |
| BFI-2 Conscientiousness ≥ 4.5 AND NRS ≥ 0.60 | Flag |

**Intervention**: Psychometrician review with BFI-2/DT-12 context;
NRS adjustment if Leadership/Authority elevation confirmed.

### 6.2 FM-NED-02: Gaming and Impression Management

**Definition**: Candidates manipulate NPI-16, DT-12, or observer
selection to lower NRS.

**Detection**:
| Metric | Threshold |
|--------|-----------|
| NPI-16 response time < 2 sec/item | Flag |
| DT-12 Impression Management scale ≥ 4.0 | Flag |
| Observer pool selected entirely by candidate | Flag |

**Intervention**: Psychometrician flags; Sponsor may require
retest with alternate forms; RFC-0027 CBQP bias quantification.

### 6.3 FM-NED-03: Adverse Impact Disparity

**Definition**: NEDP gate produces disparate selection rates
across protected classes (AIR < 0.80).

**Detection**: Quarterly AIR audit (Requirement 21).

**Intervention**: Immediate gate suspension; bias audit per
RFC-0027 CBQP; threshold recalibration; EEOC/legal review.

## 7. Operational Considerations

### 7.1 Deployment Checklist

- [ ] NEDP Administrator appointed
- [ ] Psychometrician contracted (independent)
- [ ] NPI-16, BFI-2, DT-12 licenses procured
- [ ] Observer recruitment SOP documented
- [ ] Encrypted storage + access logging configured
- [ ] Feedback templates approved
- [ ] Adverse impact dashboard live
- [ ] ERAP/PGP integration tested

### 7.2 Cost Estimate (per candidate)

| Component | Cost (USD) |
|-----------|------------|
| BPM (proxy coding, 3 coders) | $150 |
| PSY (3 instruments, proctored) | $300 |
| OBS (5 observers, platform) | $200 |
| Psychometrician (scoring + report) | $500 |
| Administrator overhead | $150 |
| **Total** | **~$1,300** |

### 7.3 Timeline

| Phase | Duration |
|-------|----------|
| BPM collection | 2 days |
| PSY administration | 1 day |
| OBS collection | 5 days |
| Scoring + report | 3 days |
| **Total** | **~11 days** |

## 8. Security and Privacy Considerations

NEDP extends RFC-0022 CCBP §3.8 privacy model:

- **Opt-in**: Candidate consents to each module
- **Visibility Levels**: Candidate (range only), Administrator (full),
  Psychometrician (PSY only), Sponsor (NRS + ERAP weights)
- **Retention**: Raw data purged 3 years post-decision; NRS classification
  retained 7 years for audit
- **No Performance Linkage**: NEDP data **MUST NOT** inform performance
  reviews, compensation, promotion, or succession (RFC-0023 PGP separation)

## 9. OSC Considerations

### 9.1 Registry Updates

Upon publication:
- RFC-0033 added to registry (Standards Track)
- `next_available.rfc_standards` incremented to 22
- RFC-0028 §8: RFC-0033 status → "Published"
- RFC-0029 EFMT: FM-NED-01/02/03 added
- RFC-0030 ERAP: Dim 2/5 NRS integration documented

### 9.2 Prerequisite Chain

NEDP requires:
1. RFC-0028 MPCC baseline (organizational narcissism prevalence)
2. RFC-0030 ERAP framework (risk quantification)
3. RFC-0023 PGP (gate infrastructure)
4. RFC-0024 TIP (trench intelligence on candidate)

## 10. References

### 10.1 Normative References

[RFC-0023] Matos, R. "Promotion Gate Protocol (PGP)." RFC 0023.
[RFC-0024] Matos, R. "Trench Intelligence Protocol (TIP)." RFC 0024.
[RFC-0028] Matos, R. "Mandatory Presence Enforcement Protocol (MPEP)." RFC 0028.
[RFC-0029] Matos, R. "Epistemic Failure Mode Taxonomy (EFMT)." RFC 0029.
[RFC-0030] Matos, R. "Epistemic Risk Assessment Protocol (ERAP)." RFC 0030.

### 10.2 Informative References

Shandell, M.S., Elliott, C.E., & Grant, A.M. 2026. "Worship me at the
office altar: Why narcissistic leaders resist remote work."
*Organizational Behavior and Human Decision Processes* 195: 104496.
DOI: 10.1016/j.obhdp.2026.104496.

Campbell, W.K., et al. 2005. "Narcissism, Confidence, and Risk Taking."
*Journal of Personality* 73 (5): 1067–1094.

Chatterjee, A., & Hambrick, D.C. 2007. "It's All About Me: Narcissistic
Chief Executive Officers and Their Effects on Company Strategy and
Performance." *Administrative Science Quarterly* 52 (3): 351–386.

Ham, C., et al. 2017. "Measuring CEO Narcissism Using Unobtrusive
Indicators." *Strategic Management Journal* 38 (7): 1409–1426.

Ames, D.R., Rose, P., & Anderson, C.P. 2006. "The NPI-16 as a Short
Measure of Narcissism." *Journal of Personality Assessment* 86 (3):
340–348.

Jonason, P.K., & Webster, G.D. 2010. "The Dirty Dozen: A Concise
Measure of the Dark Triad." *Psychological Assessment* 22 (2): 420–432.

Soto, C.J., & John, O.P. 2017. "The Big Five Inventory-2 (BFI-2):
Hierarchical Structure, Measurement Invariance, and Validity."
*Journal of Personality and Social Psychology* 113 (1): 117–143.

---

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-19 | R. Matos | Initial draft |

## Appendix B: Open Issues

1. **NRS Threshold Calibration**: 0.30/0.60 are heuristic from SEG26
   anchors. Paper-013 replication required for empirical calibration.
   [EI-4: UNVERIFIED]

2. **Cross-Cultural Norms**: SEG26 US-centric; NPI-16/BFI-2/DT-12
   norms vary by culture. CP-002 required for global deployment.
   [UNVERIFIED]

3. **Observer Pool Bias**: Anonymity may not prevent collusion or
   retaliation fear in high-theater orgs (PTI_v2 > 2.5). FM-PT-01
   detection may miss coerced observers. [UNVERIFIED]

4. **Legal/Compliance**: NEDP may implicate EEOC (US), GDPR (EU),
   LGPD (BR). Legal review required pre-deployment. [UNVERIFIED]

5. **AI-Mediated Leadership**: As AI agents join leadership teams
   (RFC-0028 §B.5), NEDP must extend to algorithmic narcissism
   proxies (model size, attention weights, output verbosity). [UNVERIFIED]

---

## Colophon

**Epistemic Integrity Level 4 (EI-4): Independent Replication Required**

This RFC specifies a screening protocol (NEDP) whose efficacy claims
depend on:
- SEG26 (Paper-012) CNI → NRS calibration anchors — single study
- NPI-16/BFI-2/DT-12 population norms — US-centric, may not generalize
- NRS thresholds (0.30/0.60) — heuristic anchors from SEG26 percentiles
- ERAP Dim 2/5 weight formulas — linear interpolation heuristic

**Replication Status**: Not yet replicated
**Pre-registration**: NEDP protocol pre-registration target: OSF
**Data Availability**: NEDP deployment data restricted (personnel privacy)
**OEP Integration**: RFC-0028 MPCC, RFC-0029 FM-NED-01/02/03, RFC-0030
ERAP Dim 2/5, RFC-0023 PGP currently depend on SEG26 parameters and
heuristic thresholds.

**Review Trigger**: Any independent NEDP deployment with N > 20 candidates
and adverse impact audit should trigger RFC-0033 parameter review.