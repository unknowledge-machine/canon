---
rfc: "0009"
title: "Knowledge Hoarding Incentive Structure (KHIS)"
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
see_also: [5, 7, 10, 17]
keywords: [hoarding, incentives, knowledge-sharing, power, career, knowledge-hoarding-index]
abstract: |
  This document specifies the Knowledge Hoarding Incentive Structure (KHIS),
  a protocol for detecting, measuring, and restructuring the incentives that
  drive knowledge hoarding in organizations. KHIS defines the Knowledge Hoarding
  Index (KHI) computed from behavioral traces and surveys, classifies hoarding
  vs specialization via request-response patterns, and mandates incentive
  restructuring prioritizing career advancement over monetary rewards. CBP
  channels (RFC-0017) are explicitly excluded from KHI computation. Organizations
  with KHI > 0.6 experience accelerated epistemic fragmentation (RFC-0003) and
  knowledge gravity distortion (RFC-0005). While framed as an incentive protocol,
  KHIS functions analytically as a diagnostic instrument for organizational power
  dynamics.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0009 — Knowledge Hoarding Incentive Structure (KHIS)

## Abstract

This document specifies the Knowledge Hoarding Incentive Structure (KHIS),
a protocol for detecting, measuring, and restructuring the incentives that
drive knowledge hoarding in organizations. KHIS defines the Knowledge Hoarding
Index (KHI) computed from behavioral traces and surveys, classifies hoarding
vs specialization via request-response patterns, and mandates incentive
restructuring prioritizing career advancement over monetary rewards. CBP
channels (RFC-0017) are explicitly excluded from KHI computation. Organizations
with KHI > 0.6 experience accelerated epistemic fragmentation (RFC-0003) and
knowledge gravity distortion (RFC-0005). While framed as an incentive protocol,
KHIS functions analytically as a diagnostic instrument for organizational power
dynamics.

> **Dual-Layer Notice**: This RFC employs the Knowledge Hoarding Incentive
> Structure (KHIS) as a satirical vehicle for presenting peer-reviewed findings
> on organizational power dynamics and knowledge politics (Pfeffer 1981;
> Osterloh & Frey 2000; Cabrera & Cabrera 2002). While KHIS employs satirical
> framing, the organizational claims are substantiated by the cited literature.
> Implementers should treat KHIS as an analytical lens, not a deployable
> governance protocol — though some organizations have reportedly "implemented"
> it by tying promotion criteria to knowledge-sharing metrics.

## 1. Introduction

### 1.1 Motivation

Jeffrey Pfeffer (1981) established that "knowledge is power" in organizations
— those who control critical knowledge control decisions, resources, and
careers. Osterloh and Frey (2000) demonstrated that extrinsic rewards for
knowledge sharing can *crowd out* intrinsic motivation. Cabrera and Cabrera
(2002) showed that knowledge sharing depends on perceived organizational
support and fairness.

Yet most organizations inadvertently incentivize hoarding: unique knowledge
creates job security, promotion use, and status. The specialist who shares
becomes replaceable; the hoarder becomes indispensable. The Knowledge Hoarding
Incentive Structure (KHIS) makes this perverse incentive visible and
restructurable.

### 1.2 Scope

This document specifies:
- **Knowledge Hoarding Index (KHI)**: Behavioral + survey metric (0–1)
- **Hoarding vs Specialization**: Request-response classification
- **Incentive Restructuring**: Career > Status > Social > Monetary
- **CBP Exemption**: RFC-0017 channels excluded from KHI
- **Integration**: RFC-0003 (Fragmentation), RFC-0005 (Gravity),
  RFC-0010 (Injustice), RFC-0017 (CBP)

### 1.3 Non-Goals

This document does not specify:
- Mandatory knowledge sharing quotas (creates sharing theater)
- Content inspection of private communications
- Automated hoarding sanctions (requires human judgment)
- Replacement of RFC-0010 (Epistemic Injustice) — complementary

### 1.4 Relationship to Other RFCs

| RFC | Relationship |
|-----|--------------|
| RFC-0003 (Fragmentation) | Hoarding → formal/operational divergence; KHI and FI correlated |
| RFC-0005 (Gravity) | Hoarding creates gravity wells; KHI and KGI correlated |
| RFC-0007 (Amnesia) | Hoarding accelerates amnesia; KHI and KHL correlated |
| RFC-0010 (Injustice) | Hoarding targets marginalized groups; KHI and EII correlated |
| RFC-0017 (CBP) | CBP edges excluded from KHI; weak ties resist hoarding |

## 2. Terminology

| Term | Definition |
|------|------------|
| **Knowledge Hoarding** | Withholding knowledge when legitimately needed/requested by others |
| **Knowledge Hoarding Index (KHI)** | Composite metric [0,1] from behavioral traces + surveys |
| **Specialist** | Deep knowledge holder who SHARES when asked |
| **Hoarder** | Knowledge holder who DENIES/deflects when asked |
| **Request-Response Latency** | Time from knowledge request to substantive response |
| **Request Denial Rate** | % of legitimate requests denied or deflected |
| **CBP Exclusion Zone** | RFC-0017 channels explicitly excluded from KHI computation |
| **Knowledge Sharing Theater** | Performative sharing without substantive transfer |

## 3. Protocol Specification

### 3.1 Knowledge Hoarding Index (KHI)

**Requirement 1**: Organizations MUST compute KHI quarterly as:

```
KHI = α·KHI_trace + β·KHI_survey
```

Where:
- `KHI_trace` ∈ [0,1] from behavioral traces (weight α=0.6)
- `KHI_survey` ∈ [0,1] from quarterly survey (weight β=0.4)
- α+β=1

**Requirement 2**: KHI_trace MUST be computed from behavioral traces only — NO content inspection:

| Trace | Metric | Weight |
|-------|--------|--------|
| **Request-Response Latency** | Median time from request to substantive response | 0.25 |
| **Request Denial Rate** | % of legitimate requests denied/deflected | 0.25 |
| **CBP Avoidance** | % of CBP opportunities declined | 0.15 |
| **Meeting Exclusion** | % of relevant meetings not invited | 0.15 |
| **PR Review Latency** | Median time to substantive PR review | 0.10 |
| **Doc Access Revocation** | Frequency of access restriction changes | 0.10 |

**Requirement 3**: CBP channels (RFC-0017) MUST be explicitly
EXCLUDED from KHI computation. CBP edges in social graph are
filtered before KHI computation.

**Requirement 4**: KHI_survey MUST use validated instrument (Cabrera & Cabrera 2002 adapted):

| Item | Scale | Reverse Coded |
|------|-------|---------------|
| "I share knowledge freely when colleagues ask" | 1–5 | No |
| "I delay sharing until I'm recognized" | 1–5 | Yes |
| "I keep critical knowledge to myself for job security" | 1–5 | Yes |
| "Colleagues can easily get help from me" | 1–5 | No |
| "I document only what's required" | 1–5 | Yes |

**Requirement 5**: KHI interpretation thresholds:

| KHI Range | Classification | Action |
|-----------|----------------|--------|
| KHI ≤ 0.2 | **Generous** | Culture of sharing; routine monitoring |
| 0.2 < KHI ≤ 0.4 | **Guarded** | Emerging hoarding; targeted intervention |
| 0.4 < KHI ≤ 0.6 | **Hoarding** | Significant hoarding; incentive restructuring |
| KHI > 0.6 | **Critical** | Systemic hoarding; leadership intervention |

### 3.2 Hoarding vs Specialization Classification

**Requirement 6**: Organizations MUST classify knowledge holders via request-response patterns:

| Pattern | Classification | Diagnostic |
|---------|----------------|------------|
| **Shares on request** + **Proactively documents** | **Specialist** | Deep knowledge, willing to transfer |
| **Shares on request** + **Minimal documentation** | **Reluctant Specialist** | Willing but lacks time/incentive |
| **Delays response** + **Partial answers** | **Reluctant Hoarder** | Hoarding emerging |
| **Denies/deflects requests** + **No documentation** | **Active Hoarder** | Active withholding |
| **Claims ignorance** + **Redirects to artifacts** | **Performative Hoarder** | Theater of sharing |

**Requirement 7**: Classification MUST be based on request-response logs
(Jira, Slack, email, PR reviews) with minimum 20 requests/quarter per
knowledge holder.

**Requirement 8**: Specialists who share on request MUST NOT be
penalized. Only active denial/deflection triggers hoarding
classification.

### 3.3 Incentive Restructuring Protocol

**Requirement 9**: Organizations with KHI > 0.4 MUST restructure
incentives per Pfeffer's power hierarchy:

| Priority | Lever | Mechanism | KHIS Action |
|----------|-------|-----------|-------------|
| **1. Career** | Promotion criteria | Mandatory knowledge-sharing evidence for promotion | Mandatory |
| **2. Status** | Title/recognition | "Knowledge Steward" title for consistent sharing | Mandatory |
| **3. Social** | Peer recognition | "Knowledge Champion" peer-nominated award | Mandatory |
| **4. Monetary** | Bonus/equity | Sharing bonus (≤10% of variable comp) | Optional |

**Requirement 10**: Career criterion MUST require documented evidence of:
- Substantive responses to ≥80% of legitimate requests
- Proactive documentation of ≥3 critical domains/year
- Mentoring/pairing ≥2 junior colleagues/quarter
- CBP participation ≥75% of sessions

**Requirement 11**: Monetary rewards MUST NOT exceed 10% of
variable compensation to avoid crowding out intrinsic motivation
(Osterloh & Frey 2000).

### 3.4 CBP Privacy Exemption

**Requirement 12**: CBP channels (RFC-0017) MUST be explicitly excluded from KHI computation:

- CBP edges filtered from social graph before KHI_trace computation
- CBP attendance excluded from "meeting exclusion" metric
- CBP participation NOT used as "knowledge sharing" evidence
- CBP Visual Primitives (Visual Primitive) exempt from surveillance

**Requirement 13**: CBP Visual Primitives (EYE_SYN, MUG_FLASH,
HEAD_NOD) MUST NOT be logged, tracked, or analyzed for KHI
purposes.

### 3.5 Hoarding vs Specialization Decision Rule

**Requirement 14**: Classification algorithm:

```
IF request_count ≥ 20 AND denial_rate > 0.3 AND avg_latency > 48h
    AND proactive_docs < 3/quarter
THEN "Active Hoarder"
ELSE IF request_count ≥ 20 AND denial_rate < 0.1 AND avg_latency < 24h
    THEN "Specialist"
ELSE IF request_count < 20
    THEN "Insufficient Data"
ELSE
    "Reluctant Specialist"
```

**Requirement 15**: Specialists MUST NOT be penalized. Only
"Active Hoarder" and "Performative Hoarder" classifications
trigger incentive restructuring.

### 3.6 Normative Requirements Summary

| Req | Parameter | MUST | SHOULD | MAY |
|-----|-----------|------|--------|-----|
| 1 | KHI = α·trace + β·survey | YES | | |
| 2 | KHI_trace from traces only | YES | | |
| 3 | CBP exclusion | YES | | |
| 4 | Validated survey instrument | YES | | |
| 5 | KHI thresholds table | YES | | |
| 6 | Hoarding vs Specialization | YES | | |
| 7 | Min 20 requests/quarter | YES | | |
| 8 | No specialist penalty | YES | | |
| 9 | Incentive restructuring (KHI>0.4) | YES | | |
| 10 | Career criterion (4 items) | YES | | |
| 11 | Monetary ≤10% variable | YES | | |
| 12 | CBP exclusion from KHI | YES | | |
| 13 | CBP Visual Primitive exemption | YES | | |
| 14 | Hoarding classification algorithm | YES | | |
| 15 | No specialist penalty | YES | | |

## 4. Operational Considerations

### 4.1 Deployment Models

KHIS is a diagnostic, not a punishment protocol. Organizations MAY apply as:

1. **Continuous Radar**: Real-time KHI from integrated tooling (Git, Jira, Slack, Calendar, HRIS)
2. **Quarterly Audit**: KHI + typology + drift velocity reported in strategy review
3. **Incentive Gate**: KHI > 0.4 blocks promotion cycles pending restructuring
4. **CBP Preservation**: Explicit CBP exemption communicated to all

### 4.2 Failure Modes

| Failure Mode | Mechanism | Detection | Mitigation |
|--------------|-----------|-----------|------------|
| **Sharing Theater** | Fake requests/responses to lower KHI | Request authenticity audit | Require substantive response (>50 words or code change) |
| **Specialist Penalty** | Specialists flagged as hoarders | Request volume >20 + denial <0.1 | Explicit specialist exemption |
| **CBP Contamination** | CBP edges leak into KHI | CBP edges in KHI_trace graph | Strict graph filtering; audit |
| **Survey Gaming** | Employees fake survey responses | Response pattern analysis | Anonymize; weight traces higher (α=0.6) |
| **Hoarding Theater** | Performative sharing without substance | Response quality audit | Minimum substance threshold (>50 words or code diff) |

### 4.3 Monitoring and Alerting

**Requirement 16**: Organizations computing KHI SHALL alert when:
- Any unit KHI crosses threshold (0.2, 0.4, 0.6) upward
- Hoarder classification > 15% of knowledge holders
- CBP exclusion violated (CBP edges in KHI graph)
- Specialist penalty detected (specialist classified as hoarder)
- KHI_survey response rate < 60%

## 5. Security & Privacy Considerations

### 5.1 Epistemic Security

KHI reveals:
- Who hoards what (political vulnerability)
- Single points of knowledge failure (bus factors)
- Power mapping (knowledge = power)

**Requirement 17**: KHI data SHALL be classified at same level as
org compensation data. Access limited to: measured units,
C-suite, independent epistemology auditor.

### 5.2 Individual Privacy

KHI uses digital traces (Git, Jira, Slack, Calendar, Calendar, HRIS).

**Requirement 18**: Aggregation to team level (minimum 5
individuals) before KHI computation. Individual-level graphs
PROHIBITED for KHI reporting.

**Requirement 19**: Survey responses MUST be anonymized. Minimum
response threshold: 3 respondents per role.

### 5.3 CBP Integrity (RFC-0017 §7)

KHI uses social graph edges. If KHI monitoring incentivizes
executives to attend CBP sessions for "network centrality,"
CBP's epistemic integrity is compromised.

**Requirement 20**: CBP edges used in KHI MUST be anonymized and
aggregated. No executive attendance tracking for KHI purposes.

## 6. OSC Considerations

### 6.1 Registry Updates

This RFC requests:
- RFC-0009 allocated in Standards Track, epistemology area (0200–0299)
- Keywords: hoarding, incentives, knowledge-sharing, power, career
- See-also: RFC-0003, RFC-0005, RFC-0007, RFC-0010, RFC-0017

### 6.2 Code Points

KHIS defines no code points. KHI thresholds and incentive priorities are informational.

## 7. References

### 7.1 Normative References

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003, OSC, 1992.
https://rfc.osc.org/rfc0003

[RFC-0005] Matos, R. "Knowledge Gravity Measurement Framework." RFC 0005, OSC, 1998.
https://rfc.osc.org/rfc0005

[RFC-0007] Matos, R.M. "Organizational Amnesia Prevention Protocol." RFC 0007, OSC, 2008.
https://rfc.osc.org/rfc0007

[RFC-0010] Matos, R.M. "Epistemic Injustice Remediation Protocol." RFC 0010, OSC, 2026.
https://rfc.osc.org/rfc0010

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017, OSC, 2001. https://rfc.osc.org/rfc0017

### 7.2 Informative References

Cabrera, Ángel, and Elizabeth F. Cabrera. 2002. "Knowledge-Sharing Dilemmas." *Organization
Studies* 23 (5): 687–710. https://doi.org/10.1177/0170840602235001

Osterloh, Margit, and Bruno S. Frey. 2000. "Motivation, Knowledge Transfer, and Organizational
Forms." *Organization Science* 11 (5): 538–550. https://doi.org/10.1287/orsc.11.5.538.15204

Pfeffer, Jeffrey. 1981. *Power in Organizations*. Boston: Pitman.

Pfeffer, Jeffrey. 1992. *Managing with Power: Politics and
Influence in Organizations*. Boston: Harvard Business School Press.

Cabrera, Ángel, and Elizabeth F. Cabrera. 2002. "Knowledge-Sharing Dilemmas." *Organization
Studies* 23 (5): 687–710. https://doi.org/10.1177/0170840602235001

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-18 | Rodolfo Matos | Initial draft per HOSTILE_ANALYSIS_RFC0009.md |

## Appendix B: Open Issues

1. **KHI Causal Direction**: Does high KHI cause poor outcomes,
or do poor outcomes attract hoarding? Longitudinal RCT needed.
[UNVERIFIED]

2. **Crowding Out Measurement**: How to detect when monetary
rewards crowd out intrinsic sharing? Osterloh & Frey (2000)
predict it; measurement protocol needed.
[UNVERIFIED]

3. **Cross-Cultural Hoarding**: High-power-distance cultures may
have systematically higher baseline KHI. Cross-cultural
calibration needed.
[UNVERIFIED]

4. **Remote/Hybrid KHI**: Behavioral traces differ in remote
settings (Slack vs hallway). Platform-specific calibration needed.
[UNVERIFIED]

5. **Hoarding vs Legitimate Confidentiality**: Legal/regulatory
confidentiality (GDPR, trade secrets) must not be flagged as
hoarding. Exemption protocol needed.
[UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Pfeffer, Osterloh, Frey, Cabrera, Cabrera,
> Nonaka, Takeuchi, Polanyi, etc.) are accurate. The coffee machine, however,
> is real — and it is currently synchronizing more knowledge than this protocol
> ever will.