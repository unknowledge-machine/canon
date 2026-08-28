---
rfc: "0011"
title: "Meeting Entropy Acceleration Protocol"
stream: "Humor"
status: "DRAFT"
category: "Informational"
area: "informal-networks"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-18"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [4, 14, 17]
keywords: [meetings, entropy, acceleration, duration, productivity-inverse]
abstract: |
  This document specifies the Meeting Entropy Acceleration Protocol
  (MEAP), a formal model for predicting and accelerating the entropy
  of organizational meetings. MEAP introduces the Meeting Duration
  Multiplier (MDM), the Agenda Decay Function (ADF), and the
  Decision Avoidance Index (DAI). Experimental evidence suggests
  that meetings without MEAP converge to zero productivity at a
  rate inversely proportional to the number of attendees.
dual_layer: true
satire_notice: "satire"
---

# RFC-0011 — Meeting Entropy Acceleration Protocol

## Abstract

This document specifies the Meeting Entropy Acceleration Protocol
(MEAP), a formal model for predicting and accelerating the entropy
of organizational meetings. MEAP introduces the Meeting Duration
Multiplier (MDM), the Agenda Decay Function (ADF), and the
Decision Avoidance Index (DAI). Experimental evidence suggests
  that meetings without MEAP converge to zero productivity at a
  rate inversely proportional to the number of attendees.

> **Satire Notice**: This document is published in the **Humor** stream.
> While technically coherent, its primary purpose is satirical illumination
> of organizational dynamics. The OSC does not recommend deploying MEAP
> in production without IRB approval and a very large whiteboard.

## 1. Introduction

Every meeting follows a predictable trajectory: initial purpose,
gradual drift, entropy maximization, and eventual collapse into
scheduling the next meeting. MEAP formalizes this trajectory
to enable organizations to measure, predict, and — if desired —
accelerate meeting entropy.

The protocol is motivated by the observation that the most
productive meeting is the one that never happens, and the second
most productive is the one that ends early.

## 2. Terminology

| Term | Definition |
|------|------------|
| **Meeting** | A gathering of 3+ humans with a shared calendar invite and divergent objectives. |
| **Entropy** | The degree to which a meeting has abandoned its original purpose. |
| **Agenda** | A list of topics that will not be discussed in the order listed. |
| **Action Item** | A task assigned during a meeting that will never be completed. |
| **Parking Lot** | A psychological container for ideas that are simultaneously important and permanently deferred. |
| **Meeting Duration Multiplier (MDM)** | Factor by which meeting duration exceeds productive content. |
| **Agenda Decay Function (ADF)** | Rate at which agenda items are replaced by unplanned topics. |
| **Decision Avoidance Index (DAI)** | Probability that a meeting concludes without any decision. |

## 3. Protocol Specification

### 3.1 Meeting Duration Multiplier (MDM)

MDM quantifies the ratio of actual meeting duration to the
minimum duration required for the meeting's stated purpose:

```
MDM = T_actual / T_minimum
```

Where:
- `T_actual` = actual meeting duration (minutes)
- `T_minimum` = minimum duration for stated purpose (minutes)

**MDM Calibration Table**:
| Meeting Type | Typical MDM | Productivity |
|-------------|-------------|--------------|
| Status Update | 2.5 | 40% |
| Brainstorm | 3.0 | 33% |
| Decision | 4.0 | 25% |
| All-Hands | 5.0 | 20% |
| Retrospective | 2.0 | 50% |
| "Quick Sync" | 6.0 | 17% |

**MEAP Prediction**: MDM increases monotonically with attendee
count. For N attendees:

```
MDM(N) = 1.5 + 0.5 * log2(N)
```

### 3.2 Agenda Decay Function (ADF)

The Agenda Decay Function models how agenda items degrade over
time during a meeting:

```
ADF(t) = A_0 * e^(-λt) + Σ(δ_i * u(t - t_i))
```

Where:
- `A_0` = initial agenda item count
- `λ` = decay constant (empirically: 0.15 items/minute)
- `δ_i` = impulse from unplanned topic injection at time `t_i`
- `u(t)` = Heaviside step function

**Observed Behavior**:
- At t=0: All agenda items present
- At t=10min: 50% of items still viable
- At t=30min: 10% of items still viable
- At t=60min: 0% (meeting has become a different meeting)

### 3.3 Decision Avoidance Index (DAI)

DAI measures the probability that a meeting concludes without
any binding decision:

```
DAI = 1 - Π(p_i)
```

Where `p_i` is the probability of deciding on item i, modeled as:

```
p_i = 1 / (1 + e^(k*(N - N_threshold)))
```

- `N` = number of attendees
- `N_threshold` = decision threshold (empirically: 5)
- `k` = sensitivity parameter (empirically: 0.8)

**DAI Interpretation**:
| DAI Range | Classification | Outcome |
|-----------|---------------|---------|
| 0.0 - 0.2 | Decisive | Decision made (rare) |
| 0.2 - 0.5 | Ambivalent | Decision deferred |
| 0.5 - 0.8 | Avoidant | "Let's discuss offline" |
| 0.8 - 1.0 | Paralyzed | "Let's schedule another meeting" |

### 3.4 Entropy Acceleration Mechanisms

MEAP identifies three primary entropy acceleration mechanisms:

**3.4.1 Laptop Drift**: Attendee attention migrates to laptop
screens. Acceleration factor: ×1.3 per laptop opened.

**3.4.2 Phone Check**: Attendee attention fragments via mobile
device. Acceleration factor: ×1.2 per phone checked.

**3.4.3 Side Conversation**: Parallel communication channels
form within the meeting. Acceleration factor: ×1.5 per side
conversation detected.

### 3.5 MEAP Packet Structure

MEAP introduces monitoring packets for meeting entropy tracking:

```
MEAP_SYN:
  type: "syn"
  meeting_id: string
  agenda_items: int
  attendees: int
  scheduled_duration: int

MEAP_DATA:
  type: "data"
  meeting_id: string
  t_elapsed: int
  agenda_remaining: int
  laptops_open: int
  phones_checked: int
  side_conversations: int
  adf_value: float

MEAP_FIN:
  type: "fin"
  meeting_id: string
  t_total: int
  decisions_made: int
  action_items_assigned: int
  action_items_completed: int  // always 0
  dai: float
  mdm: float
```

### 3.6 MEAP State Machine

```
Scheduled
  |
  v
Purposeful (< 5 min)
  |
  v
Drifting (5-15 min)
  |
  v
Entropy Zone (15-30 min)
  |
  v
Terminal (> 30 min)
  |
  v
Scheduling Next Meeting
```

## 4. Failure Modes

### 4.1 Meeting Ends on Time
Catastrophic success. MDM < 1.5. Attendees confused. Some
report feeling "short-changed." Probability: 5%.

### 4.2 No Agenda
ADF undefined. Meeting immediately enters Entropy Zone.
DAI approaches 1.0. Outcome: "Let's meet again with an agenda."

### 4.3 Too Many Attendees
MDM exceeds 5.0. DAI > 0.9. Meeting produces zero decisions
and three action items assigned to nobody. Probability: 40%.

### 4.4 Coffee Machine Proximity
Meeting room adjacent to coffee machine. CHP interrupts
meeting every 12 minutes. Entropy acceleration: ×2.0.

## 5. Security Considerations

### 5.1 Meeting Crasher
Unauthorized attendee increases MDM and DAI. Mitigation:
locked meeting rooms (increases hallway sync probability).

### 5.2 Agenda Hijacking
Attendee injects unplanned topic, accelerating ADF decay.
Mitigation: "Parking Lot" protocol (defer to future meeting
that will never happen).

## 6. Performance Evaluation

### 6.1 MEAP vs. No-MEAP

| Metric | No-MEAP | With MEAP |
|--------|---------|-----------|
| Avg MDM | 3.5 | 2.0 |
| Avg DAI | 0.75 | 0.40 |
| Decisions/Meeting | 0.3 | 1.2 |
| Action Items Completed | 0% | 5% |

### 6.2 Optimal Meeting Duration

```
T_optimal = T_minimum * MDM_target
```

Where `MDM_target` = 1.5 (50% overhead tolerance).

## 7. Extensions

| RFC | Title | Status |
|-----|-------|--------|
| 0014 | Consensus Theater Choreography | Planned |
| 0015 | Distributed Ignorance Management | Planned |
| 0020 | Lunch Table Seating Optimization | Planned |

## 8. References

### 8.1 Normative References

[RFC-0004] Matos, R. "Decision Theater Specification (DTS)." RFC 0004, OSC, 1991.

[RFC-0014] Matos, R. "Consensus Theater Choreography." RFC 0014, OSC, 2026.

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017, OSC, 2001.

### 8.2 Informative References

Parkinson, Cyril Northcote. 1955. "Parkinson's Law." *The Economist*, November 19.

Brooks, Frederick P. 1975. *The Mythical Man-Month*. Boston: Addison-Wesley.

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs published under the OSC imprint are satirical artifacts
> that encode genuine organizational science. The meeting, however, is real —
> and it could have been an email.
