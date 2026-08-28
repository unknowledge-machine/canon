---
rfc: "0026"
title: "Wernham Hogg Protocol (WHP)"
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
see_also: [1, 2, 3, 7, 11, 14, 17, 23, 24, 25]
keywords: [wernham-hogg, office-epistemology, brent-effect,
  prank-war, chair-swivel, that's-what-she-said, avô-rico]
abstract: |
  This document specifies the Wernham Hogg Protocol (WHP), the foundational
  epistemic protocol for office-based organizations. WHP models the office
  as a bounded knowledge domain where productivity is inversely proportional
  to meeting density, where the swivel chair is a communication primitive,
  and where the phrase "that's what she said" functions as a semantic
  error-correction mechanism. WHP introduces the Brent Effect (charisma
  compensating for competence), the Prank War Equilibrium, and the
  Avô-Rico-Pai-Nobre-Filho-Pobre generational decay function. WHP is the
  ground-truth layer upon which RFC-0017 (CBP), RFC-0023 (PGP), and
  See also: 25 (SEP) operate.
dual_layer: true
satire_notice: "satire"
---

# RFC-0026 — Wernham Hogg Protocol (WHP)

## Abstract

This document specifies the Wernham Hogg Protocol (WHP), the foundational
epistemic protocol for office-based organizations. WHP models the office
as a bounded knowledge domain where productivity is inversely proportional
to meeting density, where the swivel chair is a communication primitive,
and where the phrase "that's what she said" functions as a semantic
error-correction mechanism. WHP introduces the Brent Effect (charisma
compensating for competence), the Prank War Equilibrium, and the
Avô-Rico-Pai-Nobre-Filho-Pobre generational decay function. WHP is the
ground-truth layer upon which RFC-0017 (CBP), RFC-0023 (PGP), and
See also: 25 (SEP) operate.

> **Satire Notice**: This document is published in the **Humor** stream.
> While technically coherent, its primary purpose is satirical
> illumination of office dynamics. The OSC does not recommend deploying
> WHP in production without IRB approval, a competent receptionist,
> and a very good mug.

## 1. Introduction

The office is not a workplace. The office is a knowledge ecosystem
where the primary output is not product but *the appearance of work*.
WHP formalizes the epistemic structure of this ecosystem.

The office has three strata:
- **The Floor** — where work (allegedly) happens
- **The Glass Office** — where management observes without seeing
- **The Kitchen** — where truth is exchanged (CBP layer, RFC-0017)

WHP specifies the protocols governing knowledge flow between these
strata, the error-correction mechanisms that prevent total epistemic
collapse, and the generational decay that dooms every office to
irrelevance.

## 2. Terminology

| Term | Definition |
|------|------------|
| **Branch** | Local office instance (Slough, Scranton, Wernham Hogg) |
| **Regional Manager** | Local authority node (Brent/David/Michael archetype) |
| **Assistant to the Regional Manager** | Non-existent role claimed by sycophant |
| **Swivel Chair** | Primary communication primitive (rotation = attention) |
| **That's What She Said (TWSS)** | Semantic error-correction tag |
| **Brent Effect** | Charisma × Incompetence > Competence × Humility |
| **Prank War** | Asymmetric conflict using office supplies as weapons |
| **Avô-Rico-Pai-Nobre-Filho-Pobre** | Three-generation competence decay function |
| **Chair Swivel Rate (CSR)** | Rotations per hour — proxy for engagement |
| **Meeting Density (MD)** | Meetings per productive hour |

## 3. Protocol Specification

### 3.1 The Brent Effect

The Brent Effect quantifies the organizational paradox where the
least competent individual achieves the highest visibility through
performative confidence.

```
BE = (C × V) / (K × H)
```

Where:
- `C` = Charisma (0-10, self-reported)
- `V` = Visibility (meetings chaired per week)
- `K` = Actual competence (peer-assessed, 0-10)
- `H` = Humility (inverse of self-nomination frequency)

**Brent Effect Thresholds**:
| BE Range | Classification | Outcome |
|----------|---------------|---------|
| BE < 0.5 | Competent Invisible | Does the work, gets no credit |
| 0.5 ≤ BE < 2.0 | Balanced | Healthy organization |
| 2.0 ≤ BE < 5.0 | Brent Zone | Manager mistakes confidence for competence |
| BE ≥ 5.0 | Wernham Hogg Singularity | Reality detaches from performance |

**Corollary**: The Regional Manager is always in the Brent Zone.
If not, they are promoted to Regional Director (removing them from
the floor where they could cause harm).

### 3.2 The Swivel Chair Primitive

The swivel chair is the office's Visual Primitive (RFC-0017 §3.5).
Unlike the coffee machine (CBP), the swivel chair operates at
desk-level, enabling micro-synchronization without leaving the
"productivity theater."

**Protocol**:
```
Worker A: [swivels 90°] → [makes eye contact] → [holds 300ms]
    ↓
Worker B: [detects] → [swivels 90°] → [nods] → [holds 300ms]
    ↓
MICRO_SYNC_ESTABLISHED
```

**Parameters**:
- Swivel angle: 90° ± 15° (180° = "I'm leaving"; 45° = "not interested")
- Hold duration: 300ms minimum (below = nervous tic)
- Maximum CSR: 12 rotations/hour (above = "distracted")

**Failure Modes**:
| Failure | Cause | Fallback |
|---------|-------|----------|
| Chair locked | Cheap procurement | Explicit verbal sync |
| No eye contact | Dual monitors | Slack DM |
| Swivel stuck | Gum in mechanism | Standup meeting |

### 3.3 That's What She Said (TWSS) — Semantic Error Correction

TWSS functions as a protocol-level checksum. When a statement
accidentally contains sexual innuendo, TWSS tags it, allowing both
parties to acknowledge the ambiguity without losing face.

**Packet Structure**:
```
TWSS_PACKET:
  trigger: string (original statement)
  tag: "that's what she said"
  latency: < 500ms (must be immediate)
  delivery: deadpan
```

**Error Correction Logic**:
1. Statement S uttered with accidental double entendre
2. TWSS tag applied within 500ms
3. Both parties laugh → tension released
4. Conversation resumes on literal track

**Failure Mode**: TWSS latency > 2s → becomes harassment.
**Mitigation**: Automatic TWSS timeout (RFC-0017 SUSPICION adaptation).

### 3.4 Prank War Equilibrium (PWE)

Prank wars are asymmetric conflicts where office supplies become
weapons. PWE models the Nash equilibrium where neither party
escalates to HR.

**State Machine**:
```
PEACE
  |
  v (stapler in jelly)
ESCALATION_1
  |
  v (mouse wrapped in tape)
ESCALATION_2
  |
  v (desk wrapped in clingfilm)
MUTUALLY_ASSURED_DESTRUCTION
  |
  v (HR email)
HR_INTERVENTION
  |
  v
PEACE (with treaty)
```

**PWE Parameters**:
- Maximum escalation depth: 3 (beyond = HR)
- Weapon cost ceiling: £5 (stapler, jelly, tape, clingfilm)
- Duration limit: 1 week (longer = obsession)
- Truce mechanism: Shared tea round

### 3.5 Avô-Rico-Pai-Nobre-Filho-Pobre Generational Decay

The three-generation decay function, known in Portuguese organizational
folklore as "Avô rico, pai nobre, filho pobre" (Grandfather rich,
father noble, son poor).

```
Generation 0 (Avô): Founder — builds wealth, knows every brick
Generation 1 (Pai): Heir — maintains wealth, knows the stories
Generation 2 (Filho): Squanderer — spends wealth, knows the myths
Generation 3: Bankruptcy / Acquisition / Merger
```

**Decay Function**:
```
Competence(g) = C₀ × e^(-λg) × (1 - σg)
```

Where:
- `C₀` = Founder competence (baseline 10)
- `λ` = Knowledge half-life (empirically: 0.69 per generation)
- `σ` = Sinecura accumulation rate (0.1 per generation)
- `g` = Generation index (0, 1, 2, ...)

**Thresholds**:
| Generation | Competence | Classification |
|------------|------------|----------------|
| 0 (Avô) | 10.0 | Founder — builds |
| 1 (Pai) | 5.0 | Heir — maintains |
| 2 (Filho) | 1.8 | Squanderer — performs |
| 3 | 0.4 | Bankrupt / Acquired |

**SEP Integration (See also: 25)**: This is the organizational form of
Succession Entropy Protocol. The "Filho" generation is where SEP's
CHL (Competence Half-Life) crosses below the Sinecura Threshold.

### 3.6 Chair Swivel Rate (CSR) as Productivity Proxy

CSR correlates inversely with actual output:

```
Productivity = P₀ / (1 + α × CSR + β × MD)
```

Where:
- `P₀` = Baseline productivity (isolated worker)
- `α` = Swivel distraction coefficient (0.15)
- `β` = Meeting density coefficient (0.40)
- `CSR` = Chair Swivel Rate (rotations/hour)
- `MD` = Meeting Density (meetings/productive_hour)

**Empirical Data** (Slough branch, 2001-2003):
| Role | Avg CSR | Avg MD | Relative Output |
|------|---------|--------|-----------------|
| Sales (Tim) | 8/hr | 0.2 | 1.0x (baseline) |
| Reception (Dawn) | 12/hr | 0.1 | 0.9x |
| Accountant (Kevin) | 3/hr | 0.05 | 1.4x |
| Regional Manager (David) | 22/hr | 4.0 | 0.1x |
| Assistant to RM (Gareth) | 15/hr | 2.0 | 0.3x |

### 3.7 WHP Packet Formats

**WHP_SYN** (Initiate micro-sync):
```
type: "syn"
source_desk: string
swivel_angle: int (45-180)
payload: "alright?" | "busy?" | "tea?"
```

**WHP_ACK** (Acknowledge):
```
type: "ack"
target_desk: string
swivel_angle: int
payload: "yeah" | "sec" | "brew?"
```

**WHP_TWSS** (Error correction):
```
type: "twss"
trigger_hash: string (SHA-256 of trigger phrase)
latency_ms: int (< 500)
deadpan: boolean
```

**WHP_PRANK** (Escalation):
```
type: "prank"
weapon: "stapler_jelly" | "mouse_tape" | "desk_clingfilm" | "keyboard_swap"
escalation_level: 1-3
truce_offered: boolean
```

## 4. Failure Modes

### 4.1 The Michael Scott Singularity
Regional Manager achieves BE > 10. Reality fully detaches.
**Symptoms**: "I declare bankruptcy" spoken aloud; CPR dummy
resuscitation during safety training; "That's what she said"
at funeral.
**Mitigation**: Camera crew presence increases self-awareness by 40%.

### 4.2 Prank War Nuclear Escalation
Escalation depth > 3 or weapon cost > £50.
**Symptoms**: Car wrapped in post-its; server room filled with
balloons; HR receives anonymous complaint from "Brent".
**Mitigation**: Mandatory tea round treaty.

### 4.3 TWSS Timeout Cascade
TWSS latency > 2s across floor → everything becomes innuendo.
**Symptoms**: "Hard drive" → TWSS; "Insert the disk" → TWSS;
"Pull the plug" → TWSS.
**Mitigation**: Automatic TWSS suppression after 3 consecutive.

### 4.4 Generational Collapse (Avô-Rico-Pai-Nobre-Filho-Pobre)
Generation 3 competence < 1.0 → branch closure or acquisition.
**Symptoms**: Founder's portrait turned to wall; statutes used
as coasters; client list sold to competitor.
**Mitigation**: External acquisition (Staples / Sabre / NBC).

## 5. Security Considerations

### 5.1 Brent Effect Exploitation
Adversary promotes high-BE individual to management to degrade
organizational output.
**Countermeasure**: Competence-assessment gate before promotion
(RFC-0023 Promotion Gate).

### 5.2 Prank War Supply Chain Attack
Adversary contaminates jelly with non-food substance.
**Countermeasure**: Stapler serialization; jelly batch tracking.

### 5.3 TWSS as Covert Channel
Malicious actor encodes data in TWSS timing patterns.
**Countermeasure**: TWSS rate limiting (max 1/min per desk).

### 5.4 Chair Swivel Surveillance
CSR monitoring used for productivity surveillance.
**Countermeasure**: Swivel privacy mode (lock at 0°).

## 6. Performance Evaluation

| Metric | Slough (2001) | Scranton (2005) | Target |
|--------|---------------|-----------------|--------|
| Avg BE | 3.2 | 4.1 | < 2.0 |
| PWE Duration | 6 days | 4 days | < 7 days |
| TWSS Latency | 320ms | 410ms | < 500ms |
| CSR (floor avg) | 11/hr | 14/hr | < 10/hr |
| Generational Competence (g=2) | 1.8 | 2.1 | > 3.0 |

## 7. Extensions

| RFC | Title | Status |
|-----|-------|--------|
| 0017 | Coffee-Break Protocol (CBP) | Active |
| 0023 | Promotion Gate Protocol (PGP) | Active |
| 0024 | Trench Intelligence Protocol (TIP) | Active |
| 0025 | Succession Entropy Protocol (SEP) | Active |
| 0026 | Dundie Awards Specification | Planned |
| 0027 | Fire Drill Protocol | Planned |

## 8. References

### 8.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001.
[RFC-0002] Matos, R. "Conway's Law Generalization Protocol." RFC 0002.
[RFC-0007] Matos, R. "Organizational Amnesia Prevention Protocol." RFC 0007.
[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017.
[RFC-0023] Matos, R. "Promotion Gate Protocol (PGP)." RFC 0023.
[RFC-0024] Matos, R. "Trench Intelligence Protocol (TIP)." RFC 0024.
[See also: 25] Matos, R. "Succession Entropy Protocol (SEP)." RFC 0025.

### 8.2 Informative References

Gervais, R. & Merchant, S. 2001. *The Office* (BBC). Wernham Hogg Paper.
Gervais, R. & Merchant, S. 2005. *The Office* (NBC). Dunder Mifflin Paper.
Lamb, C. 2006. *The IT Crowd* (Channel 4). Reynholm Industries.
Portuguese Folklore. "Avô rico, pai nobre, filho pobre." Organizational
proverb, unattributed.

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs published under the OSC imprint are satirical artifacts
> that encode genuine organizational science. The office, however, is real —
> and somewhere, right now, a swivel chair is rotating 90 degrees,
> holding for 300ms, establishing a micro-sync that does actual work.