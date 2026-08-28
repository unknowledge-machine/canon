---
rfc: "0024"
title: "Trench Intelligence Protocol (TIP)"
stream: "Humor"
status: "DRAFT"
category: "Informational"
area: "informal-networks"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-19"
updated: "2026-07-19"
obsoletes: []
obsoleted_by: []
see_also: [1, 4, 11, 14, 17, 23]
keywords:
  - trench-intelligence
  - command-distance
  - generals-blind-spot
  - ground-truth
  - order-decay
  - executive-delusion
abstract: |
  Decisions made without ground truth have an inverse
  relationship with reality. This RFC formalizes the
  degradation of organizational decisions in proportion
  to hierarchical distance between decisor and executor.
  TIP introduces six metrics: Command Distance, Trench
  Intelligence, Generals' Blind Spot, Order Fidelity
  Decay, Crystal Glass Decision Quality, and Wine-to-Mud
  Ratio, extending RFC-0001 (HOP) by quantifying what
  HOP assumes away: that higher rank implies knowledge.
dual_layer: true
satire_notice: "satire"
---

# RFC-0024: Trench Intelligence Protocol (TIP)

| RFC   | 0024                                    |
|-------|-----------------------------------------|
| Title | Trench Intelligence Protocol (TIP)      |
| Stream| Humor                                   |
| Status| DRAFT                                   |
| Area  | Informal Networks                       |

## Status of This Memo

Distribution is unlimited. Implementation requires one
mud-soaked field visit per quarter and willingness to
cancel the wine order.

## Abstract

The finding is never about missing strategy decks.
It is about decisions made in rooms where nobody has
touched the code, walked the floor, or spoken to the
people who do the work. TIP introduces six metrics
for measuring organizational decision-delusion.

> **Satire Notice**: This document is published in the
> **Humor/Experimental** stream. Its primary purpose is
> satirical illumination of organizational dynamics.
> The OSC does not recommend deploying TIP without
> first spending one full sprint in the trench.

## 1. Introduction

World War I generals decided battles from chalices of
wine while soldiers drowned in mud. They were not
malicious. They were distant. The organizational
equivalent persists: decisions made by people who have
not consulted the people who will execute them.

RFC-0001 (HOP) codified the delusion that hierarchy
implies omniscience. TIP quantifies its failure.
RFC-0004 (Decision Theater) documented decisions that
are performed, not made. RFC-0011 (Meeting Entropy)
measured degradation in meetings absent ground truth.
RFC-0014 (Consensus Theater) analyzed the ritual of
agreeing without committing. RFC-0017 (CBP) identified
the coffee machine as the only channel where trench
intelligence reaches leadership. RFC-0023 (PGP)
described the ceremony of making bad decisions official.

## 2. Terminology

| Term | Definition |
|------|-----------|
| **Trench** | Execution-level context where work happens |
| **Command** | Decision-making context where orders originate |
| **Ground Truth** | Operational knowledge at execution level |
| **Command Distance (CD)** | Distance between decisor and executor |
| **Trench Intelligence (TI)** | Tacit knowledge at execution level |
| **Generals' Blind Spot (GBS)** | Inability to perceive ground truth |
| **Order Fidelity Decay (OFD)** | Intent degradation, command to execution |
| **Wine-to-Mud Ratio (WMR)** | Comfort asymmetry, decisor vs executor |
| **Crystal Glass Decision** | Decision without ground truth contact |

## 3. Protocol Specification

### 3.1 Command Distance (CD)

```
CD = H x F x C
```

H = hierarchy levels, F = floor differential,
C = calendar dissimilarity.

| CD Range | Classification | Ground Truth |
|----------|---------------|-------------|
| 0 | Trench-Level | Full |
| 1-3 | Platoon Range | High |
| 4-9 | Battalion Range | Moderate |
| 10-24 | Corps Range | Low |
| 25-49 | Theater Range | Minimal |
| 50+ | WWI General Range | None |

```
COMMAND (CD=50)      [wine] [slides] [ease]
        |
Senior Mgmt          [meetings] [reviews]
        |
Middle Mgmt          [reports] [summaries]
        |
Team Leads           [standups] [tickets]
        |
EXECUTION (CD=0)     [mud] [bugs] [reality]
```

### 3.2 Trench Intelligence (TI)
```
TI = f(T, I, W)  -->  TI = K / CD
```
T = tacit knowledge density, I = tool intimacy,
W = workaround count. At CD=0, TI is maximal.
At CD=50+, TI is zero.

### 3.3 Generals' Blind Spot (GBS)
```
GBS = 1 - e^(-lambda * CD)
```
lambda = 0.15 (default).

| CD | GBS | Interpretation |
|----|-----|----------------|
| 0 | 0.00 | Full visibility |
| 5 | 0.53 | Half-blind |
| 10 | 0.78 | Mostly blind |
| 20 | 0.95 | Nearly total |
| 30+ | 0.99 | Cannot perceive the trench |

### 3.4 Order Fidelity Decay (OFD)
```
OFD(t) = e^(-alpha * CD)
```
alpha = 0.08 (default), t = time since order issued.

| CD | OFD(0) | OFD(1w) | OFD(1m) | Outcome |
|----|--------|---------|---------|---------|
| 0 | 1.00 | 0.95 | 0.80 | Intact |
| 5 | 0.67 | 0.64 | 0.51 | Decay |
| 10 | 0.45 | 0.43 | 0.34 | Half intact |
| 20 | 0.20 | 0.19 | 0.15 | Unrecognizable |
| 50 | 0.02 | 0.02 | 0.01 | Fiction |

### 3.5 Crystal Glass Decision Quality (CGDQ)
```
CGDQ = (comfort x wine) / (mud x reality)
```
Higher CGDQ = worse decisions (inverse metric).

| CGDQ | Quality | Archetype |
|------|---------|-----------|
| 0-1 | Excellent | In the trench |
| 1-3 | Good | Has visited |
| 3-7 | Degraded | Reads reports |
| 7-10 | Poor | Never seen it |
| 10+ | Catastrophic | WWI General |

### 3.6 Wine-to-Mud Ratio (WMR)
```
WMR = decisor_comfort / executor_comfort
```

| WMR | Classification | Parallel |
|-----|---------------|----------|
| 1-2 | Healthy parity | Startup |
| 2-5 | Moderate gap | Normal org |
| 5-10 | Significant | Enterprise |
| 10-25 | Generational | Bureaucracy |
| 100+ | WWI Conditions | Foxhole to cellar |

## 4. TIP Composite Score
```
TIP = (GBS x CD) / (TI + 1)
    + (OFD(0) x CGDQ) / WMR
```

| TIP | State |
|-----|-------|
| 0-2 | Grounded |
| 2-5 | Drift |
| 5-10 | Detached |
| 10-20 | Delusional |
| 20+ | WWI: pour more wine |

## 5. Failure Modes

| Mode | Description | Detection |
|------|-------------|-----------|
| Trench Radio | Feedback from execution to command ceases | Zero status-outcome correlation |
| Generals' Echo | Decision-makers speak only to each other | All attendees at CD > 15 |
| Mud Deficit | Assumes conditions better than they are | Estimates exceed plan by 3x twice |
| Wine Overflow | Comfort makes reality inaccessible | GBS > 0.95, CGDQ > 10 |
| Order Echo | Orders bounce, reinterpreted per layer | Work matches no known initiative |
| PG Contamination | RFC-0023 formalizes wrong decisions | Post-PGC rejection > 60% |

## 6. Security Considerations

TIP metrics will be gamed. CD reduced by redefining
reporting lines. GBS suppressed by hiring trench
liaisons who never leave the command floor. WMR
equalized by reducing executor comfort.

The only defense is anonymous longitudinal measurement
by an entity with no stake in the outcome. This entity
does not exist in most organizations.

## 7. Performance Evaluation

| Quarter | Action | Expected Effect |
|---------|--------|----------------|
| Q1 | Baseline measurement | CD and GBS assessed |
| Q2 | Executive trench visits | CD -10%, GBS -5% |
| Q3 | Trench Radio deployment | GBS -15% |
| Q4 | Re-measurement | TIP score -25-40% |

Requires sustained executive willingness to reduce
their own comfort (historically 5-12% success rate).

**Limitation:** TIP measures the distance. Closing it
requires structures that do not yet exist at scale.

## 8. Extensions

| Extension | Description | Status |
|-----------|-------------|--------|
| TIP-CLI | Compute all metrics | Planned |
| TIP-Visualizer | CD heatmap across org chart | Planned |
| TIP-Audit | Automated Mud Deficit detection | Planned |
| TIP-Simulator | Model decay across reorg | Planned |
| TIP-TrenchVisits | Executive field scheduler | Planned |
| TIP-ComfortCap | Maximum WMR enforcement | Experimental |

## 9. References
| Ref | Document |
|-----|----------|
| [RFC1] | RFC-0001: Hierarchical Omniscience Protocol |
| [RFC4] | RFC-0004: Decision Theater Specification |
| [RFC11] | RFC-0011: Meeting Entropy Acceleration |
| [RFC14] | RFC-0014: Consensus Theater Choreography |
| [RFC17] | RFC-0017: Coffee-Break Protocol (CBP) |
| [RFC23] | RFC-0023: Promotion Gate Protocol (PGP) |

## 10. Authors' Address

Rodolfo Matos, OSC, rm@osc.org

## 11. Colophon

Dedicated to every engineer who heard "this should be
simple" from someone who never opened the repository.
The mud is real. The wine is real. The distance
between them is measurable.

---

*End of RFC-0024*
