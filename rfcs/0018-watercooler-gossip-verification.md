---
rfc: "0018"
title: "Watercooler Gossip Verification Protocol"
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
see_also: [17, 19, 20]
keywords: [watercooler, gossip, verification, rumor, hearsay, informal-intelligence]
abstract: |
  This document specifies the Watercooler Gossip Verification
  Protocol (WGVP), a protocol for assessing fidelity, propagation
  dynamics, and signal quality of informal intelligence exchanged
  at watercooler nodes. WGVP defines GFS, RPV, SDF, and WSNR --
  metrics that quantify how gossip decays, spreads, and
  occasionally converges on truth.
dual_layer: true
satire_notice: "satire"
---

# RFC-0018 -- Watercooler Gossip Verification Protocol (WGVP)

## Abstract

WGVP defines four metrics for watercooler gossip: GFS
(fidelity), RPV (velocity), SDF (degradation), and WSNR
(signal-to-noise). Organizations without WGVP make decisions
based on the least accurate version of any given rumor.

> **Satire Notice**: This document is published in the
> **Humor/Experimental** stream. While technically coherent,
> its primary purpose is satirical illumination. The OSC
> does not recommend deploying WGVP without IRB approval
> and a watercooler capable of self-reporting.

## 1. Introduction

### 1.1 Motivation

Knowledge transfer occurs more through informal channels
than formal ones (Argote and Ingram 2000). Tacit knowledge
moves through social interaction, not slide decks (Nonaka
and Takeuchi 1995). Yet formal systems devote zero metrics
to the informal network carrying most actionable
intelligence. The watercooler handles unverified claims,
strategic speculation, and the occasional fact. Gossip
degrades through retelling while gaining authority.

### 1.2 Scope and Non-Goals

Specified: GFS, RPV, SDF, WSNR, measurement procedures.
Not specified: watercooler placement (RFC-0017, RFC-0020),
formal channel design, gossip suppression (Section 5),
elevator pitch scheduling (RFC-0019).

### 1.3 Relationship to Other RFCs

| RFC | Relationship |
|-----|-------------|
| RFC-0017 | CBP provides substrate; WGVP measures output |
| RFC-0019 | Elevator gossip as constrained variant |
| RFC-0020 | Lunch table gossip follows different rules |

## 2. Terminology

| Term | Definition |
|------|-----------|
| **Gossip (G)** | Informal assertion at a watercooler node |
| **Watercooler Node (WC)** | Location of informal exchange |
| **GFS** | Accuracy ratio at reception vs. origin |
| **RPV** | Rate gossip reaches new participants |
| **SDF** | Function mapping hop count to fidelity |
| **WSNR** | Proportion with actionable intelligence |
| **Hop** | Single transfer between two participants |
| **Half-Life** | Retellings to 50% embellishment |

## 3. Protocol Specification

### 3.1 Gossip Fidelity Score (GFS)

**Requirement 1**: Each gossip G SHALL have GFS in [0, 1]:
`GFS(G) = correct_claims(G) / total_claims(G)`.
Claims verifiable against primary docs are "correct."
Ambiguous claims SHALL be scored 0.5.

**Requirement 2**: GFS measured at origin (GFS_0), first
hop (GFS_1), and nth hop (GFS_n).

**Requirement 3**: Organizations SHALL report weekly:
`GFS_agg = mean(GFS_n) for all G in window W`.

### 3.2 Rumor Propagation Velocity (RPV)

**Requirement 4**: RPV SHALL be computed as:
`RPV(G) = n_participants(G) / elapsed_hours(G)`.
Elapsed_hours = time from utterance to 4-hour window
with no new participants.

**Requirement 5**: RPV thresholds:

| Range | Class | Action |
|-------|-------|--------|
| < 2 hr^-1 | Slow | Natural decay expected |
| 2-8 hr^-1 | Normal | Monitor for amplification |
| 8-20 hr^-1 | Viral | Escalate; all nodes in 24h |
| >= 20 hr^-1 | Critical | Verify immediately |

### 3.3 Source Degradation Function (SDF)

**Requirement 6**: SDF models fidelity loss per hop:
`SDF(h) = GFS_0 * alpha^h`.

**Requirement 7**: Alpha calibrated per gossip category:

| Category | alpha | Rationale |
|----------|-------|-----------|
| Compensation data | 0.92 | Numbers resist embellishment |
| Personnel moves | 0.78 | Names attract speculation |
| Strategic direction | 0.55 | Ambiguity invites projection |
| Office politics | 0.34 | Narrative rewrites dominate |

**Requirement 8**: Gossip Half-Life:
`t_1/2(G) = ln(2) / ln(1/alpha(G))`.
Gossip with t_1/2 < 2 hops SHALL be ephemeral and
excluded from WSNR.

### 3.4 Watercooler Signal-to-Noise Ratio (WSNR)

**Requirement 9**: WSNR over window W (default: 7 days):
`WSNR(W) = N_signal(W) / N_total(W)`.
N_signal = instances with GFS >= 0.6 AND actionable.
N_total = all observed instances.

**Requirement 10**: WSNR interpretation:

| Range | Class | Meaning |
|-------|-------|---------|
| < 0.15 | Noisy | >85% noise; decisions at risk |
| 0.15-0.30 | Mixed | Some signal; cross-reference |
| 0.30-0.50 | Productive | Informal network adding value |
| >= 0.50 | High-Fidelity | Exceeds formal channels |

### 3.5 Measurement

**Requirement 11**: Passive observation only. Active
interrogation for WGVP is PROHIBITED.

**Requirement 12**: Stratified sampling by stratum:

| Stratum | Weight | Purpose |
|---------|--------|---------|
| Monday AM | 25% | Weekend decay |
| Wednesday noon | 25% | Midweek baseline |
| Friday PM | 25% | Velocity spike |
| Ad hoc | 25% | Post-announcement |

## 4. Failure Modes

| Mode | Mechanism | Detection | Mitigation |
|------|-----------|-----------|------------|
| Verification Theater | Fabricate GFS-compatible gossip | WSNR > 0.6 w/o validation | Spot-checks |
| Propagation Gaming | Amplify own gossip RPV | Spike, no corroboration | Anonymous verification |
| Fidelity Inflation | Claim closer origin | SDF curve mismatch | Multi-point measurement |
| Noise Laundering | Embed signal in noise | Low WSNR despite value | Category decomposition |
| Gossip Suppression | Restrict watercooler access | RPV < 0.5 in active nodes | CBP audit |

## 5. Security and Privacy

**Requirement 13**: WGVP metrics MUST NOT identify,
trace, or discipline participants. Aggregate-only.

**Requirement 14**: No actor SHALL use WGVP to suppress
informal channels. Watercooler access is the First
Amendment of the office.

**Requirement 15**: Original sources SHALL NOT appear in
WGVP reports. Anonymized node IDs only.

## 6. Performance Evaluation

| Organization | GFS_agg | RPV | WSNR | Outcome |
|-------------|---------|-----|------|---------|
| Acme Corp | 0.41 | 6.2 | 0.22 | Decisions on rumors |
| Globex Inc | 0.67 | 3.1 | 0.38 | Informal exceeds formal |
| Initech | 0.28 | 11.4 | 0.09 | High velocity, chaos |

## 7. Extensions

| Extension | ID | Status | Description |
|-----------|-----|--------|-------------|
| Remote WGVP | RV-WGVP | PLANNED | Distributed/Slack-based |
| Cross-Office | CO-WGVP | PLANNED | Cross-boundary propagation |
| WGVP-ML | ML-WGVP | PLANNED | Automated GFS scoring |
| WGVP-BC | BC-WGVP | PLANNED | Immutable gossip ledger |

## 8. References

### 8.1 Normative

[RFC-0017] Matos, R. "Coffee-Break Protocol."
RFC 0017, OSC, 2001. https://rfc.osc.org/rfc0017

### 8.2 Informative

Argote, Linda, and Paul Ingram. 2000. "Knowledge Transfer."
*Org. Behavior and Human Decision Processes* 82 (1): 150-169.

Nonaka, Ikujiro, and Hirotaka Takeuchi. 1995. *The
Knowledge-Creating Company*. Oxford University Press.

Granovetter, Mark S. 1973. "The Strength of Weak Ties."
*American Journal of Sociology* 78 (6): 1360-1380.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-18 | R. Matos | Initial draft |

## Appendix B: Open Issues

1. **GFS Calibration**: Scoring unverifiable claims
   requires primary source access. [UNVERIFIED]

2. **Alpha Stability**: Whether coefficients hold across
   cultures. Longitudinal data needed. [UNVERIFIED]

3. **WSNR Thresholds**: Heuristic; validation pending.
   [UNVERIFIED]

---

> **Colophon**: The OSC does not exist. It is a fictional
> standards body for the Organizational Epistemology
> Project. RFCs under the OSC imprint are satirical
> artifacts encoding genuine organizational science.
> The watercooler is real -- and running WGVP since 1973.
