---
rfc: "0014"
title: "Consensus Theater Choreography"
stream: "Best Current Practice"
status: "DRAFT"
category: "Process"
area: "process"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-18"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [4, 6, 11]
keywords: [consensus, theater, choreography, performative, decision-making, alignment]
abstract: |
  This document specifies the Consensus Theater Choreography Protocol
  (CTCP), a formal framework for measuring the performance of consensus
  in organizational settings. CTCP introduces four diagnostic metrics:
  the Consensus Performance Score (CPS), the Pre-Decision Detection
  Rate (PDDR), the Dissent Suppression Index (DSI), and the Alignment
  Theater Factor (ATF). Organizations achieving high CPS while
  maintaining low ATF produce fewer decisions and better outcomes.
dual_layer: true
satire_notice: "satire"
---

# RFC-0014 — Consensus Theater Choreography

## Abstract

Organizational consensus is rarely a decision-making process; it is a
performance art. The meeting room is a stage, the agenda is a script,
and the predetermined outcome is the audience's expected finale. CTCP
formalizes the metrics that distinguish genuine alignment from
choreographed agreement.

## 1. Introduction

In most organizations, the decision is made before the meeting
convenes. The meeting exists to transform a private preference into a
public preference through ritualized nods, murmurs, and strategic
silence. CTCP does not aim to eliminate consensus theater. It aims to
measure it.

### 1.1 Scope

This RFC applies to any gathering of three or more actors convened for
"reaching alignment," including steering committees, architecture
reviews, sprint retrospectives, and post-mortems.

### 1.2 Non-Goals

- Eliminating performative consensus (see RFC-0004 for DTS)
- Detecting strategic misalignment (see RFC-0006 for SMDP)
- Accelerating meeting entropy (see RFC-0011 for MEAP)

## 2. Terminology

| Term | Definition |
|------|-----------|
| Consensus Theater | Ritualized performance of agreement in a group setting |
| Pre-Decision | Decision made before the formal consensus process begins |
| Choreography | Sequence of performative actions producing alignment appearance |
| Dissent Suppression | Mechanism reducing probability of minority opinion expression |
| Alignment Theater | Ratio of performed alignment to actual belief convergence |
| Stage Director | Individual who orchestrates the choreography sequence |
| Audience | Participants expected to observe without interrupting |
| Curtain Call | Closing statement affirming the predetermined outcome |

## 3. Protocol Specification

### 3.1 Consensus Performance Score (CPS)

CPS measures how well a team performs agreement.

```
CPS = (AE x PD x SC) / (1 + DC)
```

Where:
- AE = Average Enthusiasm (scale 1-10, self-reported)
- PD = Participation Duration ratio (time spent / time allocated)
- SC = Satisfaction Count (post-meeting positive survey responses)
- DC = Dissent Count (explicit objections raised)

CPS ranges from 0 (total performance failure) to 50 (theoretical
maximum). Organizations targeting CPS above 40 exhibit theater
addiction.

### 3.2 Pre-Decision Detection Rate (PDDR)

PDDR estimates the probability a decision was made before the meeting.

```
PDDR = (FD + PS + ES) / (3 x T)
```

Where:
- FD = First-Draft Match (binary: final output matches initial
  proposal without substantive revision)
- PS = Prior-Signal Strength (decision frequency in pre-meeting
  communications)
- ES = Early-Support Ratio (attendees who agreed before meeting)
- T = Total attendees

PDDR above 0.7 indicates performative meetings. PDDR of 1.0 means
the meeting was unnecessary.

### 3.3 Dissent Suppression Index (DSI)

DSI measures the degree to which minority opinions are silenced.

```
DSI = 1 - (DI x PF x RS) / N
```

Where:
- DI = Dissent Incidents (minority positions articulated)
- PF = Platform Fraction (meeting time allocated to dissent)
- RS = Responsiveness Score (engagement quality with dissent, 0-1)
- N = Normalization constant (set to 3)

DSI ranges from 0 (dissent encouraged) to 1 (dissent suppressed).
DSI above 0.8 indicates internally consistent choreography.

### 3.4 Alignment Theater Factor (ATF)

ATF is the ratio of performed alignment to actual alignment.

```
ATF = PA / AA
```

Where:
- PA = Performed Alignment (post-meeting agreement rate, 0-1)
- AA = Actual Alignment (follow-through rate on decisions, 0-1)

ATF of 1.0 means perfect alignment between performance and reality.
ATF of 3.0 means the team performed three times more alignment than
they achieved.

## 4. Failure Modes

| Mode | Threshold | Indicator | Corrective Action |
|------|-----------|-----------|-------------------|
| CPS Saturation | CPS > 45 | Performance metrics override quality | Mandate dissent period |
| PDDR Collapse | PDDR < 0.3 | Decisions genuinely open | Use RFC-0006 (SMDP) to assess |
| DSI Inversion | DSI < 0.1 | Dissent actively encouraged | Inject controversial agenda item |
| ATF Drift | ATF > 4.0 | Performance-reality gap dangerous | Conduct alignment audit |

## 5. Security Considerations

- Post-meeting surveys MUST be anonymous
- PDDR metrics MUST NOT identify and penalize dissenters
- DSI scores MUST NOT optimize suppression
- ATF data SHOULD be shared transparently

Organizations using CTCP to optimize theater quality rather than
reduce it exhibit theater addiction (see Section 4).

## 6. Performance Evaluation

| Metric | Healthy | Warning | Critical |
|--------|---------|---------|----------|
| CPS | 15-35 | 35-45 | >45 |
| PDDR | 0.3-0.7 | 0.7-0.9 | >0.9 |
| DSI | 0.3-0.6 | 0.6-0.8 | >0.8 |
| ATF | 1.0-1.5 | 1.5-2.5 | >2.5 |

## 7. Extensions

| Extension | Status | Description |
|-----------|--------|-------------|
| CTCP-Realtime | Experimental | Live monitoring via sentiment analysis |
| CTCP-Audit | Proposed | Quarterly theater quality reviews |
| CTCP-Anonymous | Proposed | Blind scoring to reduce observer effect |
| CTCP-Lite | Informational | Simplified metrics for short meetings |
| CTCP-Adversarial | Informational | Inject dissent to test DSI resilience |

## 8. References

### 8.1 Normative References

[RFC-0004] Decision Theater Specification (DTS). OSC, 2026.
  https://rfc.osc.org/rfc0004

[RFC-0006] Strategic Misalignment Detection Protocol (SMDP). OSC,
  2026. https://rfc.osc.org/rfc0006

### 8.2 Informative References

[RFC-0011] Meeting Entropy Acceleration Protocol (MEAP). OSC, 2026.
  https://rfc.osc.org/rfc0011

[RFC-0017] Coffee-Break Protocol (CBP). OSC, 2001.
  https://rfc.osc.org/rfc0017

Mintzberg, Henry. 1983. *Power In and Around Organizations*.
  Englewood Cliffs: Prentice-Hall.

March, James G. 1994. *A Primer on Decision Making: How Decisions
  Happen*. New York: Free Press.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-18 | Rodolfo Matos | Initial draft |

## Appendix B: Open Issues

1. Whether CPS should account for coffee quality (CBP integration)
2. Handling Stage Directors who are also primary dissenters
3. Whether negative ATF values indicate choreography surprise

---

> **Satire Notice**: This document is published in the
> **Best Current Practice** stream. While its metrics are internally
> consistent and its formulas are mathematically coherent, CTCP is
> designed to illuminate the gap between organizational performance
> and organizational reality. The OSC does not recommend deploying
> CTCP to optimize theater quality, though it acknowledges that some
> organizations will inevitably try.

---

> **Colophon**: The Organizational Standards Consortium (OSC) does
> not exist. It is a fictional standards body created for the
> Organizational Epistemology Project (OEP). RFCs, OEPs, Theorems,
> and Papers published under the OSC imprint are satirical artifacts
> that encode genuine organizational science. All citations of real
> scholars (Mintzberg, March, Simon, Granovetter, etc.) are accurate.
