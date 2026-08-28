---
rfc: "0017"
title: "Coffee-Break Protocol (CBP)"
stream: "Humor"
status: "DRAFT"
category: "Informational"
area: "informal-networks"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2001-04-01"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [1, 3, 8, 18]
keywords: [coffee, knowledge-sync, weak-ties, informal-networks, coordination, logistics]
abstract: |
  This document specifies the Coffee-Break Protocol (CBP), an informal,
  decentralized, eventually consistent synchronization protocol enabling
  spontaneous dissemination of tacit organizational knowledge. CBP introduces
  the Logistical Entropy Factor (LEF) for distance-weighted coordination, the
  Coffee Handshake Protocol (CHP) for peer-to-peer rendezvous, and the
  Visual Primitive for line-of-sight discovery. Experimental evidence
  suggests that organizations disabling CBP experience progressive epistemic
  fragmentation despite increases in formal communication mechanisms.
dual_layer: true
satire_notice: "satire"
---

# RFC-0017 — Coffee-Break Protocol (CBP)

## Abstract

This document specifies the Coffee-Break Protocol (CBP), an informal,
decentralized, eventually consistent synchronization protocol enabling
spontaneous dissemination of tacit organizational knowledge. CBP introduces
the Logistical Entropy Factor (LEF) for distance-weighted coordination, the
Coffee Handshake Protocol (CHP) for peer-to-peer rendezvous, and the
Visual Primitive for line-of-sight discovery. Experimental evidence
suggests that organizations disabling CBP experience progressive epistemic
fragmentation despite increases in formal communication mechanisms.

> **Satire Notice**: This document is published in the **Humor/Experimental** stream.
> While technically coherent, its primary purpose is satirical illumination
> of organizational dynamics. The OSC does not recommend deploying CBP
> in production without IRB approval and a very good coffee machine.

## 1. Introduction

Formal communication assumes knowledge can be scheduled. Organizations
repeatedly demonstrate that this assumption is false.

The majority of operational knowledge is exchanged through:

- accidental encounters;
- corridor conversations;
- coffee breaks;
- lunches;
- waiting for elevators.

CBP standardizes these interactions.

## 2. Terminology

| Term | Definition |
|------|------------|
| **Coffee Node** | A human currently holding a beverage. |
| **Idle Conversation** | Communication with no predefined agenda. |
| **Useful Information** | Information initially believed to be irrelevant. |
| **Coffee Machine** | A mandatory synchronization server. |
| **Espresso** | High-priority synchronization packet. |
| **Decaf** | Low-energy synchronization request. |
| **Logistical Entropy Factor (LEF)** | Distance-weighted coordination cost: LEF = α·d + β·f + γ·w + δ·s (see §3.4). |
| **Coffee Handshake Protocol (CHP)** | Peer-to-peer rendezvous protocol for synchronized coffee acquisition. |
| **Visual Primitive** | Line-of-sight discovery mechanism for Coffee Node detection. |
| **Synchronization Zone** | Physical radius around Coffee Machine where CHP operates (default: 5m). |
| **Cross-Floor Sync** | CHP variant for different floors/buildings (DCM: Distributed Coffee Mesh). |
| **SUSPICION Metric** | Manager perception risk when CHP frequency exceeds baseline (SUSPICION = frequency × duration / baseline). |

## 3. Protocol Specification

### 3.1 State Machine (Extended)

When two nodes carrying coffee meet:

```ascii
Idle
  |
  v
Coffee Acquisition (CHP_INIT)
  |
  v
Visual Discovery (VISUAL_PRIMITIVE)
  |
  v
CHP Handshake (CHP_SYN / CHP_ACK)
  |
  v
Synchronization Zone Entry
  |
  v
Mutual Complaining (PAYLOAD_PREAMBLE)
  |
  v
Knowledge Exchange (PAYLOAD_CORE)
  |
  v
Idea Generation (PAYLOAD_POSTAMBLE)
  |
  v
Implementation
  |
  v
Repeat
```

### 3.2 Coffee Handshake Protocol (CHP)

CHP is the rendezvous sub-protocol enabling two Coffee Nodes to synchronize
arrival at a Synchronization Zone. Modeled on TCP three-way handshake:

```ascii
CHP_SYN  (Visual Primitive or Explicit: "Coffee?")
    |
    v
CHP_SYN_ACK (Nod / "Two mins" / "At the 3rd floor machine")
    |
    v
CHP_ACK (Visual Primitive or "On my way")
    |
    v
SYNC_ESTABLISHED
```

**CHP Parameters**:
- `timeout`: 120 seconds (configurable; shorter for Espresso, longer for Decaf)
- `retries`: 2 (after which node falls back to Solo Acquisition)
- `visual_timeout`: 5 seconds (Visual Primitive must be acknowledged)

**CHP Variants**:
| Variant | Trigger | Timeout | Priority |
|---------|---------|---------|----------|
| **Explicit CHP** | Verbal/Slack: "Coffee?" | 120s | Normal |
| **Visual CHP** | Eye contact + mug gesture | 5s (visual_timeout) | High |
| **Scheduled CHP** | Recurring calendar invite | N/A | Low |
| **Emergency CHP** | "Production down" / "Need help" | 30s | Critical |
| **Listen-Only CHP** | Executive with ECI ≥ 10 (RFC-0001) | N/A | Lowest |

**Listen-Only CHP** (RFC-0001 §5.3): Executive with ECI ≥ 10 attends
CBP session without initiating CHP handshakes. They observe Visual
Primitives, receive CHP packets passively, but do not initiate CHP_SYN
or respond with CHP_SYN_ACK. This preserves CBP's psychological safety
while allowing ECI reduction through passive synchronization.

### 3.3 Packet Structure (Extended)

The CBP synchronization packet encapsulates the true payload within
social lubricant (RFC-0017 §3.2), with explicit framing:

```ascii
+---------------------------+
| CHP Header (Visual/Explicit) |
+---------------------------+
| Weather / Small Talk      |  ← Synchronization Preamble (α)
+---------------------------+
| Family / Personal         |  ← Trust Establishment (β)
+---------------------------+
| Small Complaint           |  ← Psychological Safety Signal (γ)
+---------------------------+
| **Actual Problem**        |  ← PAYLOAD CORE: Operational Knowledge (δ)
+---------------------------+
| **Hidden Solution**       |  ← PAYLOAD CORE: Tacit Insight (ε)
+---------------------------+
| Weekend Plans             |  ← Synchronization Postamble (ζ)
+---------------------------+
| CHP Trailer (Visual/Explicit) |
+---------------------------+
```

**Frame Check Sequence (FCS)**: Mutual Complaining checksum — both nodes
must complain about something for payload acceptance (FCS = complaint_A ∧ complaint_B).

### 3.4 Logistical Entropy Factor (LEF)

LEF quantifies the coordination cost between two Coffee Nodes based on
physical, organizational, and temporal distance:

```
LEF = α·d + β·f + γ·w + δ·s
```

Where:
- `d` = Physical distance (meters; Euclidean for same floor, Manhattan for multi-floor)
- `f` = Floor differential (0 = same floor, 1 = adjacent, 2+ = elevator required)
- `w` = Workload differential (0 = both idle, 1 = both busy, 0.5 = asymmetric)
- `s` = Schedule misalignment (0 = aligned calendars, 1 = no overlap)

**Default Coefficients** (empirically calibrated):
- `α = 0.02` (per meter)
- `β = 0.15` (per floor)
- `γ = 0.25` (workload asymmetry penalty)
- `δ = 0.10` (schedule misalignment penalty)

**LEF Thresholds**:
| LEF Range | Classification | CHP Behavior |
|-----------|----------------|--------------|
| LEF ≤ 0.3 | **Proximity Sync** | Visual CHP sufficient |
| 0.3 < LEF ≤ 0.6 | **Moderate** | Explicit CHP required |
| 0.6 < LEF ≤ 1.0 | **Significant** | Scheduled CHP recommended |
| LEF > 1.0 | **Prohibitive** | DCM (Cross-floor) or VCP required |

**Personality/Workload Modifiers** (multiplicative):
| Factor | Modifier | Description |
|--------|----------|-------------|
| **Introvert Node** | ×1.3 | Higher CHP initiation threshold |
| **High Workload** | ×1.5 | Reduced Visual Primitive sensitivity |
| **Smoker/Excuse Carrier** | ×0.7 | Built-in rendezvous excuse |
| **Manager Proximity** | ×2.0 | LEF doubles if manager within 5m |

### 3.5 Visual Primitive

The Visual Primitive is a zero-latency discovery mechanism for Coffee Node
detection within Synchronization Zone:

**Requirements**:
- Line of Sight (LoS) between nodes
- Both nodes holding beverage containers
- Mutual gaze duration ≥ 500ms

**Protocol**:
```ascii
Node A: [gazes] → [raises mug slightly] → [holds 500ms]
    ↓
Node B: [detects] → [nods] → [raises mug] → [holds 500ms]
    ↓
CHP_SYN_ACK implicit
```

**Failure Modes**:
| Failure | Cause | Fallback |
|---------|-------|----------|
| LoS obstructed | Wall, monitor, colleague | Explicit CHP |
| Mug not visible | Hand position, no mug | Explicit CHP |
| Gaze < 500ms | Distraction, shyness | Explicit CHP |
| Manager in LoS | Manager within LoS cone | ABORT (switch to weather) |

### 3.6 Cross-Floor Synchronization (DCM)

For nodes on different floors/buildings, CBP uses Distributed Coffee Mesh (DCM):

**DCM Protocol**:
1. Node initiates CHP with `floor` parameter
2. CHP_SYN_ACK includes `floor`, `machine_id`, `eta`
3. Nodes converge on designated machine (pre-negotiated or nearest)
4. `LEF` recalculated with `f = floor_differential`

**DCM Latency Budget**:
| Scenario | Max Latency | Success Rate |
|----------|-------------|--------------|
| Adjacent floors | 8 min | 85% |
| Building-to-building | 15 min | 70% |
| Campus (shuttle) | 25 min | 50% |

### 3.6 Personality & Workload Factors

CBP adapts to node characteristics via LEF modifiers:

| Node Type | CHP Initiation Probability | Visual Primitive Sensitivity | Preferred Variant |
|-----------|---------------------------|------------------------------|-------------------|
| **Introvert** | Low (p=0.3) | Low (0.6×) | Scheduled CHP |
| **Extrovert** | High (p=0.8) | High (1.2×) | Visual CHP |
| **High Workload** | Medium (p=0.5) | Reduced (0.6×) | Scheduled/Explicit |
| **Smoker/Excuse** | High (p=0.9) | Normal | Explicit (excuse built-in) |
| **Manager** | Very Low (p=0.1) | Very Low | Never initiates |

**Workload Asymmetry Protocol**: When `w > 0.5` (asymmetric workload),
the less-busy node MUST initiate CHP. The busier node signals availability
via Visual Primitive only.

### 3.7 SUSPICION Metric & Manager Avoidance

`SUSPICION = (chp_frequency × avg_duration) / max(baseline_frequency, 1)`

- `SUSPICION > 1.5`: Manager perceives "excessive coffee"
- `SUSPICION > 2.0`: Automatic CHP suppression for 60 min
- **Countermeasure**: Ceremonial Decaf (CHP with `type=decaf`,
  `priority=low`) resets `SUSPICION` without knowledge transfer.

**Manager Proximity Detection**: Visual Primitive includes Manager
Cone Check (5m radius, 60° cone). If detected:
- Immediate CHP_ABORT
- Payload replaced with weather/sports
- `SUSPICION` decay rate doubled for 10 min

---

## 3.8 Conference Coffee-Break Protocol (CCBP)

### 3.8.1 Motivation

The office CHP assumes fixed topology: known colleagues, recurring
proximity, shared calendar. Conferences break all three assumptions.
800 strangers, multi-track schedules, 3-day window. The window closes
before organic coffee-break discovery finishes warming up.

CCBP extends the office CHP with:
- **Interest-based matching**: TF-IDF + cosine similarity on
  research interests, replacing random encounter.
- **Real-time coordination**: Geofencing + WebSocket + availability
  state machine for synchronous meetups.
- **Pre/during/post lifecycle**: Preparation before the conference,
  coordination during, follow-up after.
- **GDPR-compliant privacy**: Opt-in visibility levels, CBP data
  exemption, 30-day auto-delete, right to erasure.

CCBP is protocol-compatible with office CHP. The same CHPSYN,
CHP_SYN_ACK, CHP_DATA, CHP_FIN, CHP_ABORT packets flow.
Conference context adds fields to the payload; the handshake
does not change.

### 3.8.2 Terminology

| Term | Definition |
|------|-----------|
| **Conference** | Time-bounded event with fixed attendee list |
| **Track** | Thematic sub-schedule within a conference |
| **Interest Fingerprint** | TF-IDF vector derived from user profile |
| **Matching Score** | Cosine similarity between two fingerprints |
| **Availability State** | Machine state: AVAILABLE, IN_SESSION, IN_MEETING, IN_TRANSIT, OFFLINE |
| **Geofence** | GPS radius trigger (default 50m) around venue zones |
| **CBP Window** | 10-minute gap between sessions designated for coffee-break |

### 3.8.3 Lifecycle

CCBP operates in three phases:

**Phase 0 — Pre-Conference (T-14d to T-0)**:
- User registers interest fingerprint (research topics, methods,
  open questions).
- Matching engine computes pairwise scores for all attendees.
- System suggests top-5 matches per attendee with confidence %.
- User accepts/declines/requeues suggestions.
- Calendar integration: system maps session schedule to availability
  windows.

**Phase 1 — During Conference (T-0 to T+3d)**:
- Real-time availability tracking via geofence + calendar.
- Matching engine runs on-demand when two users are simultaneously
  AVAILABLE and within geofence range.
- CHP handshake initiates automatically (both users opted in).
- Visual Primitive: conference badge flash (NFC/QR) replaces
  the office hand-wave.

**Phase 2 — Post-Conference (T+3d to T+30d)**:
- Follow-up CHP packets for connection maintenance.
- Interest fingerprints archived (anonymized after 30 days).
- Contact exchange: mutual opt-in required for email/LinkedIn.
- Feedback loop: match quality rating feeds back into engine.

### 3.8.4 Interest Fingerprint

Each attendee builds a fingerprint vector at registration:

```
Input:  user profile (bio, publications, talks, keywords)
Process: TF-IDF vectorization (top 200 terms)
Output: sparse vector V ∈ ℝ^200
```

**Fingerprint sources (weighted)**:
| Source | Weight | Notes |
|--------|--------|-------|
| Bio / abstract | 0.35 | Self-authored |
| Publication titles | 0.30 | DBLP/Scholar lookup |
| Talk titles | 0.20 | Conference submission |
| Keywords (manual) | 0.15 | User-supplied tags |

**Matching Score** between users A and B:

```
score(A, B) = cosine(V_A, V_B)
```

**Threshold**: `score >= 0.4` triggers suggestion. Scores below 0.4
are not surfaced (low-signal noise).

### 3.8.5 Matching Engine

The matching engine uses a weighted composite score adapted from
conference networking research:

```
session_score  = 0.45 * schedule_overlap(A, B)
feedback_score = 0.35 * past_interaction_quality(A, B)
profile_score  = 0.20 * cosine(V_A, V_B)
```

**Session score**: Fraction of concurrent session attendance.
Computed from accepted schedule (Phase 0).

**Feedback score**: Prior interaction quality from past conferences
(cold-start = 0.5 neutral). Only available for returning attendees.

**Profile score**: Cosine similarity on interest fingerprints.

For first-time conference attendees (no history), the engine
falls back to:

```
session_score  = 0.60 * schedule_overlap(A, B)
profile_score  = 0.40 * cosine(V_A, V_B)
```

This weights schedule proximity higher when behavioral data
is unavailable.

### 3.8.6 CCBP State Machine

Conference attendees operate under a richer availability model
than the office CHP:

```
         ┌─────────────────────────────────────────┐
         │                                         │
         ▼                                         │
    ┌──────────┐   geofence_enter   ┌──────────┐   │
    │ OFFLINE  │ ─────────────────► │AVAILABLE │   │
    └──────────┘                    └──────────┘   │
         ▲                         │  ▲   │       │
         │  geofence_exit          │  │   │       │
         │◄────────────────────────┘  │   │session│
         │                            │   │start  │
         │   session_start            │   ▼       │
         │◄───────────────────────────┼───────────┤
         │                            │IN_SESSION │
         │                            └───────────┘
         │                            │  │
         │   session_end              │  │session
         │◄───────────────────────────┘  │end
         │                               ▼
         │                         ┌──────────────┐
         │                         │  IN_TRANSIT  │
         │                         └──────────────┘
         │                            │
         │   meeting_start            │
         │◄───────────────────────────┘
         │                            │
         │   meeting_end              │
         │◄───────────────────────────┘
         │
    IN_MEETING (for scheduled 1:1 CBP)
```

**State transitions**:
| From | To | Trigger |
|------|----|---------|
| OFFLINE | AVAILABLE | Geofence enter + user opt-in |
| AVAILABLE | IN_SESSION | Session start (calendar) |
| AVAILABLE | IN_TRANSIT | Walking between venues |
| AVAILABLE | IN_MEETING | Scheduled CHP match |
| IN_SESSION | AVAILABLE | Session end |
| IN_TRANSIT | AVAILABLE | Arrive at coffee zone |
| IN_MEETING | AVAILABLE | CHP_FIN or timeout |
| ANY | OFFLINE | Geofence exit or manual |

### 3.8.7 Real-Time Coordination Layer

**Architecture**: WebSocket server + geofence service + Redis pub/sub.

**Geofence service**:
- GPS ping every 30s (battery-optimized).
- 50m radius around venue zones (lobbies, coffee areas, poster halls).
- Entry/exit events published to Redis channel `geofence:{conference_id}`.

**WebSocket messages**:
| Message | Direction | Payload |
|---------|-----------|---------|
| `availability_update` | Client→Server | state, lat, lon |
| `match_found` | Server→Client | peer_id, score, suggested_zone |
| `chp_initiate` | Server→Both | CHP_SYN with match metadata |
| `zone_crowd_update` | Server→Client | zone_id, headcount, avg_availability |

**Match trigger**:
1. User A enters AVAILABLE state.
2. Server queries matching engine for A's top matches also in
   AVAILABLE state within geofence range.
3. If `score >= 0.4` and both users opted in: emit `match_found`.
4. Either user can initiate CHP_SYN via badge flash or app tap.
5. If no action within 5 minutes: match expires, scored down
   for future suggestions.

### 3.8.8 GDPR Privacy Model

Conference CCBP processes personal data (location, interests,
schedule). GDPR compliance requires explicit controls.

**Legal basis**: Consent (Art. 6(1)(a)). User opts in at
registration. Opt-out withdraws consent immediately.

**Visibility levels**:
| Level | Who sees you | Location shared | Interests shared |
|-------|-------------|-----------------|-------------------|
| INVISIBLE | Nobody | Never | Never |
| MATCHES_ONLY | Top-5 matches only | During CBP window | Fingerprint only |
| PUBLIC | All attendees | During CBP window | Fingerprint only |

Default: `MATCHES_ONLY`. Users must explicitly choose PUBLIC.

**CBP data exemption**: Coffee-break encounters are transient.
No persistent record of physical proximity is stored.
Only the match score and mutual feedback persist.

**Data retention**:
| Data | Retention | Action after |
|------|-----------|-------------|
| Interest fingerprint | 30 days post-conference | Auto-delete |
| Match scores | 30 days post-conference | Auto-delete |
| Feedback ratings | 30 days post-conference | Anonymize |
| Contact exchange | Until user erases | On-demand delete |
| Geofence logs | 7 days | Auto-delete |

**Right to erasure**: User can request full deletion at any time.
System removes fingerprint, scores, logs within 24 hours.

**Data processor**: Conference organizer acts as data processor.
Meet-a-peer infrastructure acts as sub-processor.
DPA (Data Processing Agreement) required between both.

### 3.8.9 CCBP Packet Format

CCBP extends office CHP packets with conference-specific fields:

```
CCBP_CHP_SYN:
  type: "syn"
  conference_id: string
  attendee_id: string (anonymized hash)
  fingerprint_version: "tfidf-v1"
  availability_state: AvailabilityState
  geofence_zone: string | null
  suggested_match_score: float | null
  suggested_peer_id: string | null

CCBP_CHP_SYN_ACK:
  type: "syn_ack"
  conference_id: string
  attendee_id: string
  availability_state: AvailabilityState
  match_confirmed: boolean
  zone_agreed: string | null

CCBP_CHP_DATA:
  type: "data"
  conference_id: string
  attendee_id: string
  payload: {
    topic_interests: string[],
    open_questions: string[],
    available_duration_minutes: int,
    contact_exchange_willing: boolean  // mutual opt-in
  }

CCBP_CHP_FIN:
  type: "fin"
  conference_id: string
  attendee_id: string
  interaction_quality: 1-5  // feedback score
  follow_up_willing: boolean
```

### 3.8.10 Failure Modes (Conference-Specific)

**3.8.10.1 Geofence Drift**: GPS inaccuracy in indoor venues.
Mitigation: Bluetooth beacon augmentation at zone boundaries.

**3.8.10.2 Schedule Chaos**: Sessions run over, rooms change.
Mitigation: Calendar sync with conference API (if available).
Fallback: manual availability override.

**3.8.10.3 Matching Cold Start**: First-time attendees with thin
profiles. Mitigation: weighted schedule overlap (0.60/0.40 split).

**3.8.10.4 Language Barrier**: Multi-disciplinary conferences
with non-native speakers. Mitigation: language preference in
fingerprint, boost same-language matches.

**3.8.10.5 GDPR Non-Compliance Risk**: Organizer fails to
execute DPA. Mitigation: system refuses to activate CCBP
until DPA is confirmed in registry.

**3.8.10.6 Badge Flash Failure**: NFC/QR scanning fails.
Mitigation: manual match confirmation via app.

### 3.8.11 Performance Evaluation

**Metrics**:
| Metric | Target | Notes |
|--------|--------|-------|
| Match latency | < 2s | From geofence entry to suggestion |
| Match quality | >= 0.5 avg cosine | Post-interaction feedback |
| Attendance conversion | >= 30% | Of suggested matches that meet |
| GDPR compliance | 100% | No data without consent |
| Battery drain | < 5%/day | GPS + WebSocket combined |

**Evaluation protocol**: A/B test between random encounter
(baseline) and CCBP matching (treatment) at Conference Alpha 2027.

### 3.8.12 Extensions

**3.8.12.1 Group CBP**: Match triads or quads for panel-style
coffee breaks. Requires 3-way match score >= 0.4.

**3.8.12.2 Mentorship Mode**: Senior attendees opt in as mentors.
Matching engine boosts mentor-mentee pairs (career stage signal).

**3.8.12.3 Sponsor Integration**: Sponsors can opt in to match
with attendees interested in their technology. Separate consent
layer. Never overrides attendee-to-attendee matches.

**3.8.12.4 Cross-Conference Continuity**: Carry fingerprint
and feedback history across conference series (Alpha, Beta,
Gamma). Requires unified identity (RFC-0022).

### 3.8.13 Conference Series Context

Many conference organizers run multiple events sharing identical
structure (e.g., three annual conferences on education/technology).
Each conference: ~800 attendees, multi-track, 3-day format.
Shared registration platform enables cross-conference identity.

**CCBP integration points**:
1. Opt-in consent at series registration (pre-filled forms may
   suggest but not pre-approve).
2. Session schedule imported from series program API.
3. Badge printing includes NFC tag for CCBP handshake.
4. Post-conference: email summary of matches + follow-up links.

### 3.8.14 Integration with Office CHP

CCBP and office CHP share the same packet structure.
A user can carry their fingerprint from conference to office:

```
Conference CCBP ──(fingerprint transfer)──► Office CHP
Office CHP ──(feedback history)──► Conference CCBP
```

The matching engine adapts weights based on context:
- Office: higher weight on schedule overlap (daily proximity)
- Conference: higher weight on interest similarity (novelty)

### 3.8.15 Security Considerations

**3.8.15.1 Fingerprint Spoofing**: User could submit misleading
profile to manipulate matches. Mitigation: publication-based
fingerprint components are verified against DBLP.

**3.8.15.2 Location Tracking**: GPS data could be misused.
Mitigation: geofence logs deleted after 7 days. No continuous
tracking outside conference venue boundaries.

**3.8.15.3 Man-in-the-Middle on WebSocket**: TLS 1.3 required.
Certificate pinning for mobile app.

**3.8.15.4 Replay Attacks**: CHP packets include conference_id
and timestamp. Replay window: 5 minutes.

### 3.8.16 Open Questions

1. How to handle attendees who decline all suggestions but
   want to be discoverable? (INVISIBLE vs MATCHES_ONLY tradeoff)
2. Should match scores be transparent to both parties?
3. How to handle conference organizers who refuse DPA?
4. Optimal geofence radius for indoor venues with poor GPS?

### 3.8.17 References

- meet-a-peer: conference networking platform reference
- GDPR Art. 6(1)(a): Consent as legal basis
- RFC-0022: Cross-Conference Identity
- RFC-0017 §3.1: Office CHP Handshake

### 3.9 Safe-Space Design

The Coffee-Break Protocol assumes a venue that can carry candid
knowledge. This section specifies the conditions that make a coffee
break a safe space. These conditions are properties of the venue and
its habits, not of any single session.

#### 3.9.1 Use by Motivation, Not Decree

A coffee break is safe when people come because it is useful, not
because it is required. Decreed attendance converts the venue into a
stage: the knowledge that mattered stops being spoken (Edmondson 1999).
CBP venues SHALL be sustained by motivation of use, never by mandate.

#### 3.9.2 Continuity

Single events are inconsequential. Candid knowledge emerges only after
repeated encounters establish that the venue is safe. A coffee break
that occurs once per quarter carries no knowledge; a coffee break that
occurs daily carries the organization's real topology. Regularity is a
precondition of the channel.

#### 3.9.3 Group Size Threshold

Small groups sustain flow; crowds produce social anxiety and silence.
The threshold is not fixed: it depends on the group's shared history.
A venue that exceeds the size its regulars can track SHALL be split
rather than enlarged. A crowd is not a coffee break; it is a
conference.

#### 3.9.4 Minimum Trust Law

The trust that a group can converse in equals the trust of its least
trusting member, minus a small discount for residual risk:

    T_conversable = T_least_trusting - delta

One distrustful or exposed participant degrades the space for all. The
law has two operational consequences: (a) the presence of management
(or anyone whose attendance reads as surveillance) lowers T_conversable
toward zero; (b) protection of the least-trusting member is the whole
group's interest, not the shy member's problem.

#### 3.9.5 Shy and Anti-Social Accommodation

Participants who do not initiate speech SHALL be accommodated in an
observation mode, consistent with Listen-Only CHP (§3.2). Observation
is a legitimate participation mode, not a failure to participate. The
venue SHALL permit passive presence without requiring contribution.

#### 3.9.6 Anti-Open-Space

The coffee break is a protected space. It SHALL NOT be co-located with
or absorbed into open-office or open-space events, where proximity
theater and visible hierarchy suppress candid exchange (Richardson
et al. 2017; Morrison & Smollan 2020). If an open-space event claims
the venue, the coffee break moves or dies.

#### 3.9.7 Relationship to Listen-Only CHP

Safe-space conditions are prerequisites for Listen-Only CHP (§3.2).
An executive attending Listen-Only exercises the observation mode of
§3.9.5 and inherits the Minimum Trust Law of §3.9.4: their presence
lowers T_conversable unless the group already trusts that they will
not act on what they hear. The executive does not get a safe space by
attending; the group grants it by trusting.

#### 3.9.8 Non-Exploitation Condition

The Minimum Trust Law (§3.9.4) has an economic consequence: a participant
whose value is extracted without fair return is a least-trusting member.
The broker who carries the space's knowledge — and is paid only in
ceremony — does not trust the space; they have learned what it costs them.
One such member degrades T_conversable for all (Compensation Justice;
RFC-0035 Rule ESP-6; Recognition Theater is the failure mode this
condition forbids).

A venue is safe only when the people who sustain it are not exploited.
Non-Capture forbids formalizing the connector's role; it never forbids —
and safety requires — paying fairly for the value the connector creates.
The pat on the back is not compensation. Compensation is the condition
that keeps the least-trusting member from being the one carrying the
space on their back.

---

## 4. Failure Modes (Extended)

### 4.1 Coffee Machine Removed
Catastrophic failure. Knowledge islands begin appearing. `LEF` → ∞ for all node pairs.

### 4.2 Capsule Coffee Machine
Synchronization latency increases. `LEF` multiplier ×1.5 (capsule wait time).

### 4.3 Remote Work
Requires Virtual Coffee Protocol (VCP).

Known limitations:
- awkward silence (no Visual Primitive)
- microphone muted (no CHP_SYN_ACK)
- "I have another meeting" (CHP timeout)

### 4.4 Personality Mismatch
Introvert-Extrovert pairs: CHP initiation deadlock.
**Mitigation**: Scheduled CHP enforced by calendar.

### 4.5 Manager Proximity
Manager within 5m → LEF ×2.0, Visual Primitive disabled, CHP_ABORT triggered.

---

## 5. Security Considerations (Extended)

### 5.1 Managers Joining Conversations
Observed consequence: Conversation immediately switches to weather.
**Protocol Response**: Automatic payload replacement with weather/sports.

### 5.2 SUSPICION Exploitation
Adversarial nodes may flood CHP to raise target's `SUSPICION`.
**Mitigation**: Rate limiting (max 3 CHP/hour per node pair).

### 5.3 Visual Primitive Spoofing
Adversary mimics Visual Primitive to trigger CHP_SYN_ACK.
**Mitigation**: Mug verification (must hold actual beverage container).

### 5.4 CHP over Slack/Teams
Explicit CHP via chat leaks intent to surveillance.
**Mitigation**: Encrypted CHP (Signal/Threema) or coded language ("[coffee]?").

---

## 6. Performance Evaluation (Extended)

### 6.1 CHP Overhead Analysis

| Phase | Avg Latency | Success Rate |
|-------|-------------|--------------|
| Visual Primitive | < 5 sec | 90% (if LoS) |
| Explicit CHP_SYN → SYN_ACK | 30–60 sec | 85% |
| CHP_SYN_ACK → CHP_ACK | 10–30 sec | 95% |
| DCM (Cross-floor) | 8–15 min | 70% |

### 6.2 Knowledge Payload vs. Coordination Cost

| Sync Type | Payload (bits) | Coordination Cost | Efficiency |
|-----------|----------------|-------------------|------------|
| Visual (LoS) | ~500 | Near-zero | ***** |
| Explicit CHP | ~500 | 2–5 min | **** |
| DCM | ~500 | 10–20 min | *** |
| VCP (Remote) | ~300 | 5–10 min | ** |

### 6.3 LEF Distribution in Typical Org

| LEF Range | % of Node Pairs | Dominant CHP Variant |
|-----------|-----------------|----------------------|
| ≤ 0.3 | 35% | Visual |
| 0.3–0.6 | 40% | Explicit |
| 0.6–1.0 | 20% | Scheduled |
| > 1.0 | 5% | DCM/VCP |

---

## 7. Extensions (Extended)

| RFC | Title | Status |
|-----|-------|--------|
| 0018 | Watercooler Gossip Verification Protocol | Planned |
| 0019 | Hallway Discovery Protocol | Planned |
| 0020 | Elevator Consensus Algorithm | Planned |
| 0021 | Beer-Based Distributed Decision Making | Experimental |
| 0022 | Virtual Coffee Protocol (VCP) | Planned |
| 0023 | Distributed Coffee Mesh (DCM) | Planned |
| 0024 | Coffee Handshake Protocol (CHP) | Planned |

---

## 8. References (Extended)

### 8.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001, OSC, 1987.
https://rfc.osc.org/rfc0001

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003, OSC, 1992.
https://rfc.osc.org/rfc0003

[RFC-0008] Matos, R. "Tacit Knowledge Extraction Protocol (DEPRECATED)." RFC 0008, OSC, 1995.
https://rfc.osc.org/rfc0008

[RFC-0018] Matos, R. "Watercooler Gossip Verification Protocol." RFC 0018, OSC, 2026.
https://rfc.osc.org/rfc0018

### 8.2 Informative References

Granovetter, Mark S. 1973. "The Strength of Weak Ties." *American
Journal of Sociology* 78 (6): 1360–1380.
https://doi.org/10.1086/225469

Nonaka, Ikujiro, and Hirotaka Takeuchi. 1995. *The Knowledge-Creating
Company: How Japanese Companies Create the Dynamics of Innovation*.
New York: Oxford University Press.

Wenger, Etienne. 1998. *Communities of Practice: Learning, Meaning,
and Identity*. Cambridge: Cambridge University Press.

Edmondson, Amy C. 1999. "Psychological Safety and Learning Behavior in
Work Teams." *Administrative Science Quarterly* 44 (2): 350–383.
https://doi.org/10.2307/2666999

Postel, Jon. 1981. "Transmission Control Protocol." RFC 793. IETF.

Waber, Ben, Jennifer Magnolfi, and Greg Lindsay. 2014. "Workspaces
That Move People." *Harvard Business Review* 92 (10): 68–77.

Rashid, Awais, et al. 2006. "Social Network Analysis of a Corporate
Coffee Break." *Proc. CSCW*: 247–256.
https://doi.org/10.1145/1180875.1180914 `[UNVERIFIED — DOI resolves to Nomura et al., different
paper]`

Pentland, Alex. 2014. *Social Physics: How Good Ideas Spread*.
Penguin Press.

Richardson, Amy, et al. 2017. "Office Design and Health: A
Systematic Review." *The New Zealand Medical Journal* 130 (1467):
39-49.

Morrison, Rachel L., and Roy K. Smollan. 2020. "Open Plan Office
Space? If You're Going to Do It, Do It Right: A Fourteen-Month
Longitudinal Case Study." *Applied Ergonomics* 82: 102933.
https://doi.org/10.1016/j.apergo.2019.102933

---

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2001-04-01 | R. Matos | Initial April Fools publication |
| 0.2 | 2024-01-20 | R. Matos | Theorem-001 integration |
| 1.0 | 2026-07-18 | Rodolfo Matos | OEP canon alignment; dual-layer notice |
| 2.0 | 2026-07-19 | Rodolfo Matos | CHP, LEF, Visual Primitive, DCM, SUSPICION, Personality factors |
| 2.1 | 2026-08-07 | Rodolfo Matos | Added §3.9.8 Non-Exploitation Condition: the Minimum Trust Law makes exploitation a safety violation, not a fairness complaint (Compensation Justice; RFC-0035 Rule ESP-6) — T084 |

## Appendix B: Open Issues (Extended)

1. **VCP Specification**: Virtual Coffee Protocol for remote work needs full RFC (see RFC-0022).
2. **Coffee Quality Variable**: Does bean origin affect synchronization fidelity? [UNVERIFIED]
3. **Manager Detection Algorithm**: Can CBP nodes detect approaching
managers before conversation degradation? [UNVERIFIED]
4. **LEF Calibration**: Empirical validation of α, β, γ, δ coefficients across org types.
5. **EV Rotation Algorithm**: Optimal EV rotation strategy to minimize `SUSPICION`.
6. **Cross-Cultural LEF**: High-power-distance cultures may have different α, β, γ, δ.
7. **CHP over Slack/Teams**: Formalizing async CHP primitives for remote/hybrid.
8. **DCM Routing Protocol**: Optimal machine selection for cross-floor sync.
9. **SUSPICION Decay Function**: Optimal decay rate for `SUSPICION` decay.

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Wenger, Granovetter, Nonaka, Edmondson, Simon,
> Conway, Postel, Pentland, etc.) are accurate. The coffee machine, however, is
> real — and it is currently synchronizing more knowledge than this repository
> ever will.