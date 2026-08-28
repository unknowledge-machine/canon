---
rfc: "0016"
title: "Institutional Memory Backup Specification"
stream: "Standards Track"
status: "DRAFT"
category: "Informational"
area: "knowledge-ops"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-18"
updated: "2026-08-07"
obsoletes: []
obsoleted_by: []
see_also: [7, 15]
keywords:
  - memory
  - backup
  - institutional
  - knowledge-preservation
  - turnover
  - documentation
abstract: |
  This document specifies the Institutional Memory Backup
  Protocol (IMBP), a formal framework for measuring and
  managing the backup of organizational knowledge. IMBP
  introduces Memory Backup Fidelity (MBF), Knowledge Decay
  Rate (KDR), Turnover Entropy Coefficient (TEC), and the
  Documentation Immune Response (DIR). The core finding is
  that organizations treat knowledge as ephemeral data that
  needs backup, but the backup process itself strips critical
  context — producing archives that are complete yet useless.
dual_layer: true
satire_notice: "satire"
---

# RFC-0016 — Institutional Memory Backup Specification

> **Satire Notice**: This document is published in the
> **Standards Track** stream. While technically coherent,
> its primary purpose is satirical illumination of how
> organizations mishandle knowledge preservation. The OSC
> does not recommend deploying IMBP without first backing
> up your backup strategy.

## 1. Introduction

Every organization experiences a recurring cycle: a valued
employee departs, taking irreplaceable context with them.
The remaining team discovers that "documentation" consists
of a README last updated eighteen months ago and a page
titled "Things Steve Knew." IMBP formalizes this cycle to
enable measurement, prediction, and mitigation of memory
loss. Organizations backup everything except what matters:
why decisions were made, what failed, and which hallway
conversations resolved conflicts no ticket ever captured.

## 2. Terminology

| Term | Definition |
|------|------------|
| **Institutional Memory** | Knowledge that exists nowhere in writing. |
| **Backup** | Copying knowledge to a location no one checks. |
| **MBF** | Memory Backup Fidelity — contextual transfer completeness. |
| **KDR** | Knowledge Decay Rate — speed of memory loss. |
| **TEC** | Turnover Entropy Coefficient — loss per departure. |
| **DIR** | Documentation Immune Response — recording resistance. |
| **Knowledge Graveyard** | A wiki space where documentation is forgotten. |
| **Negative Knowledge** | Knowledge of what was tried and failed. |

## 3. Protocol Specification

### 3.1 Memory Backup Fidelity (MBF)

MBF measures how much context survives a backup. It ranges
from 0 (no context preserved) to 1 (perfect transfer,
theoretical maximum never observed):

```
MBF = C_preserved / C_original
```

| Category | Typical MBF | Example |
|----------|-------------|---------|
| Explicit facts | 0.85 | API endpoints, config values |
| Decisions and rationale | 0.30 | "We chose X because Y" |
| Relationships and norms | 0.10 | Who approves what, who to ask |
| Negative knowledge | 0.05 | "We tried Z; it failed because..." |
| Emotional context | 0.00 | Why this deadline truly matters |

MBF degrades across backup generations. After N cycles:

```
MBF_effective(N) = MBF_initial * (1 - delta)^N
```

Empirical delta: 0.22 across 42 organizational case studies.

### 3.2 Knowledge Decay Rate (KDR)

KDR measures how fast institutional memory degrades after
the original holder departs:

```
KDR(t) = K_0 * e^(-lambda*t) + Sum(alpha_i * d(t - t_i))
```

| Knowledge Type | Half-Life | Time to Irrelevance |
|----------------|-----------|---------------------|
| Explicit procedures | 14 months | 36 months |
| Decision rationale | 6 weeks | 4 months |
| Relationship context | 3 weeks | 2 months |
| "Why this exists" | 1 week | 6 weeks |

When KDR drops below 0.3, the organization can no longer
distinguish institutional knowledge from institutional
mythology.

### 3.3 Turnover Entropy Coefficient (TEC)

TEC quantifies knowledge loss per employee departure:

```
TEC = (K_before - K_after) / K_total
```

**TEC Scaling by Role**:

| Role Category | TEC Multiplier | Rationale |
|---------------|----------------|-----------|
| IC (new hire) | 1.0x | Baseline loss |
| Senior IC | 2.5x | Deep domain knowledge |
| Tech Lead | 4.0x | Cross-cutting context |
| Manager | 3.0x | Relationship graph |
| "The person who knows" | 8.0x | Single point of failure |

**Aggregate TEC** for N departures in period T:

```
TEC_aggregate = Sum(TEC_i) / N * (1 + 0.5 * H)
```

Where H is the Herfindahl index of knowledge concentration.
When H > 0.7, the organization is one resignation from crisis.

### 3.4 Documentation Immune Response (DIR)

DIR measures an organization's resistance to recording
knowledge. High DIR indicates strong antibodies against
documentation:

```
DIR = (E_attempted / E_required) * (1 + R_friction)
```

**DIR Resistance Mechanisms**:

| Mechanism | Friction | Description |
|-----------|----------|-------------|
| "We don't have time" | 0.8 | Time allocation barrier |
| "It's obvious" | 0.9 | Tacit knowledge fallacy |
| "The wiki is outdated" | 0.7 | Tool decay spiral |
| "Ask Bob" | 1.0 | Knowledge personification |

**DIR Thresholds**:
- DIR < 0.3: Documentation culture exists (rare)
- DIR 0.3-0.6: Selective documentation (common)
- DIR 0.6-0.9: Documentation theater (very common)
- DIR > 0.9: Active knowledge hoarding (common)

## 4. Failure Modes

### 4.1 Backup Without Context
MBF approaches 0.05. Artifacts preserved; meaning lost.
Organization has 2,000 wiki pages and understands none of
them. Probability: 70%.

### 4.2 The Single Person of Failure
TEC > 0.6 for one individual. Departure triggers cascading
loss. "We need to document everything they know" is said,
then not done. Probability: 45%.

### 4.3 Documentation Theater
DIR > 0.8. Organization produces documentation that exists
to be counted, not read. Metrics show "95% coverage." No
one can find anything. Probability: 55%.

### 4.4 The Wiki Graveyard
KDR exceeds backup frequency. New documentation generated
faster than old is consumed. Knowledge graveyard grows
monotonically. Probability: 60%.

## 5. Security Considerations

Individuals with disproportionate knowledge (TEC multiplier
> 4.0) represent a resilience risk and a single point of
compromise. Mitigation: pair programming, rotating on-call,
knowledge-sharing mandates. Mandate effectiveness: low.
Backups may include sensitive information never classified
because it was never written down. Encryption must account
for tacit knowledge outside formal classification systems.

## 6. Performance Evaluation

| Metric | No-IMBP | With IMBP |
|--------|---------|-----------|
| Avg MBF | 0.12 | 0.35 |
| Avg KDR (months) | 2.1 | 4.8 |
| Avg TEC per departure | 0.42 | 0.28 |
| "Who knows?" lookup time | 3.2 days | 1.4 days |

Each senior departure costs 1.5-3x salary in knowledge
loss alone, excluding recruitment.

## 7. Extensions

| RFC | Title | Status |
|-----|-------|--------|
| 0007 | Organizational Amnesia Prevention | Published |
| 0008 | Tacit Knowledge Extraction | Published |
| 0009 | Knowledge Hoarding Incentive | Published |
| 0015 | Shadow Knowledge Networks | Planned |
| 0018 | Context-Aware Documentation | Planned |
| 0038 | External Memory Nodes (live, non-durable layer) | Draft (RFC-0038 §4.3.1) |

## 8. References

### 8.1 Normative References

[RFC-0007] Matos, R. "Organizational Amnesia Prevention." RFC 0007, OSC, 2026.
[RFC-0008] Matos, R. "Tacit Knowledge Extraction." RFC 0008, OSC, 2026.
[RFC-0015] Matos, R. "Shadow Knowledge Networks." RFC 0015, OSC, 2026.

### 8.2 Informative References

Nonaka, Ikujiro, and Hirotaka Takeuchi. 1995. *The
Knowledge-Creating Company*. Oxford University Press.
Davenport, Thomas H., and Laurence Prusak. 1998.
*Working Knowledge*. Harvard Business School Press.

## 9. Amendments

- 2026-08-07: **External Memory Nodes amendment.** Ratifies RFC-0038
  §4.3.1: external un-captured participants (volunteers, students,
  interns, retirees) extend IMBP as a *live, non-durable memory layer* —
  current knowledge held while present, never a permanent archive
  replacing MBF-backed durable backup. Two binding conditions:
  flow-not-tenure (RFC-0035 §3.3.2) and intern decoupling as a
  precondition, not a label property (Non-Capture, RFC-0035 Rule
  ESP-6). The extension belongs to IMBP, not OAPP: an external node's
  value is redundancy, not prevention (RFC-0007 §1.3, §1.4).

---

> **Colophon**: The Organizational Standards Consortium (OSC)
> does not exist. It is a fictional standards body created for
> the Organizational Epistemology Project (OEP). RFCs published
> under the OSC imprint are satirical artifacts that encode
> genuine organizational science. Your institutional memory,
> however, is already decaying — and no one backed it up.
