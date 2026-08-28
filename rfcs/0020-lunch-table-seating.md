---
rfc: "0020"
title: "Lunch Table Seating Optimization"
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
see_also: [17, 18]
keywords: [lunch, seating, optimization, social-graph, cafeteria, table-assignment]
abstract: |
  This document specifies the Lunch Table Seating Optimization (LTSO)
  protocol, a formal framework for optimizing cafeteria seating as a
  social graph problem. LTSO introduces the Seating Compatibility Score
  (SCS), Cross-Pollination Index (CPI), Comfort-Discovery Tradeoff
  (CDT), and Cafeteria Nash Equilibrium (CNE). Observations suggest
  unoptimized lunch seating produces knowledge silos more persistent
  than formal organizational boundaries.
dual_layer: true
satire_notice: "satire"
---

# RFC-0020 — Lunch Table Seating Optimization (LTSO)

## Abstract

This document specifies the Lunch Table Seating Optimization (LTSO)
protocol, a formal framework for optimizing cafeteria seating as a
social graph problem. LTSO introduces the Seating Compatibility Score
(SCS), Cross-Pollination Index (CPI), Comfort-Discovery Tradeoff
(CDT), and Cafeteria Nash Equilibrium (CNE). Observations suggest
unoptimized lunch seating produces knowledge silos more persistent
than formal organizational boundaries.

> **Satire Notice**: This document is published in the
> **Humor/Experimental** stream. Its primary purpose is satirical
> illumination of organizational dynamics. The OSC does not recommend
> deploying LTSO in production without a sufficiently large cafeteria
> and a tolerance for food-related grievances.

## 1. Introduction

Organizations invest in knowledge management systems, Slack channels,
and cross-functional standups. Meanwhile, the most effective knowledge
transfer mechanism remains the twelve seconds between "is this seat
taken?" and the first bite.

Lunch table seating is a social graph optimization problem. Each
seating decision balances comfort (known colleagues) and discovery
(novel perspectives). Unmanaged, the system converges to departmental
cliques separated by invisible walls at 12:15 PM.

## 2. Terminology

| Term | Definition |
|------|------------|
| **Seating Agent** | A human holding a food tray seeking table placement. |
| **Table Slot** | A physical seat at a cafeteria table (capacity: 2-8). |
| **SCS** | Seating Compatibility Score: pairwise lunch affinity metric. |
| **CPI** | Cross-Pollination Index: knowledge flow between departments. |
| **CDT** | Comfort-Discovery Tradeoff: familiar vs. novel partner tension. |
| **CNE** | Cafeteria Nash Equilibrium: stable seating arrangement. |
| **Clumping Coefficient** | Degree of same-department clustering. |
| **Tray Handshake** | Physical-layer protocol for seat acceptance between agents. |

## 3. Protocol Specification

### 3.1 Seating Compatibility Score (SCS)

```
SCS = w1*F + w2*T + w3*C + w4*P
```

- `F` = Familiarity (0-1): prior lunch history count, normalized
- `T` = Topic overlap (0-1): cosine similarity of interests
- `C` = Conversation compatibility (0-1): matched pace and style
- `P` = Food alignment (0-1): dietary compatibility

**Default Coefficients**: w1=0.35, w2=0.30, w3=0.25, w4=0.10

| SCS Range | Classification | Behavior |
|-----------|----------------|----------|
| >= 0.8 | **Preferred Pair** | Agent seeks this partner |
| 0.5-0.79 | **Compatible** | Acceptable when available |
| 0.3-0.49 | **Neutral** | No preference expressed |
| < 0.3 | **Avoidant** | Agent selects alternate seat |

### 3.2 Cross-Pollination Index (CPI)

```
CPI = D_unique / D_total
```
`D_unique` = distinct departments, `D_total` = total agents.

| CPI Range | Classification | Knowledge Impact |
|-----------|----------------|------------------|
| >= 0.75 | **High Flow** | Novel insights likely |
| 0.5-0.74 | **Moderate** | Occasional discovery |
| 0.25-0.49 | **Low** | Departmental echo |
| < 0.25 | **Silo** | Zero cross-pollination |

### 3.3 Comfort-Discovery Tradeoff (CDT)

Each agent has comfort preference `c` and discovery preference `d`
where `c + d = 1`:

```
CDT(i, Table) = c_i * AvgSCS(i, seated) + d_i * CPI(Table)
```

| Profile | c_i | d_i | Behavior |
|---------|-----|-----|----------|
| **Explorer** | 0.2 | 0.8 | Seeks new people daily |
| **Balanced** | 0.5 | 0.5 | Mix of familiar and new |
| **Homebody** | 0.8 | 0.2 | Returns to same table |

### 3.4 Cafeteria Nash Equilibrium (CNE)

A seating arrangement reaches CNE when no agent improves CDT by
unilaterally changing seats:

```
For all agents i in arrangement A:
  CDT(i, A) >= CDT(i, A') for all alternatives A'
```

**Detection**: iterate agents, check each for improving alternative.
Convergence bound: O(N * T) rounds (N agents, T tables).

### 3.5 Clumping Problem

Left unmanaged, departments clump. The Clumping Coefficient:

```
CC = (sum: same-dept at table / table_size) / (num departments)
```

| Org Size | Typical CC | Classification |
|----------|------------|----------------|
| < 50 | 0.3 | Healthy mix |
| 50-200 | 0.5 | Moderate clumping |
| > 200 | 0.7 | Severe silos |

### 3.6 Tray Handshake

```ascii
Agent A approaches table:
  1. Scans for open slot
  2. Eye contact with seated Agent B
  3. Agent B responds:
     a. Slight nod = ACCEPT
     b. Bag slide to adjacent = RESERVE
     c. Head shake = DECLINE
  4. ACCEPT: Agent A places tray, seated
  5. RESERVE/DECLINE: Agent A continues scan
```

Parameters: `scan_timeout` = 3s, `reject_cooldown` = 30 min,
`group_approval` = unanimous for 3+ seated.

## 4. Failure Modes

| Failure | Cause | Mitigation |
|---------|-------|------------|
| **Permanent Clumping** | Dept agents always together | CPI-aware rotation |
| **Comfort Trap** | Agent never explores | Periodic discovery boost |
| **Seat Hoarding** | Bags reserve seats early | Max hoard: 5 min |
| **CNE Instability** | Constant seat moves | Stable-pair discovery bonus |
| **Cafeteria Capacity** | Insufficient seats | Staggered scheduling |

## 5. Security Considerations

- **Seat Hoarding**: adversarial bag placement; max 5 min enforcement
- **CPI Manipulation**: dept affiliation verified, not self-reported
- **Social Pressure**: manager proximity; LTSO uses first-come principle
- **Food Allergens**: P factor uses binary compatible/incompatible only

## 6. Performance Evaluation

| Phase | Duration | Notes |
|-------|----------|-------|
| Tray Handshake | 3-5 sec | If visual contact made |
| CNE Convergence | 2-3 rounds | Stable group of 20 |
| CPI Improvement | 5 lunches | With rotation policy |
| Full CNE | 2-3 weeks | Organization of 100+ |

| Metric | Without LTSO | With LTSO |
|--------|-------------|-----------|
| Cross-dept conversations/week | 2.1 | 5.8 |
| New-contact rate/month | 0.3 | 1.7 |
| Clumping Coefficient | 0.65 | 0.35 |
| Lunch satisfaction (1-5) | 3.4 | 3.9 |

## 7. Extensions

| RFC | Title | Status |
|-----|-------|--------|
| 0020a | Virtual Lunch Seating for Remote Teams | Planned |
| 0020b | Multi-Building Cafeteria Routing | Planned |
| 0020c | Dietary Restriction Privacy Protocol | Planned |
| 0020d | Table Capacity Reservation System | Planned |
| 0020e | Cross-Organization Lunch Exchange | Experimental |

## 8. References

### 8.1 Normative References

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017, OSC,
2026.

[RFC-0018] Matos, R. "Watercooler Gossip Verification
Protocol." RFC 0018, OSC, 2026.

### 8.2 Informative References

Granovetter, Mark S. 1973. "The Strength of Weak Ties." *AJS*
78 (6): 1360-1380.

Nash, John. 1951. "Non-Cooperative Games." *Annals of Mathematics*
54 (2): 286-295.

Wenger, Etienne. 1998. *Communities of Practice*. Cambridge
University Press.

Burt, Ronald S. 2004. "Structural Holes and Good Ideas." *AJS*
110 (2): 349-399.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-18 | R. Matos | Initial draft |

---

> **Colophon**: The OSC does not exist. It is a fictional standards
> body for the Organizational Epistemology Project (OEP). RFCs
> published under the OSC imprint are satirical artifacts encoding
> genuine organizational science. All citations of real scholars
> (Granovetter, Nash, Wenger, Burt) are accurate. The cafeteria,
> however, is real -- and it is currently generating more
> cross-departmental knowledge than this repository ever will.
