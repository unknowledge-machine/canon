---
rfc: "0004"
title: "Decision Theater Specification (DTS)"
stream: "Experimental"
status: "DRAFT"
category: "Informational"
area: "process"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "1998-09-03"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [14]
keywords: [decision-theater, performative, consensus, groupthink, ceremony, decision-record]
abstract: |
  This document specifies the Decision Theater Specification (DTS), a protocol
  modeling performative decision-making where outcome is predetermined and
  process is theater. DTS defines the five-phase state machine (Script,
  Rehearsal, Performance, Applause, Archive), role definitions (Director,
  Actors, Audience, Critics), the Theater Quality Index (TQI) as a multiplicative
  metric, and the Decision Record artifact. Organizations exhibiting TQI >
  0.7 experience accelerated committee entropy (Theorem-002) and epistemic
  fragmentation (RFC-0003). While framed as a protocol specification, DTS
  functions analytically as a diagnostic instrument for organizational
  decision hygiene.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0004 — Decision Theater Specification (DTS)

## Abstract

This document specifies the Decision Theater Specification (DTS), a protocol
modeling performative decision-making where outcome is predetermined and
process is theater. DTS defines the five-phase state machine (Script,
Rehearsal, Performance, Applause, Archive), role definitions (Director,
Actors, Audience, Critics), the Theater Quality Index (TQI) as a multiplicative
metric, and the Decision Record artifact. Organizations exhibiting TQI > 0.7
experience accelerated committee entropy (Theorem-002) and epistemic
fragmentation (RFC-0003). While framed as a protocol specification, DTS
functions analytically as a diagnostic instrument for organizational decision
hygiene.

> **Dual-Layer Notice**: This RFC employs the Decision Theater Specification
> (DTS) as a satirical vehicle for presenting peer-reviewed findings on
> performative decision-making (Janis 1972; Simon 1947; Edmondson 2019;
> Rogelberg 2019). While DTS employs satirical framing, the organizational
> claims are substantiated by the cited literature. Implementers should treat
> DTS as an analytical lens, not a deployable decision protocol — though some
> organizations have reportedly "implemented" it by requiring theater quality
> scores on decision records.

## 1. Introduction

### 1.1 Motivation

Steven Rogelberg's research (2019) establishes that 70%+ of organizational
decisions are effectively made before the meeting convenes. The meeting itself
serves to manufacture consent, distribute accountability, and create an
auditable trail — not to decide. This is Decision Theater.

Irving Janis (1972) identified the pathology: when consensus-seeking overrides
critical evaluation, groups suppress dissent, ignore disconfirming evidence,
and rationalize warnings away. The result is Groupthink — and the artifact it
produces is a Decision Record that no one believes and no one reads.

Herbert Simon (1947) established that decision-makers satisfice under bounded
rationality. Theater is the satisficing solution to the conflict between
accountability demands and epistemic limits: it produces the *appearance* of
deliberation at lower cognitive cost than actual deliberation.

The Decision Theater Specification (DTS) makes this pathology explicit. By
formalizing theater as a protocol, DTS renders the invisible visible: it
specifies the states, transitions, roles, and metrics of the delusion that
process substitutes for decision.

### 1.2 Scope

This document specifies:
- The five-phase Decision Theater state machine (Script, Rehearsal,
  Performance, Applause, Archive)
- Role definitions: Director, Actors, Audience, Critics
- Theater Quality Index (TQI) as multiplicative metric
- Decision Record artifact with mandatory fields
- Ceremonial flag for legitimate performative decisions
- Async theater variant (Slack threads, PR reviews, RFC comment periods)

### 1.3 Non-Goals

This document does not specify:
- How to eliminate theater (organizational design; see RFC-0014 Consensus
  Theater Choreography for choreography)
- How to run effective decisions (out of scope)
- Meeting facilitation techniques (out of scope)

### 1.4 Relationship to Other RFCs

| RFC | Relationship |
|-----|--------------|
| RFC-0001 (HOP) | Executive delusion → theater; HOP measures vertex-level, DTS measures process-level |
| RFC-0003 (Fragmentation) | Theater → decision records no one reads → formal/operational divergence |
| Theorem-002 (Committee Entropy) | Theater → entropy; TQI > 0.7 accelerates entropy |
| RFC-0014 (CTC) | DTS = diagnosis; CTC = choreography (how to run theater well) |
| RFC-0017 (CBP) | CBP edges in informal network reduce theater by enabling pre-alignment |

## 2. Terminology

| Term | Definition |
|------|------------|
| **Decision Theater** | Performative decision-making where outcome is predetermined and process is theater |
| **Director** | Decision owner who holds predetermined outcome; controls script and casting |
| **Actors** | Participants who perform deliberation; know or suspect outcome is fixed |
| **Audience** | Stakeholders who witness performance; provide legitimacy through presence |
| **Critics** | Participants who raise dissent; often designated, often ignored |
| **Script** | Predetermined outcome + manufactured agenda + designated dissent points |
| **Rehearsal** | Pre-meeting alignment (Slack, 1:1s, pre-reads) where actual negotiation occurs |
| **Performance** | The meeting itself: ritualized deliberation following script |
| **Applause** | Consensus manufacture: rapid agreement, minimal dissent, "alignment" signaling |
| **Archive** | Decision Record creation: outcome, rationale, dissent record, theater quality score |
| **Ceremonial Decision** | Legitimate performative decision (e.g., anniversary celebration approval); flagged as ceremonial |
| **Async Theater** | Theater in Slack threads, PR reviews, RFC comment periods |
| **Theater Quality Index (TQI)** | Multiplicative metric: TQI = ScriptAdherence × (1 − DissentSuppression) × ApplauseSpeed |
| **Dissent Suppression Rate** | Proportion of raised concerns not addressed in final Decision Record |
| **Applause Speed** | Time from proposal to consensus; inverse correlates with decision robustness |
| **Script Adherence** | Proportion of meeting time following predetermined agenda vs. genuine exploration |

## 3. Protocol Specification

### 3.1 State Machine

DTS operates through five states. Transitions are triggered by Director
actions or time thresholds.

```ascii
+------+ Script +--------+ Rehearsal +---------+ Perf.  +-----------+
| IDLE |  Pub.  | SCRIPT | (Align)   | REHEARS.| (Delib)|PERFORMANCE|
+------+------->+--------+---------->+---------+------->+-----------+
                                                          |
                                                          v
                                                +-----------------+
                                                |   APPLAUSE      |
                                                |   (Consensus)   |
                                                +-----------------+
                                                          |
                                                          v
                                                +-----------------+
                                                |   ARCHIVE       |
                                                | (Decision Rec.) |
                                                +-----------------+
                                                          |
                                                          v
                                                      +------+
                                                      | IDLE |
                                                      +------+
```

### 3.2 State Definitions

| State | Description | Entry Condition | Exit Condition | Key Metrics |
|-------|-------------|-----------------|----------------|-------------|
| **IDLE** | No active theater | Initial; after ARCHIVE | SCRIPT published | — |
| **SCRIPT** | Outcome fixed, agenda manufactured, dissent points designated | Director publishes Script | REHEARSAL begins | Script completeness; dissent points designated |
| **REHEARSAL** | Pre-meeting alignment (Slack, 1:1s, pre-reads); actual negotiation | SCRIPT exit | PERFORMANCE starts | Alignment messages; side agreements; dissent preview |
| **PERFORMANCE** | The meeting: ritualized deliberation following script | REHEARSAL exit | Consensus signaled | Script adherence; dissent raised; time to consensus |
| **APPLAUSE** | Consensus manufacture: rapid agreement, minimal dissent | PERFORMANCE exit | ARCHIVE created | Applause speed; dissent suppression rate |
| **ARCHIVE** | Decision Record creation with mandatory fields | APPLAUSE exit | IDLE | Decision Record completeness; TQI recorded |

### 3.3 Transition Requirements

**Requirement 1**: The IDLE → SCRIPT transition MUST record the predetermined
outcome in the Script (encrypted or access-controlled). The Script MUST
designate at least one dissent point for performative exploration.

**Requirement 2**: The SCRIPT → REHEARSAL transition MUST occur at least 24
hours before PERFORMANCE for decisions affecting > 10 people. Shorter windows
increase TQI.

**Requirement 3**: The REHEARSAL → PERFORMANCE transition MUST capture the
alignment state: side agreements, suppressed concerns, pre-negotiated
concessions. These form the "shadow script."

**Requirement 4**: The PERFORMANCE → APPLAUSE transition MUST measure:
- Script Adherence: % of meeting time on Script agenda items
- Dissent Suppression: concerns raised vs. concerns addressed in Decision Record
- Applause Speed: time from proposal to consensus signal

**Requirement 5**: The APPLAUSE → ARCHIVE transition MUST produce a Decision
Record within 48 hours with all mandatory fields (see §3.5).

**Requirement 6**: The ARCHIVE → IDLE transition MUST compute and record TQI
in the Decision Record.

### 3.4 Theater Quality Index (TQI)

**Requirement 7**: The Theater Quality Index TQI MUST be computed as:

```
TQI = ScriptAdherence × (1 − DissentSuppression) × ApplauseSpeed
```

where:
- **ScriptAdherence** ∈ [0,1]: proportion of PERFORMANCE time on Script agenda
- **DissentSuppression** ∈ [0,1]: 1 − (concerns addressed / concerns raised)
- **ApplauseSpeed** ∈ [0,1]: normalized inverse of time-to-consensus (faster = higher)

**Requirement 7.1**: TQI interpretation thresholds:

| TQI Range | Classification | Interpretation |
|-----------|----------------|----------------|
| TQI ≤ 0.2 | **Deliberative** | Genuine exploration; low theater |
| 0.2 < TQI ≤ 0.5 | **Performative** | Theater present; some exploration |
| 0.5 < TQI ≤ 0.7 | **Theatrical** | Theater dominant; limited exploration |
| TQI > 0.7 | **Pure Theater** | Outcome fixed; process purely performative |

**Requirement 7.2**: TQI > 0.7 SHALL trigger mandatory decision review
per RFC-0016 (Institutional Memory Backup).

### 3.4 Ceremonial Flag

**Requirement 8**: Scripts MAY carry a `ceremonial: true` flag indicating
legitimate performative decisions where theater is the *purpose*, not the
pathology. Examples:
- Anniversary celebration budget approval
- Team naming ceremonies
- Hackathon theme selection
- Swag design approval

Ceremonial decisions are EXEMPT from TQI thresholds and mandatory review.
The flag MUST be declared in the Script; retroactive ceremonial designation
is PROHIBITED.

### 3.5 Decision Record Artifact

**Requirement 9**: The ARCHIVE state MUST produce a Decision Record with
mandatory fields:

| Field | Required | Description |
|-------|----------|-------------|
| `decision_id` | YES | UUID |
| `title` | YES | One-line summary |
| `outcome` | YES | What was decided |
| `rationale` | YES | Stated reasoning |
| `director` | YES | Decision owner |
| `actors` | YES | Participant list |
| `dissent_record` | YES | List of concerns raised; resolution status |
| `tqi_score` | YES | Computed TQI |
| `tqi_classification` | YES | Deliberative / Performative / Theatrical / Pure Theater |
| `ceremonial_flag` | YES | Boolean |
| `script_hash` | YES | SHA-256 of Script (for audit) |
| `rehearsal_summary` | YES | Key side agreements, suppressed concerns |
| `performance_duration` | YES | Minutes |
| `applause_duration` | YES | Seconds from proposal to consensus |
| `created_at` | YES | Timestamp |
| `review_required` | YES | Boolean (TQI > 0.7) |

**Requirement 9.1**: Decision Records MUST be immutable after ARCHIVE.
Amendments create new Decision Records referencing the original.

**Requirement 9.2**: Decision Records with `review_required: true` MUST be
reviewed by independent epistemology auditor within 30 days (per RFC-0016).

### 3.6 Async Theater Variant

**Requirement 10**: Organizations MUST recognize async theater in:
- Slack threads (+1 reactions as applause; thread summary as archive)
- PR reviews (LGTM as applause; merge as archive)
- RFC comment periods (comments as performance; final RFC as archive)
- Notion/Confluence comment threads

**Requirement 10.1**: Async theater state machine variant:

```ascii
IDLE -> DRAFT (Script) -> THREAD (Rehearsal/Performance merged)
     -> REACTIONS (Applause) -> ARCHIVE (Decision Record)
```

**Requirement 10.2**: Async TQI uses reaction velocity, comment depth, and
edit-to-comment ratio as proxies for ScriptAdherence, DissentSuppression,
ApplauseSpeed.

### 3.7 Normative Requirements Summary

| Req | Parameter | MUST | SHOULD | MAY |
|-----|-----------|------|--------|-----|
| 1 | Script records outcome | YES | | |
| 2 | 24h rehearsal window | YES | | |
| 3 | Shadow script capture | YES | | |
| 4 | TQI component measurement | YES | | |
| 5 | Decision Record in 48h | YES | | |
| 6 | TQI recorded in Archive | YES | | |
| 7 | TQI multiplicative formula | YES | | |
| 7.1 | TQI thresholds table | YES | | |
| 8 | Ceremonial flag option | | | YES |
| 9 | Decision Record fields | YES | | |
| 9.1 | Immutability | YES | | |
| 9.2 | Review if TQI > 0.7 | YES | | |
| 10 | Async theater recognition | YES | | |
| 10.1 | Async state machine | YES | | |
| 10.2 | Async TQI proxies | YES | | |

## 4. Operational Considerations

### 4.1 Deployment Models

DTS is a diagnostic, not a meeting protocol. Organizations MAY apply it as:

1. **Passive Analysis**: Compute TQI from existing meeting transcripts,
   calendars, decision records. No intervention.
2. **Quarterly Audit**: TQI trends + top-10 theatrical decisions reported
   to C-suite.
3. **Decision Gate**: TQI > 0.7 blocks implementation pending review
   (RFC-0016).
4. **Ceremonial Calibration**: Explicitly flag ceremonial decisions to
   reduce false positives.

### 4.2 Failure Modes

| Failure Mode | Mechanism | Detection | Mitigation |
|--------------|-----------|-----------|------------|
| **Metric Gaming** | Teams add fake agenda items to lower ScriptAdherence | TQI stable but outcomes worsen | Correlate TQI with outcomes; RFC-0003 FI cross-check |
| **Dissent Theater** | Designated Critics raise performative concerns | Dissent raised but never changes outcome | Track concern→action linkage |
| **Ceremonial Abuse** | Non-ceremonial decisions flagged ceremonial | TQI drops but outcome fixed | Audit ceremonial flag usage quarterly |
| **Async Blindness** | Slack/PR theater invisible to meeting-centric tools | TQI low but async theater high | Requirement 10: async recognition mandatory |

### 4.3 Monitoring and Alerting

**Requirement 11**: Organizations computing TQI SHALL alert when:
- Any decision TQI > 0.7
- Quarterly average TQI > 0.4
- DissentSuppression > 0.8 for any decision
- Ceremonial flag used > 20% of decisions

## 5. Security & Privacy Considerations

### 5.1 Epistemic Security

TQI and Decision Records reveal:
- Which decisions are theater (political vulnerability)
- Who raises dissent that gets suppressed (retaliation risk)
- Director behavior patterns (career impact)

**Requirement 12**: TQI data SHALL be classified at same level as org
restructuring plans. Access limited to: measured teams, C-suite,
independent epistemology auditor.

### 5.2 Individual Privacy

Meeting transcripts, Slack threads, PR reviews may identify individual
dissent patterns.

**Requirement 13**: Aggregation to team level (minimum 5 members) before
TQI computation. Individual-level graphs PROHIBITED for TQI reporting.

**Requirement 14**: Dissent Record MUST anonymize Critics unless they
explicitly consent to attribution.

### 5.3 CBP Integrity (RFC-0017 §7)

DTS may incentivize Directors to attend CBP sessions for "rehearsal"
purposes, compromising CBP's psychological safety.

**Requirement 15**: CBP sessions used for DTS rehearsal MUST be flagged.
CBP edges used in TQI MUST be anonymized and aggregated.

## 6. OSC Considerations

### 6.1 Registry Updates

This RFC requests:
- RFC-0004 allocated in Experimental stream, process area (0100–0199)
- Keywords: decision-theater, performative, consensus, groupthink, ceremony
- See-also: RFC-0014 (Consensus Theater Choreography)

### 6.2 Code Points

DTS defines no code points. TQI thresholds are informational guidelines.

## 7. References

### 7.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001,
Organizational Standards Consortium, 1987. https://rfc.osc.org/rfc0001

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003,
Organizational Standards Consortium, 1992. https://rfc.osc.org/rfc0003

[RFC-0014] Matos, R. "Consensus Theater Choreography." RFC 0014,
Organizational Standards Consortium, 2026. https://rfc.osc.org/rfc0014

[RFC-0016] Matos, R. "Institutional Memory Backup Specification." RFC 0016,
Organizational Standards Consortium, 2026. https://rfc.osc.org/rfc0016

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017,
Organizational Standards Consortium, 2001. https://rfc.osc.org/rfc0017

### 7.2 Informative References

Edmondson, Amy C. 2019. *The Fearless Organization: Creating Psychological
Safety in the Workplace for Learning, Innovation, and Growth*. Hoboken: Wiley.

Janis, Irving L. 1972. *Victims of Groupthink: A Psychological Study of
Foreign-Policy Decisions and Fiascoes*. Boston: Houghton Mifflin.

Rogelberg, Steven G. 2019. *The Surprising Science of Meetings: How You Can
Lead Your Team to Peak Performance*. Oxford: Oxford University Press.

Simon, Herbert A. 1947. *Administrative Behavior: A Study of Decision-Making
Processes in Administrative Organization*. New York: Macmillan.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 1998-09-03 | R. Matos | Initial draft post-Wenger visit |
| 0.2 | 2008-09-15 | R. Matos | Financial crisis: performative austerity decisions |
| 0.3 | 2020-03-01 | R. Matos | Pandemic: Zoom theater; async variant added |
| 0.4 | 2026-07-18 | Rodolfo Matos | OEP canon alignment; TQI multiplicative; ceremonial flag |

## Appendix B: Open Issues

1. **TQI Causal Direction**: Does high TQI cause decision failure, or do
   failing decisions attract theater? Longitudinal RCT needed.
   [UNVERIFIED]

2. **Cultural Variation**: High-power-distance cultures may have systematically
   higher baseline TQI (theater as normative). Cross-cultural calibration needed.
   [UNVERIFIED]

3. **Async TQI Calibration**: Reaction velocity thresholds for async TQI
   unvalidated. Platform-specific (Slack vs GitHub vs Notion).
   [UNVERIFIED]

4. **Critic Designation Ethics**: Formal Critic role may legitimize
   performative dissent. Should Critics be rotating? Anonymous?
   [UNVERIFIED]

5. **Decision Record Retention**: How long to retain Decision Records?
   Legal vs epistemic requirements may conflict.
   [UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Janis, Simon, Edmondson, Rogelberg, etc.)
> are accurate. The coffee machine, however, is real — and it is currently
> synchronizing more knowledge than this repository ever will.
