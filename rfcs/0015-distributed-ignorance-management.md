---
rfc: "0015"
title: "Distributed Ignorance Management"
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
see_also: [7, 16]
keywords: [ignorance, distributed, management, knowledge-gaps,
  organizational-blind-spots]
abstract: |
  This document specifies the Distributed Ignorance Management Protocol
  (DIMP), a protocol for detecting, quantifying, and governing the
  propagation of ignorance across distributed organizations. DIMP
  introduces the Ignorance Distribution Protocol (IDP), the Knowledge
  Gap Propagation Model (KGPM), the Blind Spot Synchronization Index
  (BSSI), and the Ignorance Equilibrium Theorem (IET). Organizations
  without DIMP reach ignorance equilibrium faster than they reach
  consensus, and ignorance generation exceeds knowledge generation
  by a factor inversely proportional to documentation writers.
dual_layer: true
satire_notice: "satire"
---

# RFC-0015 — Distributed Ignorance Management Protocol

## Abstract

This document specifies the Distributed Ignorance Management Protocol
(DIMP), a protocol for detecting, quantifying, and governing the
propagation of ignorance across distributed organizations. DIMP
introduces the Ignorance Distribution Protocol (IDP), the Knowledge
Gap Propagation Model (KGPM), the Blind Spot Synchronization Index
(BSSI), and the Ignorance Equilibrium Theorem (IET). Organizations
without DIMP reach ignorance equilibrium faster than they reach
consensus, and ignorance generation exceeds knowledge generation
by a factor inversely proportional to documentation writers.

> **Satire Notice**: This document is published in the **Standards Track**
> stream. While technically coherent, its primary purpose is satirical
> illumination of organizational dynamics. The OSC does not recommend
> deploying DIMP without a Chief Ignorance Officer.

## 1. Introduction

Every organization generates ignorance at a predictable rate. Unlike
knowledge, which requires effort to produce, ignorance arises
spontaneously from missed meetings, departed employees, unwritten
decisions, and the natural decay of undocumented context. In
distributed organizations, ignorance propagates through org charts,
slack channels, and onboarding documents with high fidelity.

DIMP formalizes this propagation to enable organizations to measure
and govern what they do not know. Most organizational failures stem
not from bad decisions, but from decisions made without awareness of
relevant ignorance.

## 2. Terminology

| Term | Definition |
|------|------------|
| **Ignorance** | Knowledge the org possesses in aggregate but no individual holds in full. |
| **Blind Spot** | Ignorance unknown and unmeasurable by the team that holds it. |
| **Knowledge Gap** | Ignorance identified but not yet addressed. |
| **IDP** | Ignorance Distribution Protocol — formal mechanism for propagation. |
| **KGPM** | Knowledge Gap Propagation Model — amplification across teams. |
| **BSSI** | Blind Spot Synchronization Index — shared unknown unknowns. |
| **IET** | Ignorance Equilibrium Theorem — steady-state convergence proof. |

## 3. Protocol Specification

### 3.1 Ignorance Distribution Protocol (IDP)

IDP models how ignorance propagates through organizational structure.
Each node maintains an Ignorance Vector (IV):

```
IV_i = [k_gaps, u_blind, d_expired]
```

Where `k_gaps` = identified gaps, `u_blind` = estimated blind spots,
`d_expired` = stale knowledge items. Propagation along reporting lines:

```
IV_j += alpha * IV_i
```

Propagation coefficients: 0.8 direct reports, 0.4 skip-level,
0.2 cross-functional peers, 0.1 external partners.

**IDP Packets**:

```
IDP_ANNOUNCE: source_node, vector, timestamp
IDP_SYNC:     source_node, target_node, gap_delta, blind_estimate
IDP_EXPIRE:   source_node, knowledge_item, decay_reason
```

### 3.2 Knowledge Gap Propagation Model (KGPM)

Gaps amplify as they cross team boundaries:

```
GAP_total = G_0 * (1 + beta)^h * (1 + gamma * r)
```

`G_0` = initial gap, `h` = team hops, `beta` = amplification per hop
(0.15), `gamma` = context-loss factor (0.3), `r` = downstream
turnover ratio.

| Distance | Amplification | Gap Size |
|----------|--------------|----------|
| Same team | 1.0x | G_0 |
| 1 hop | 1.15x | 1.15 * G_0 |
| 2 hops | 1.32x | 1.32 * G_0 |
| 3 hops | 1.52x | 1.52 * G_0 |
| Executive | 2.0x+ | 2.0 * G_0 |

### 3.3 Blind Spot Synchronization Index (BSSI)

BSSI measures shared unknown unknowns across teams:

```
BSSI = |Intersection(B_i, B_j)| / |Union(B_i, B_j)|
```

Where `B_i` = blind spots not queried by team i and not reported
by neighbors.

| BSSI Range | Classification | Risk |
|------------|---------------|------|
| 0.0 - 0.2 | Diverse ignorance | Low |
| 0.2 - 0.5 | Partial overlap | Moderate |
| 0.5 - 0.8 | Synchronized | High |
| 0.8 - 1.0 | Lockstep | Critical |

### 3.4 Ignorance Equilibrium Theorem (IET)

Organizations with constant staffing reach steady-state ignorance
where generation equals resolution:

```
dI/dt = G(t) - R(t) = 0   =>   I_eq = G_rate / R_rate
```

`G_rate` = ignorance generation (turnover + decisions + time).
`R_rate` = ignorance resolution (documentation + onboarding).

**Corollaries**:

1. `R_rate < G_rate` yields unbounded ignorance growth.
2. Doubling team size increases `G_rate` by N*(N-1)/2 new gaps.
3. Documentation reduces `G_rate` but `R_rate` increases only when
   read. Unread docs are blind spots with URLs.

## 4. Failure Modes

| Mode | Description | Mitigation |
|------|-------------|------------|
| Feedback Loop | Team A ignorant of X, B assumes A knows. Oscillation. | IDP_SYNC broadcasts |
| Documentation Theater | High doc volume, zero readers. BSSI spikes. | Reading verification |
| Onboarding Amplification | New hire inherits IV * (1 + beta). | Explicit gap briefing |
| Sync Event | Reorg causes BSSI spike 0.2 to 0.9 in one quarter. | Mandatory ignorance audits |

## 5. Security Considerations

| Threat | Description | Mitigation |
|--------|-------------|------------|
| Weaponization | Suppress ignorance reports for power asymmetry. | Mandatory IDP_ANNOUNCE |
| Selective Leaking | Reveal others' ignorance, hide own. | Cryptographic commitment |
| Ignorance DDoS | Flood IDP_SYNC with low-quality reports. | Rate limiting |

## 6. Performance Evaluation

### 6.1 DIMP vs. No-DIMP

| Metric | No-DIMP | With DIMP |
|--------|---------|-----------|
| Avg BSSI | 0.65 | 0.30 |
| IET Convergence | 3 months | 8 months |
| Gap Amplification | 2.0x/hop | 1.1x/hop |
| Audit Cost | Unknown | Measurable |

### 6.2 Optimal Ignorance Budget

```
I_optimal = G_rate / (R_rate * (1 + epsilon))
```

`epsilon` = acceptable overshoot (0.1 recommended). Below
`I_optimal`: over-investing in documentation. Above: accumulating
blind spots.

## 7. Extensions

| RFC | Title | Status |
|-----|-------|--------|
| 0007 | Organizational Amnesia Prevention | Active |
| 0009 | Knowledge Hoarding Incentive Structure | Active |
| 0010 | Epistemic Injustice Remediation | Active |
| 0016 | Unknown Unknowns Registry | Planned |
| 0022 | Ignorance Budget Allocation | Planned |

## 8. References

### 8.1 Normative References

[RFC-0007] Matos, R.M. "Organizational Amnesia Prevention Protocol."
RFC 0007, OSC, 2008.

[RFC-0016] Matos, R.M. "Unknown Unknowns Registry." RFC 0016, OSC, 2026.

### 8.2 Informative References

Argote, L. and Miron-Spektor, E. 2011. "Organizational Learning:
From Experience to Knowledge." *Organization Science* 22(5).

March, J.G. 1991. "Exploration and Exploitation in Organizational
Learning." *Organization Science* 2(1).

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not
> exist. It is a fictional standards body created for the Organizational
> Epistemology Project (OEP). RFCs published under the OSC imprint are
> satirical artifacts that encode genuine organizational science. The
> ignorance, however, is real -- and it is distributed.
