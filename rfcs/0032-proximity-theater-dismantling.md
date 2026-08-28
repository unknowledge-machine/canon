---
rfc: "0032"
title: "Proximity Theater Dismantling Protocol (PTDP)"
stream: "Humor"
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
see_also: [17, 22, 24, 28, 29, 31]
keywords:
  - proximity-theater
  - dismantling
  - mandatory-presence
  - intentional-coordination
  - coordination-contracts
  - organizational-theater
abstract: |
  This document specifies the Proximity Theater Dismantling Protocol (PTDP),
  a systematic protocol for identifying, measuring, and eliminating mandatory
  presence mandates that serve narcissistic supply (proximity theater) while
  preserving genuine coordination needs. PTDP introduces PTI v2.0 with an
  outcome-correlated denominator, the Coordination Contract Registry (CCR) for
  explicit synchronization needs, and a four-phase dismantling protocol:
  Audit → Exposure → Substitution → Elimination. The Genuine Collaboration
  Preservation mechanism ensures remote-first defaults with CCR-gated office
  access. NSST Level 1 (RFC-0031) is a prerequisite for the Exposure phase.
dual_layer: true
satire_notice: "satire"
---

# RFC-0032 — Proximity Theater Dismantling Protocol (PTDP)

## Abstract

This document specifies the Proximity Theater Dismantling Protocol (PTDP),
a systematic protocol for identifying, measuring, and eliminating mandatory
presence mandates that serve narcissistic supply (proximity theater) while
preserving genuine coordination needs. PTDP introduces PTI v2.0 with an
outcome-correlated denominator, the Coordination Contract Registry (CCR) for
explicit synchronization needs, and a four-phase dismantling protocol:
Audit → Exposure → Substitution → Elimination. The Genuine Collaboration
Preservation mechanism ensures remote-first defaults with CCR-gated office
access. NSST Level 1 (RFC-0031) is a prerequisite for the Exposure phase.

> **Satire Notice**: This document is published in the **Humor** stream.
> While technically coherent, its primary purpose is satirical illumination
> of organizational dynamics. The OSC does not recommend deploying PTDP
> without board sponsorship, a qualified organizational epistemologist,
> and a very large mirror.

## 1. Introduction

The Mandatory Presence Enforcement Protocol (RFC-0028) establishes that
mandatory presence policies correlate strongly with leadership narcissism
(MPCC = 0.73). The Presence Theater Index (PTI) quantifies the gap between
mandated and productivity-justified office attendance: organizations with
MPCC > 0.6 exhibit median PTI = 3.2 — over three days of theater per
justified day.

RFC-0029 classifies this as FM-NP-01 (Narcissistic Proximity Control):
mandates driven by leader's supply need, not productivity. FM-NP-02
(Supply Disruption Retaliation) warns that remote work adoption triggers
punitive presence mandates. FM-NP-03 (Mirror-Gazing Escalation) tracks
leader time shifting from value-adding to visibility-seeking.

PTDP addresses the root cause: **implicit presence defaults**. When
"office = work" is the unexamined assumption, theater thrives. PTDP makes
coordination intentional — replacing presence mandates with explicit
coordination contracts.

## 2. Terminology

| Term | Definition |
|------|------------|
| **Proximity Theater** | Mandated physical presence serving narcissistic supply rather than productivity |
| **PTI v2.0** | Presence Theater Index with outcome-correlated denominator |
| **Coordination Contract Registry (CCR)** | Team-owned registry of explicit synchronization needs |
| **Genuine Collaboration** | Coordination with measurable outcome correlation |
| **Outcome Correlation** | Correlation between daily office presence and decision/artifact/handoff events |
| **NSST L1 Gate** | Prerequisite: RFC-0031 Level 1 (Nudges) active before PTDP Exposure phase |
| **PTDP Sponsor** | CTO/Board member authorizing Exposure and approving CCR entries |

## 3. PTI v2.0 — Outcome-Correlated Theater Index

### 3.1 Definition

PTI v2.0 replaces the RFC-0028 denominator (productivity-justified days,
often estimated) with an empirically measurable outcome correlation:

```
PTI_v2 = Mandated_Office_Days / max(1, Days_With_Outcome_Correlation)
```

Where **Days_With_Outcome_Correlation** = count of days in measurement
window where:

```
Correlation(Office_Presence_t, Outcome_Events_t) > 0.5
```

And **Outcome_Events** = sum of:
- Decision artifacts produced (RFC-0014 DTS outputs)
- Artifact handoffs completed (design→dev, dev→QA, etc.)
- CCR-registered sync events executed
- Decision gates passed (RFC-0004 DTS milestones)

### 3.2 Interpretation

| PTI_v2 Range | Classification | Action |
|--------------|----------------|--------|
| PTI_v2 ≤ 1.0 | **Justified** | Mandates correlate with outcomes |
| 1.0 < PTI_v2 ≤ 1.5 | **Moderate Theater** | NSST L1 + CCR audit |
| 1.5 < PTI_v2 ≤ 2.5 | **Heavy Theater** | NSST L1 + PTDP Audit phase |
| PTI_v2 > 2.5 | **Pure Theater** | Full PTDP protocol required |

### 3.3 Measurement Protocol

**Requirement 1**: Organizations **MUST** measure PTI_v2 monthly using
automated data sources (badge swipes, calendar API, artifact repository
events, CCR entries). Manual estimation **MUST NOT** be used.

**Requirement 2**: Outcome events **MUST** be timestamped and attributed
to specific coordination contracts (CCR entries) to prevent metric gaming.

**Requirement 3**: Measurement window **SHOULD** be 30 days minimum; 90
days for baseline establishment.

## 4. Coordination Contract Registry (CCR)

### 4.1 Purpose

The CCR replaces implicit "office = coordination" assumptions with
explicit, auditable synchronization contracts. Every mandated office day
must map to a CCR entry; every CCR entry must specify a remote alternative.

### 4.2 Contract Schema

Each CCR entry **MUST** contain:

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `contract_id` | UUID | YES | Unique identifier |
| `team` | string | YES | Owning team identifier |
| `sync_type` | enum | YES | `decision_gate`, `artifact_handoff`, `design_review`, `incident_response`, `relationship_building` |
| `cadence` | ISO8601 duration | YES | e.g., `P1W`, `P2D`, `PT4H` |
| `artifact_in` | array[string] | NO | Input artifacts (specs, designs, data) |
| `artifact_out` | array[string] | NO | Output artifacts (decisions, code, docs) |
| `decision_gate` | string | NO | RFC-0004 DTS gate identifier |
| `remote_alternative` | string | YES | How this sync works remotely (async doc, video call, RFC-0017 CBP) |
| `outcome_metric` | string | YES | How success is measured (decision count, handoff latency, defect rate) |
| `ttl` | ISO8601 duration | YES | Time-to-live (default `P90D`, max `P180D`) |
| `sponsor_approval` | boolean | YES | PTDP Sponsor sign-off |

### 4.3 Governance

**Requirement 4**: CCR entries **MUST** be team-proposed,
sponsor-approved. Teams **MAY** propose contracts; sponsors **MUST**
verify remote alternative adequacy.

**Requirement 5**: CCR entries **MUST** expire at TTL. Renewal requires
outcome metric evidence (correlation > 0.5).

**Requirement 6**: CCR **MUST** be public within organization.
Transparency prevents theater migration to hidden channels.

### 4.4 CCR Gap Analysis

**Requirement 7**: Audit phase **MUST** compute CCR Coverage Ratio:

```
CCR_Coverage = CCR_Registered_Sync_Events / Total_Sync_Events_Observed
```

Where Total_Sync_Events_Observed = all meetings, handoffs, reviews
detected via calendar/artifact analysis.

CCR_Coverage < 0.7 triggers mandatory CCR population before Substitution.

## 5. Four-Phase Dismantling Protocol

### 5.1 State Machine

```ascii
AUDIT
  |
  v
PTI_v2 Measurement + CCR Gap Analysis
  |
  v
EXPOSURE (NSST L1 Gate)
  |
  v
Private Metrics Briefing → Sponsor
  |
  v
SUBSTITUTION
  |
  v
CCR Population + Mandate Removal
  |
  v
ELIMINATION
  |
  v
Remote-First Default + CCR-Gated Office Access
```

### 5.2 Phase Definitions

#### Phase 1: Audit

**Entry Condition**: PTI_v2 > 1.0 OR CCR_Coverage < 0.7

**Activities**:
- Measure PTI_v2 for 90-day baseline
- Analyze CCR gap (CCR_Coverage ratio)
- Identify all active presence mandates
- Map mandates to CCR entries (or gaps)
- Classify each mandate: Theater / Justified / Unknown

**Exit Condition**: Baseline PTI_v2 + CCR Gap Report delivered to Sponsor

**Requirement 8**: Audit **MUST** use lagging indicators (outcome
correlation) not leading indicators (activity, badge swipes, camera-on %).

#### Phase 2: Exposure

**Entry Condition**: Audit complete + **NSST Level 1 Active** (RFC-0031
§6 — VPA opt-in, DSA badges, AAR Tier 3 deployed)

**Activities**:
- Private briefing to PTDP Sponsor (CTO/Board)
- Metrics: PTI_v2, CCR_Coverage, Mandate Inventory, FM-NP detection
- No public disclosure; no leader attribution in briefing
- Sponsor authorizes Substitution phase

**Exit Condition**: Sponsor sign-off on Substitution plan

**Requirement 9**: Exposure briefing **MUST NOT** be shared with
mandate-originating leaders. NSST L1 supplies alternative supply
channels to prevent FM-NP-02 retaliation.

#### Phase 3: Substitution

**Entry Condition**: Sponsor authorization

**Activities**:
- Populate CCR for all Justified mandates (outcome correlation > 0.5)
- Remove Theater mandates (no CCR entry, no outcome correlation)
- For Unknown mandates: 30-day observation with outcome tracking
- Deploy Remote-First Default: no office mandate without CCR entry
- NSST L1 mechanisms active (VPA, DSA, AAR-T3) for supply continuity

**Exit Condition**: All mandates either CCR-registered or removed

**Requirement 10**: Mandate removal **MUST** be gradual — one mandate
per team per sprint maximum, to allow CCR adaptation.

#### Phase 4: Elimination

**Entry Condition**: All mandates CCR-registered or removed; PTI_v2 ≤
1.5 sustained 60 days

**Activities**:
- Enforce Remote-First Default: office access only via CCR entry
- CCR entries expire at TTL (90-day default); renewal requires outcome
evidence
- Continuous PTI_v2 monitoring with Sponsor alerts at PTI_v2 > 1.5
- Integrate with RFC-0028 MPCC monitoring for regression detection

**Exit Condition**: Sustained PTI_v2 ≤ 1.0 for 180 days

**Requirement 11**: Elimination **MUST NOT** be declared while any FM-
NP or FM-PT failure mode is active (RFC-0029 detection thresholds).

## 6. Genuine Collaboration Preservation

### 6.1 Remote-First Default

**Requirement 12**: Organizations **MUST** adopt Remote-First Default:
physical presence is opt-in via CCR, not opt-out via mandate.

### 6.2 CCR-Gated Office Access

**Requirement 13**: Office access **MAY** be granted for:
- CCR-registered sync events (with outcome evidence)
- Hardware/lab access (registered in CCR as `artifact_in: [lab_equipment]`)
- Legal/compliance requirements (documented, time-bounded)
- Voluntary individual preference (no mandate, no CCR entry needed)

**Requirement 14**: Office access **MUST NOT** be granted for:
- "Culture building" without CCR entry
- "Serendipity" without outcome correlation evidence
- Leader preference without CCR entry

### 6.3 Preservation Monitoring

**Requirement 15**: PTDP Sponsor **MUST** monitor:
- CCR_Coverage (target > 0.8)
- Outcome correlation for CCR entries (target > 0.5)
- Team velocity / decision latency (no degradation vs. baseline)
- FM-NP / FM-PT detection (RFC-0029 thresholds)

## 7. EFMT Extensions (RFC-0029)

PTDP introduces two new failure modes in the FM-PT (Proximity Theater) class:

### 7.1 FM-PT-01: Theater Metrics Gaming

**Definition**: Leaders mandate "collaboration hours," "focus days," or
"innovation sprints" that are performative theater disguised as PTDP
compliance.

**Detection Metrics**:
| Metric | Threshold | Source |
|--------|-----------|--------|
| CCR entries with outcome_correlation < 0.3 | > 30% of CCR | RFC-0032 §4.3 |
| Mandate re-introduction after removal | Any | RFC-0028 §3.2 |
| CCR entries created by leadership (not team) | > 50% | CCR audit |

**Interventions**:
- CCR governance: team-proposed only (Requirement 4)
- Sponsor veto of leadership-proposed CCR entries
- RFC-0024 TIP: Trench Intelligence audit of CCR outcomes

### 7.2 FM-PT-02: Exposure Retaliation

**Definition**: Leader responds to PTDP Exposure briefing by doubling
down on mandates, increasing surveillance, or punishing PTDP
participants.

**Detection Metrics**:
| Metric | Threshold | Source |
|--------|-----------|--------|
| MPCC increase > 0.1 post-Exposure | 30 days | RFC-0028 §3.1 |
| New mandates introduced post-Exposure | Any | Mandate inventory |
| ASM increase > 0.1 post-Exposure | 30 days | RFC-0028 §3.3 |

**Interventions**:
- NSST L1 prerequisite for Exposure (Requirement 9)
- Sponsor immunity for PTDP participants
- RFC-0025 SEP activation if leader retaliation detected
- Board-level MPCC accountability (RFC-0031 §6 Level 3)

## 8. Operational Considerations

### 8.1 Deployment Checklist

- [ ] PTI_v2 measurement pipeline operational (badge + calendar + artifact APIs)
- [ ] CCR platform deployed (team-proposed, sponsor-approved, public)
- [ ] NSST Level 1 active (RFC-0031 §6 — VPA, DSA, AAR-T3)
- [ ] PTDP Sponsor appointed (CTO or Board member)
- [ ] RFC-0028 MPCC monitoring integrated
- [ ] RFC-0029 FM-NP/FM-PT detection active
- [ ] RFC-0024 TIP ground-truth channel established

### 8.2 Monitoring Dashboard

| Metric | Frequency | Owner | Alert Threshold |
|--------|-----------|-------|-----------------|
| PTI_v2 | Weekly | People Ops / CTO | > 1.5 |
| CCR_Coverage | Weekly | Team Leads | < 0.7 |
| CCR Outcome Correlation | Monthly | Sponsor | < 0.5 |
| FM-NP-01/02/03 | Weekly | People Ops | Any detection |
| FM-PT-01/02 | Weekly | Sponsor | Any detection |
| MPCC | Monthly | Board | > 0.6 |

## 9. Security and Privacy Considerations

PTDP metrics (PTI_v2, CCR entries, mandate inventory) extend the
RFC-0022 CCBP §3.8 privacy model:

- **Team-owned data**: CCR entries owned by proposing team
- **Sponsor access only**: Exposure metrics visible only to PTDP Sponsor
- **No individual tracking**: Metrics aggregated at team/org level
- **Retention**: CCR entries retained for TTL + 1 year; PTI_v2 raw data
  purged at 90 days
- **No performance linkage**: PTDP data **MUST NOT** inform performance
  reviews, compensation, or promotion decisions (RFC-0023 PGP separation)
- **Right to audit**: Any team may request PTDP Sponsor audit of their
  CCR coverage and PTI_v2 calculation

## 10. OSC Considerations

### 10.1 Registry Updates

Upon publication:
- RFC-0032 added to registry
- `next_available.rfc_humor` incremented to 4023
- RFC-0028 §8 Extensions table: RFC-0032 status → "Published"
- RFC-0029 EFMT: FM-PT-01, FM-PT-02 added to taxonomy

### 10.2 Prerequisite Chain

PTDP requires sequential activation:
1. RFC-0028 MPCC monitoring (baseline)
2. RFC-0031 NSST Level 1 (supply continuity)
3. RFC-0032 PTDP Audit → Exposure → Substitution → Elimination

Skipping steps triggers FM-PT-02 (Exposure Retaliation) or incomplete
dismantling.

## 11. References

### 11.1 Normative References

[RFC-0004] Matos, R. "Decision Theater Specification (DTS)." RFC 0004.
[RFC-0014] Matos, R. "Consensus Theater Choreography." RFC 0014.
[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017.
[RFC-0022] Matos, R. "Conference Coffee-Break Protocol (CCBP)." RFC 0022.
[RFC-0024] Matos, R. "Trench Intelligence Protocol (TIP)." RFC 0024.
[RFC-0028] Matos, R. "Mandatory Presence Enforcement Protocol (MPEP)." RFC 0028.
[RFC-0029] Matos, R. "Epistemic Failure Mode Taxonomy (EFMT)." RFC 0029.
[RFC-0031] Matos, R. "Narcissistic Supply Substitution Therapy (NSST)." RFC 0031.

### 11.2 Informative References

Matos, R. 2026. "The 500-CEO Study: Narcissism and Proximity Control
in Mandatory Presence Decisions." Paper 012. Organizational
Epistemology Project.

Matos, R. 2026. "Organizational Epistemology Failure Modes: A Case
Compendium." Paper 011. Organizational Epistemology Project.

---

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-19 | R. Matos | Initial draft |

## Appendix B: Open Issues

1. **PTI v2.0 Outcome Correlation Threshold**: The 0.5 correlation
threshold is heuristic. Paper-013 replication data may refine.
[UNVERIFIED]

2. **CCR TTL Calibration**: 90-day default TTL may be too short for
strategic coordination, too long for tactical. Organizational context
matters. [UNVERIFIED]

3. **Cross-Cultural PTI**: High-power-distance cultures may show
baseline PTI_v2 > 1.5 without theater. Regional calibration needed.
[CP-002, UNVERIFIED]

4. **AI-Mediated Coordination**: As AI agents join CCR syncs
(RFC-0028 §B.5), outcome correlation definition must include AI-human
handoffs. [UNVERIFIED]

---

## Colophon

**Epistemic Integrity Level 4 (EI-4): Independent Replication Required**

This RFC specifies a dismantling protocol (PTDP) whose efficacy claims
depend on:
- MPCC = 0.73 from SEG26 (Paper-012) — single-study estimate, requires replication (Paper-013, T001)
- PTI v2.0 outcome correlation methodology — novel, not yet validated in production
- NSST L1 prerequisite — heuristic, requires RFC-0031 deployment data

**Replication Status**: Not yet replicated
**Pre-registration**: PTDP protocol pre-registration target: OSF
**Data Availability**: PTDP deployment data will be restricted (organizational privacy)
**OEP Integration**: RFC-0028 PTI/MPCC, RFC-0029 FM-PT-01/02,
RFC-0031 NSST L1 currently depend on SEG26 parameters and heuristic thresholds

**Review Trigger**: Any independent PTDP deployment with
N > 3 organizations and PTI_v2 pre/post measurement
should trigger RFC-0032 parameter review.