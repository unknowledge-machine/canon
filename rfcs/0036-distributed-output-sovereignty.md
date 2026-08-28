---
rfc: "0036"
title: "Distributed Output Sovereignty Protocol (DOSP)"
stream: "Experimental"
status: "DRAFT"
category: "Informational"
area: "informal-networks"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
created: "2026-08-09"
updated: "2026-08-09"
obsoletes: []
obsoleted_by: []
see_also: [35, 17, 1, 5, 38]
keywords:
  - stealth
  - autonomy
  - sovereignty
  - listen-only
  - adaptive-space
  - beaver
  - ECI-reduction
abstract: |
  This document specifies the Distributed Output Sovereignty Protocol (DOSP),
  a Layer-A behavioral protocol for leaders whose epistemic capture distorts the
  knowledge they receive. DOSP prescribes two behavioral primitives: (a) the
  Abstenção de Engenharia (Builder's Recusal) — attending Adaptive Space
  sessions in Listen-Only mode, refraining from issuing directives even when
  technical errors are detected, trusting truth vertices for autocorrection; and
  (b) the Contentor de Segurança (Adaptive Dam) — using formal authority
  exclusively to remove external bureaucratic obstacles, creating an Adaptive
  Space where the team retains total sovereignty over execution method. DOSP is
  voluntary by construction: it encourages behavior, never mandates attendance,
  and private diagnosis is not institutional measurement.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0036 — Distributed Output Sovereignty Protocol (DOSP)

## Abstract

This document specifies the Distributed Output Sovereignty Protocol (DOSP), a
Layer-A behavioral protocol for leaders whose epistemic capture distorts the
knowledge they receive. DOSP prescribes two behavioral primitives: (a) the
**Abstenção de Engenharia (Builder's Recusal)** — attending Adaptive Space
sessions in Listen-Only mode, refraining from issuing directives even when
technical errors are detected, trusting truth vertices for autocorrection; and
(b) the **Contentor de Segurança (Adaptive Dam)** — using formal authority
exclusively to remove external bureaucratic obstacles, creating an Adaptive
Space where the team retains total sovereignty over execution method. DOSP is
voluntary by construction: it encourages behavior, never mandates attendance,
and private diagnosis is not institutional measurement.

> **Dual-Layer Notice**: This RFC presents the Distributed Output Sovereignty
> Protocol as a satirical vehicle for peer-reviewed findings on leader
> epistemic capture and autonomy-supportive leadership. The serious layer is
> behavioral: leaders who stop engineering and start clearing debris learn
> more. The satirical layer is the ritualization: the protocol reads like a
> dam manual because, in power-dominant organizations, protecting autonomy is
> treated as a covert hydraulic operation.

## Status

DRAFT — Submitted for Editorial, Technical, and Canon review.

## 1. Introduction

### 1.1 Problem Statement

Leaders in power-dominant organizations (RFC-0001) receive filtered,
upward-distorted knowledge. The Knowledge Gravity Index (KGI, RFC-0005)
quantifies this distortion: knowledge flows toward power, distorting as it
moves. Traditional remediation — measuring the distortion more often,
publishing dashboards, adding approval layers — fails because the measurement
apparatus is itself captured: metrics computed by the hierarchy are gamed by
the hierarchy (Theorem-001 cross-check).

The failure is structural, not informational. Leaders do not lack data. They
lack a channel that the hierarchy does not control — and they lack the
behavioral discipline to use that channel without capturing it.

The Epistemic Capture Index (ECI, RFC-0001) formalizes this:
ECI = (OR × DL_avg) / max(FF, 0.1), where OR is the Omniscience Radius
(distance in communication hops to operational reality), DL_avg is average
Directive Latency, and FF is Feedback Fidelity. High ECI means the leader
reacts to a mirage.

### 1.2 Scope

DOSP is a Layer-A behavioral protocol for leaders. It specifies what a leader
*does*, not what an organization *mandates*. DOSP does not create new metrics,
new committees, new reporting lines, new roles, or new dashboards. Where a
metric or mechanism is referenced, it already exists (RFC-0001 ECI, RFC-0017
Listen-Only CHP, RFC-0035 ESP, Paper-014 Adaptive Space). DOSP adds leader
behavior; it does not amend the protocols it references.

## 2. Terminology

| Term | Definition |
|------|------------|
| **DOSP** | Distributed Output Sovereignty Protocol, this document. |
| **Abstenção de Engenharia** | The leader's behavioral commitment to attend Adaptive Space sessions in Listen-Only mode (RFC-0017 §3.2, RFC-0035 §3.2) and refrain from issuing directives, trusting truth vertices for autocorrection. |
| **Contentor de Segurança** | The leader's use of formal authority exclusively to remove external bureaucratic obstacles ("debris"), creating an Adaptive Space where the team has total sovereignty over execution method. |
| **ASM (Autonomy Suppression Index)** | Private heuristic: measures reduction in team's decision latitude when leader is present. Target: ASM < 0.1. Private diagnostic lens, not institutional metric. |
| **DL (Directive Latency)** | Private heuristic: time for team to ignore leader's informal suggestion in favor of real technical evidence from Adaptive Space. High DL for leader suggestions = epistemic health signal. |
| **Dam Factor** | Private heuristic: proportion of technical decisions made by team without formal hierarchy consultation. Target: > 0.8. |
| **Adaptive Space** | The informal network context where un-captured nodes exchange knowledge outside formal channels (Paper-014; RFC-0038 instantiation as iLab). |
| **Truth Vertex** | A vertex that knows how the organization works in practice, distinct from a power vertex that only appears central (RFC-0005). |
| **Non-Capture Principle** | Any mechanism that converts informal connections into formal reporting lines destroys their capacity to carry candid knowledge (Theorem-001; RFC-0035 Rule ESP-6). DOSP forbids formalizing the *role*, never pricing the *value*. |

## 3. Protocol Specification

DOSP consists of two behavioral primitives. Compliance is measured by the
leader's own practice, not by organizational surveillance.

### 3.1 Abstenção de Engenharia (The Builder's Recusal)

**Behavior**: The leader attends Adaptive Space sessions (Paper-014; RFC-0038
iLab instantiation) or Coffee-Break Protocol sessions (RFC-0017) in Listen-Only
mode as defined in RFC-0017 §3.2 and RFC-0035 §3.2. The leader observes
without initiating handshakes, does not speak, does not identify as
management, and does not issue directives.

**Rationale**: Listen-Only attendance permits ECI reduction through passive
synchronization without collapsing psychological safety (Edmondson 1999;
RFC-0001 §4.1). The leader's silence is the point: the channel closes the
moment management is detected. The Abstenção de Engenharia goes further: even
when the leader detects a technical error or a deviation from plan, the leader
is PROHIBITED from issuing an immediate directive. The leader must trust the
truth vertices (the specialists) for autocorrection. Intervention freezes the
network; autocorrection preserves it.

**Rule DOSP-1**: The leader SHALL attend Adaptive Space sessions in Listen-Only
mode without speaking, asking questions, or identifying as management.

**Rule DOSP-2**: The leader SHALL NOT issue directives, corrections, or
"guidance" during Adaptive Space attendance. If a technical error is detected,
the leader documents it privately and trusts the truth vertices for
autocorrection.

**Rule DOSP-3**: Attendance is voluntary. DOSP MUST NOT be used to mandate
Adaptive Space participation. Mandated attendance destroys the psychological
safety the protocol depends on (RFC-0035 Rule ESP-4).

**Rule DOSP-4**: The leader SHALL NOT convert Listen-Only attendance into a
reporting line, a dashboard metric, or a performance indicator. Attendance is
a behavioral habit, not a program metric (RFC-0035 §6.3).

### 3.2 Contentor de Segurança (The Adaptive Dam)

**Behavior**: Instead of managing tasks, the leader acts as a Broker of
resources. The leader uses formal authority *exclusively* to remove external
bureaucratic obstacles — the "debris" of the formal system: approval chains
that delay experiments, budget gates that block prototypes, compliance
processes that delay prototypes, reporting requirements that consume
engineering time. The leader creates an Adaptive Space (Paper-014; RFC-0038
iLab) where the team has total sovereignty over execution method.

**Rationale**: The Knowledge Gravity Theorem (Theorem-003, RFC-0005) proves that
knowledge flows toward power gradients, distorting as it moves. The leader's
directive presence is a power gradient. By removing obstacles instead of
directing work, the leader inverts the gradient: the leader becomes a
centrifugal force, pushing bureaucracy outward so knowledge can flow inward.
The "dam" holds back the flood of bureaucracy so the team's stream can flow.

**Rule DOSP-5**: The leader SHALL use formal authority exclusively to remove
external bureaucratic obstacles: approval chains, budget gates, compliance
delays, reporting overhead. The leader SHALL NOT use authority to direct
technical method, assign tasks, or override team decisions.

**Rule DOSP-6**: The Contentor de Segurança is a behavioral stance, not a role.
The leader SHALL NOT formalize this stance into a title, position, reporting
line, badge, or "program". Formalizing the stance destroys it (Non-Capture
Principle; Rule ESP-6). The leader remains the leader; the change is in
behavior, not structure.

**Rule DOSP-7**: The leader SHALL ensure the team has total sovereignty over
execution method within the cleared space. The leader does not assign tasks,
does not approve technical approaches, does not review code as gatekeeper. The
team's sovereignty is the point; the leader's clearance is the enabler.

## 4. Diagnóstico Furtivo (Private Heuristics)

DOSP defines three private diagnostic heuristics for the leader's own
calibration. These are **not institutional metrics**. They are not published,
dashboarded, reported, or institutionalized. The leader may quantify them for
self-calibration; the organization does not. The absence of infrastructure is
a feature (RFC-0035 §6.3).

### 4.1 ASM — Autonomy Suppression Index

**Definition**: Measures the reduction in the team's decision latitude when the
leader is present vs. absent.

**Observation Method**: The leader observes privately: when present, does the
team defer decisions that they would make autonomously? Do they seek approval
for things they would normally decide? Do they self-censor technical
disagreements?

**Target**: ASM < 0.1 (less than 10% reduction in autonomous decision-making).

**Interpretation**: High ASM means the leader's presence suppresses autonomy —
the leader is the bottleneck. Low ASM means the team operates with full
sovereignty even when the leader is present.

**Rule DOSP-8**: ASM is a private diagnostic lens for the leader's
self-calibration. It is not published, dashboarded, reported, or
institutionalized.

### 4.2 DL — Directive Latency

**Definition**: The time (in interactions) for the team to ignore the leader's
informal suggestion in favor of real technical evidence from the Adaptive
Space.

**Observation Method**: The leader makes an informal suggestion (not a
directive — DOSP forbids directives). The leader observes how long the team
takes to evaluate it against real technical evidence from the Adaptive Space
and discard it if contradicted by evidence.

**Target**: High DL for leader suggestions. Paradoxically, a team that quickly
ignores the leader's bad suggestions in favor of real evidence is
epistemically healthy. A team that obeys immediately is captured.

**Interpretation**: High DL for leader suggestions = epistemic health signal
(paradoxical). The team trusts evidence over authority.

**Rule DOSP-9**: DL is a private diagnostic lens for the leader's
self-calibration. It is not published, dashboarded, reported, or
institutionalized.

### 4.3 Dam Factor

**Definition**: The proportion of technical decisions made by the team without
formal hierarchy consultation.

**Observation Method**: Over a measurement window, the leader counts: (a)
technical decisions made autonomously by the team; (b) technical decisions
escalated to hierarchy for approval. Dam Factor = (a) / (a + b).

**Target**: Dam Factor > 0.8 (more than 80% of technical decisions made
autonomously).

**Interpretation**: High Dam Factor = the "dam" is holding — bureaucracy is
blocked, team sovereignty flows. Low Dam Factor = bureaucracy seeps through,
team waits for permission.

**Rule DOSP-10**: Dam Factor is a private diagnostic lens for the leader's
self-calibration. It is not published, dashboarded, reported, or
institutionalized.

## 5. Impacto no ECI (Epistemic Capture Index)

The Epistemic Capture Index is defined in RFC-0001 as:

    ECI = (OR × DL_avg) / max(FF, 0.1)

Where:
- **OR (Omniscience Radius)**: Distance in communication hops between leader
  and operational reality.
- **DL_avg**: Average Directive Latency across all directive channels.
- **FF (Feedback Fidelity)**: Proportion of signals reaching the leader that
  accurately represent operational reality.

DOSP attacks all three components:

1. **OR ↓ (Omniscience Radius Reduction)**: By attending Adaptive Space in
   Listen-Only mode, the leader physically and socially reduces the number of
   intermediaries filtering information. The leader approaches truth vertices
   directly. OR decreases.

2. **FF ↑ (Feedback Fidelity Increase)**: The Abstenção de Engenharia prevents
   the leader from freezing the network. Without fear of immediate directive,
   truth vertices share unfiltered operational reality. FF increases.

3. **DL_avg → DL for leader suggestions**: The DL heuristic measures latency
   for *leader* suggestions specifically. High DL for leader suggestions means
   the team evaluates authority against evidence — a component of FF.

**Net Effect**: ECI = (OR × DL_avg) / max(FF, 0.1)
- Numerator ↓ (OR decreases)
- Denominator ↑ (FF increases)
- **ECI decreases**.

**Composite Illustration — Meridian Financial**: A fictional institution's CEO
began attending the Adaptive Space (a cleared conference room, no agenda, no
badge) in Listen-Only mode twice per week. Over six months, the CEO's
measured OR dropped from 5 to 3 (direct access to two additional truth
vertices), FF rose from 0.12 to 0.38 (unfiltered signals from truth vertices
increased), and ECI fell from 89 to 34. The CEO did not issue a single
directive during Adaptive Space sessions. The institution did not track
attendance. The knowledge flowed; the channel stayed open; the ECI dropped.
*This is a composite illustration per RFC-0035 §3.3.2 precedent; no
institution named Meridian Financial exists.*

## 6. Relationship to Other RFCs

- **RFC-0035 (ESP)**: DOSP is the leader-in-Adaptive-Space specialization of
  ESP. ESP Layer-A behaviors (weak-tie cultivation, Listen-Only attendance,
  connector identification) are prerequisites. DOSP adds the Abstenção de
  Engenharia and Contentor de Segurança primitives specific to leader-in-
  Adaptive-Space context.
- **RFC-0017 (CBP)**: DOSP Layer-A behavior depends on the Listen-Only CHP
  defined in RFC-0017 §3.2. DOSP adds leader behavioral discipline; it does not
  amend the protocol.
- **RFC-0001 (HOP)**: DOSP operationalizes ECI reduction as voluntary leader
  practice. DOSP aligns with RFC-0001 §5.3 Requirement 15 (ECI ≥ 10 →
  Listen-Only attendance).
- **RFC-0005 (KGMF)**: DOSP's Contentor de Segurança directly counters
  Knowledge Gravity by creating a low-gravity zone (Adaptive Space) where
  truth vertices and power vertices meet without reporting-line conversion.
- **Paper-014 (Adaptive Space)**: DOSP operates within the Adaptive Space
  infrastructure; the Abstenção de Engenharia and Contentor de Segurança are
  the leader-facing behavioral primitives for that infrastructure.
- **RFC-0038 (iLab)**: The iLab is a canonical instantiation of the Adaptive
  Space (Paper-014). DOSP leader behaviors are designed for the iLab's
  anti-theater properties.

DOSP supersedes no other RFC. It implements behavior consistent with findings
already documented in the RFCs above.

## 7. Security Considerations

### 7.1 Narcisismo de Proximidade (FM-NP-01)

A leader may use "autonomy" and "listen-only" as a trap: attending Adaptive
Space sessions to observe failures, then reasserting visual dominance by
criticizing the very autonomy they claimed to grant. This is the Narcisismo de
Proximidade — proximity weaponized as dominance.

**Mitigation**: The Non-Capture Principle (Rule ESP-6) and the Abstenção de
Engenharia (Rule DOSP-2) forbid converting observation into correction. The
leader's private ASM heuristic (Rule DOSP-8) detects this: if ASM rises when
leader attends, the leader is capturing, not releasing.

### 7.2 Amnésia por Abandono (FM-AB-01)

A leader may confuse "autonomy" with "disinterest", ceasing to feed Strategic
Context Availability (SCA, RFC-0006) to the team. The team gains sovereignty
over *method* but loses *context* — fragmentation increases (FI, RFC-0003).

**Mitigation**: DOSP does not relieve the leader of SCA feeding (RFC-0006).
The Contentor de Segurança (Rule DOSP-5) includes removing context-blocking
bureaucracy. The leader's private Dam Factor heuristic (Rule DOSP-10) detects
abandonment: if Dam Factor rises but FI rises, the team has method sovereignty
without strategic context.

### 7.3 Surveillance Misuse

An organization that deploys DOSP as a surveillance mechanism — monitoring
which leaders attend which sessions, mapping ASM/DL/Dam Factor for evaluation
— violates the private heuristic principle (Rules DOSP-8, DOSP-9, DOSP-10) and
the voluntary basis of DOSP. Such deployment is anti-therapeutic and SHALL be
rejected.

### 7.4 Formalization of the Contentor de Segurança

An organization that formalizes the Contentor de Segurança into a role —
"Adaptive Dam Manager", "Bureaucracy Clearance Officer" — violates Rule DOSP-6
and the Non-Capture Principle. The Contentor de Segurança is a behavioral
stance, not a role. Formalizing it destroys it.

## 8. Operational Considerations

### 8.1 Deployment

DOSP requires no organizational infrastructure. The leader requires:
- Access to an Adaptive Space session (Paper-014; RFC-0038 iLab or CBP venue)
- Permission to attend without management identification
- Protected time (RFC-0001 §4.1 Model 3)
- Willingness to be silent and to clear debris

### 8.2 Failure Modes

| Mode | Behavior | Outcome |
|------|----------|---------|
| Narcisismo de Proximidade (FM-NP-01) | Leader uses "autonomy" as trap to observe failures and reassert dominance | Psychological safety collapses; Adaptive Space closes |
| Amnésia por Abandono (FM-AB-01) | Leader confuses autonomy with disinterest; stops feeding SCA | FI rises; team has method sovereignty without strategic context |
| Contentor Formalizado | Organization formalizes Contentor de Segurança as role | Behavioral stance destroyed; bureaucracy returns with a badge |
| Vetted Space | Organization adds approval committee, dashboard, or portfolio to Adaptive Space | The space becomes a proposal funnel; brokers submit instead of assemble; space closes (RFC-0035 §6.2) |
| Surveillance | Organization maps attendance/ASM/DL for evaluation | Psychological safety collapses; attendance stops |
| Forum Theater | Leader attends but room was staged | No candid knowledge; ECI unchanged |

### 8.3 Non-Goals

DOSP does not create new metrics, new dashboards, new reports, new roles, new
committees, or new reporting lines. The absence of infrastructure is a feature:
the protocol is a habit, not a program (RFC-0035 §6.3).

**Rule DOSP-11**: DOSP SHALL NOT be used to create metrics, dashboards, roles,
reporting lines, or approval committees. Any such creation is a DOSP violation
and reverts the protocol to theater.

## 9. IANA Considerations

None. This protocol assigns no numbers, codes, or parameters.

## 10. References

### 10.1 Normative

- RFC-0035: Executive Stealth Protocol (ESP) — §3.2 Listen-Only CHP, Rule
  ESP-6, §3.3.1 archetypes, §3.3.2 Half-Day composite, §6.2 failure modes,
  §6.3 non-goals
- RFC-0017: Coffee-Break Protocol (CBP) — §3.2 Listen-Only CHP, §3.9 Safe-Space
  Design, §3.9.4 Minimum Trust Law, §3.9.8 Non-Exploitation Condition
- RFC-0001: Hierarchical Omniscience Protocol (HOP) — ECI formula, OR, DL, FF,
  §5.3 Requirement 15
- RFC-0005: Knowledge Gravity Measurement Framework (KGMF) — Knowledge Gravity,
  truth vertices vs power vertices
- Paper-014: Adaptive Space: Theoretical Foundations and Canon Integration —
  Adaptive Space definition, connector archetypes, metric impact table
- RFC-0038: Living Innovation Lab (iLab) — Adaptive Space instantiation,
  anti-theater properties, Non-Capture Principle

### 10.2 Informative

- [Edmondson 1999] "Psychological Safety and Learning Behavior in Work Teams",
  *Administrative Science Quarterly* 44(2): 350-383.
- [RFC-0035 §3.3.2] Half-Day (Composite) — fictional institution illustration
  precedent.
- [Theorem-001] Coffee Machine Theorem — informal bandwidth exceeds formal.
- [Theorem-003] Knowledge Gravity Theorem — power-knowledge distortion dynamics.

## Appendix A: Changelog

- 2026-08-09: Created as Layer-A behavioral protocol for leaders (DOSP);
  Abstenção de Engenharia + Contentor de Segurança primitives; ASM/DL/Dam
  Factor private heuristics; ECI mathematical impact; Meridian Financial
  composite illustration (per RFC-0035 §3.3.2).

## Appendix B: Open Issues

1. **Private Heuristic Calibration Precision**: Rules DOSP-8/9/10 define ASM,
   DL, Dam Factor as private heuristics. Formal calibration methods are
   deliberately absent to prevent metric gaming. [UNVERIFIED]

2. **Threshold Alignment Audit**: RFC-0001 §5.3 and RFC-0017 §3.2 agree on
   ECI ≥ 10 for Listen-Only attendance. DOSP aligns with this threshold. Any
   future divergence SHOULD be flagged. [UNVERIFIED]

3. **DOSP-GAAP Interaction**: RFC-0037 (GAAP) protects Energizers; DOSP
   protects team sovereignty. The interaction when a leader applies both in
   the same Adaptive Space is not yet specified. [UNVERIFIED]

---

## Colophon

**Epistemic Integrity Level 4 (EI-4): Independent Replication Required**

This RFC prescribes leader behaviors whose efficacy claims depend on:
- Listen-Only CHP ECI reduction (RFC-0017 §3.2) — deployment data restricted
  (executive privacy)
- Non-Capture Principle — theoretical, derived from Theorem-001
- ECI formula (RFC-0001) — formal, not yet empirically calibrated (see
  Paper-013)

**Replication Status**: Not yet replicated
**Pre-registration**: None required (behavior protocol)
**Data Availability**: Adaptive Space session data restricted (RFC-0017
privacy model; RFC-0035 privacy model)
**OEP Integration**: RFC-0035 §3.2, RFC-0017 §3.2, RFC-0001 §5.3, RFC-0005,
Paper-014, RFC-0038 depend on voluntary leader behavior. DOSP adds no new
parameters.

**Review Trigger**: Any independent deployment reporting behavioral change in
leader knowledge reception (measured qualitatively, not by ECI publication)
should trigger RFC-0036 parameter review.