---
rfc: "0019"
title: "Elevator Pitch Bandwidth Allocation"
stream: "Experimental"
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
see_also: [17, 20]
keywords: [elevator, pitch, bandwidth, allocation, 30-seconds, compression]
abstract: |
  This document specifies the Elevator Pitch Bandwidth Allocation
  (EPBA) protocol, a formal model for optimizing information
  transfer within bandwidth-constrained verbal channels. EPBA
  introduces the Pitch Compression Ratio (PCR), the Attention
  Bandwidth Allocation (ABA) model, the Interruption Probability
  Model (IPM), and the Elevator Floor Algorithm (EFA). The core
  constraint: elevator pitches operate within a 30-second window
  where every word competes for finite bandwidth.
dual_layer: true
satire_notice: "satire"
---

# RFC-0019 -- Elevator Pitch Bandwidth Allocation (EPBA)

## 1. Introduction

Formal communication assumes unlimited channel capacity.
Elevators demonstrate the opposite: a shared, bandwidth-limited,
broadcast channel with unpredictable duration and mandatory
co-presence. Every organizational role contains information that
must transfer within the elevator ride. The challenge is not what
to say, but how much fits through a 30-second channel before the
doors open.

EPBA addresses four problems:
- How much information fits in 30 seconds? (PCR)
- How does the listener allocate attention? (ABA)
- What is the probability of interruption? (IPM)
- How does floor count affect pitch duration? (EFA)

## 2. Terminology

| Term | Definition |
|------|------------|
| **Pitch** | Compressed verbal message transmitted during a ride. |
| **Pitcher** | Node initiating information transfer. |
| **Pitchee** | Node receiving the pitch. |
| **PCR** | Pitch Compression Ratio -- bits per 30 seconds. |
| **ABA** | Attention Bandwidth Allocation -- cognitive partitioning. |
| **IPM** | Interruption Probability Model -- termination likelihood. |
| **EFA** | Elevator Floor Algorithm -- duration from floor count. |
| **Channel** | Physical elevator cabin, shared by all nodes present. |

## 3. Protocol Specification

### 3.1 Pitch Compression Ratio (PCR)

```
PCR = (W_meaningful * log2(V)) / T_max
```

`W_meaningful` = words carrying information. `V` = vocabulary
size in bits per word. `T_max` = 30 seconds.

| PCR (bits/sec) | Classification | Example |
|-----------------|----------------|---------|
| > 8.0 | Dense | "Series A closed, $12M, need backend lead." |
| 4.0 -- 8.0 | Normal | "We shipped the feature, metrics look strong." |
| 1.0 -- 4.0 | Sparse | "Working on the new project, going well." |
| < 1.0 | Noise | "Hey, nice weather." |

Every social lubricant word (greeting, filler, hedge) reduces PCR
by 0.3 bits/sec. Starting with "Hey, so, um" costs 0.9 bits/sec
before content begins.

### 3.2 Attention Bandwidth Allocation (ABA)
```
ABA(pitch) = A_total * (1 - sum(ABA_distraction_i))
```
`A_total` = total listener attention (normalized: 1.0).

| Distraction | ABA_cost | Notes |
|-------------|----------|-------|
| Phone notification | 0.15 | Even if not checked |
| Mental to-do list | 0.20 | Default internal noise |
| Floor indicator watching | 0.30 | Anticipating exit |
| Other passenger | 0.40 | Shared channel contention |
| Manager presence | 0.60 | Dominant channel capture |

Effective bandwidth: `BW_effective = PCR * ABA(pitch)`.
A PCR of 6.0 with ABA = 0.3 yields only 1.8 bits/sec.

### 3.3 Interruption Probability Model (IPM)
```
IPM(t) = 1 - e^(-lambda * t)
```
`lambda` = lambda_base + lambda_floors + lambda_social.

| Source | lambda | Mean Time to Interruption |
|--------|--------|--------------------------|
| Floor stops (other) | 0.05 | 20 sec |
| Destination floor | 0.10 | 10 sec |
| Phone call (pitchee) | 0.03 | 33 sec |
| Social obligation | 0.01 | 100 sec |

| Elapsed (sec) | IPM (single floor) | IPM (3-floor ride) |
|---------------|--------------------|--------------------|
| 5 | 0.22 | 0.45 |
| 10 | 0.39 | 0.70 |
| 20 | 0.63 | 0.92 |
| 30 | 0.78 | 0.98 |

A 3-floor ride has 98% interruption probability by 30 seconds.

### 3.4 Elevator Floor Algorithm (EFA)
```
EFA(floors, stops) = T_floor * (floors - stops) - T_margin
```
`T_floor` = 4 seconds. `T_margin` = 3 seconds (door buffer).

| EFA Duration | Phase 1 (Hook) | Phase 2 (Core) | Phase 3 (Close) |
|--------------|----------------|-----------------|------------------|
| 25-30 sec | 5 sec | 18 sec | 5 sec |
| 15-25 sec | 3 sec | 10 sec | 4 sec |
| 8-15 sec | 2 sec | 5 sec | 2 sec |
| < 8 sec | 2 sec | 2 sec | 1 sec |

Below 8 seconds: Phase 1 only. "We should talk about X."

### 3.5 Protocol State Machine
```ascii
IDLE -> CHANNEL_ACQUIRED -> VISUAL_SCAN
  -> COGNITIVE_SCAN -> EFA_CALC -> HOOK_TX
  -> ABA Check: No -> ABORT | Yes -> CORE_TX
  -> Floor Event: Open -> TERMINATE | Closed -> CLOSE_TX
  -> CHANNEL_RELEASED
```

## 4. Failure Modes

**4.1 Empty Elevator**: No receiver. PCR approaches infinity.
Protocol stays IDLE.

**4.2 Competing Pitches**: Two Pitchers transmit simultaneously.
Both ABA drops to 0.3. Effective bandwidth collapses.

**4.3 Manager in Elevator**: ABA for manager = 0.60. PCR degrades
to 30%. Content shifts to weather.

**4.4 Awkward Silence**: Neither party initiates. Channel idle
for entire duration. IPM irrelevant.

**4.5 Floor Miscalculation**: Pitcher estimates 10-floor ride.
Pitchee exits at floor 2. EFA overestimates by 32 seconds.

Failed pitches generate a Resume Token: "Anyway, about X --
elevator Thursday?" This converts EPBA failure into a scheduled
CBP exchange (RFC-0017).

## 5. Security Considerations

**5.1 Eavesdropping**: Channels are broadcast. Sensitive pitches
require CBP (RFC-0017). **5.2 Pitch Injection**: Unauthorized
party interrupts; ABA cost increases by 0.5. **5.3 Social
Engineering**: Adversary offers small pitch to solicit a larger
one. **5.4 Floor Indicator Spoofing**: Misrepresenting
destination to extend pitch window.

## 6. Performance Evaluation

| Metric | Without EPBA | With EPBA |
|--------|-------------|-----------|
| PCR (bits/sec) | 2.1 | 5.8 |
| ABA efficiency | 35% | 62% |
| Pitch completion rate | 40% | 73% |
| Resume Token usage | 0% | 45% |

**Key observation**: A 3-floor ride at 4 sec/floor yields 16
seconds of usable channel. At PCR = 5.8, that is 93 bits. A
well-crafted elevator pitch needs 200+ bits. The protocol does
not solve the problem -- it quantifies why it is unsolvable
and routes failures to CBP.

## 7. Extensions

| RFC | Title | Status |
|-----|-------|--------|
| 0017 | Coffee-Break Protocol (CBP) | DRAFT |
| 0020 | Elevator Consensus Algorithm | PLANNED |

## 8. References

### 8.1 Normative References

[RFC-0017] Matos, R.M. "Coffee-Break Protocol (CBP)." RFC 0017,
OSC, 2001. https://rfc.osc.org/rfc0017.

[RFC-0020] Matos, R.M. "Elevator Consensus Algorithm." RFC 0020,
OSC, 2026. https://rfc.osc.org/rfc0020.

### 8.2 Informative References

Granovetter, Mark S. 1973. "The Strength of Weak Ties." *American
Journal of Sociology* 78 (6): 1360--1380.

Nonaka, Ikujiro, and Hirotaka Takeuchi. 1995. *The Knowledge-
Creating Company*. New York: Oxford University Press.

Wenger, Etienne. 1998. *Communities of Practice*. Cambridge:
Cambridge University Press.

Shannon, Claude E. 1948. "A Mathematical Theory of Communication."
*Bell System Technical Journal* 27 (3): 379--423.

Goffman, Erving. 1959. *The Presentation of Self in Everyday Life*.
New York: Anchor Books.

---

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-18 | Rodolfo Matos | Initial draft |

## Appendix B: Open Issues

1. Multi-elevator buildings: EPBA in adjacent shafts.
2. Escalator variant: moving walkways vs. elevators.
3. Pitch length limits: maximum PCR threshold.
4. Open-shaft environments: behavior undefined.

---

> **Colophon**: The Organizational Standards Consortium (OSC)
> does not exist. It is a fictional standards body created for
> the Organizational Epistemology Project (OEP). RFCs published
> under the OSC imprint are satirical artifacts that encode
> genuine organizational science. The elevator, however, is
> real -- and it is currently synchronizing more knowledge than
> this repository ever will.
