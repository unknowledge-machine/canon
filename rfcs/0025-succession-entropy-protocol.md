---
rfc: "0025"
title: "Succession Entropy Protocol (SEP)"
stream: "Humor"
status: "DRAFT"
category: "Informational"
area: "informal-networks"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-19"
updated: "2026-07-29"
obsoletes: []
obsoleted_by: []
see_also: [2, 3, 7, 9, 17, 23, 24, 26]
keywords: [succession, entropy, founder-decay,
  knowledge-transfer, voluntary-association, sinecura, chair-handoff]
abstract: |
  This document specifies the Succession Entropy Protocol (SEP), a
  formal model for the predictable degradation of organizational
  competence across leadership generations in voluntary associations
  (political parties, sports clubs, non-profits, standards bodies).
  SEP introduces the Founder Decay Factor (FDF), Ideology Drift (ID),
  Competence Half-Life (CHL), Structural Sinecura Index (SSI), and
  Behavioral Opportunism Index (BOI). A state machine governs the
  succession ceremony (Chair Handoff), and packet structures define
  knowledge-transfer attempts. Experimental evidence suggests that
  associations without explicit Promotion Gates (RFC-0023) and Trench
  Intelligence channels (RFC-0024) experience irreversible entropy
  within three generations.
dual_layer: true
satire_notice: "satire"
---

# RFC-0025 — Succession Entropy Protocol (SEP)

## Abstract

This document specifies the Succession Entropy Protocol (SEP), a
formal model for the predictable degradation of organizational
competence across leadership generations in voluntary associations
(political parties, sports clubs, non-profits, standards bodies).
SEP introduces the Founder Decay Factor (FDF), Ideology Drift (ID),
Competence Half-Life (CHL), Structural Sinecura Index (SSI), and
Behavioral Opportunism Index (BOI). A state machine governs the
succession ceremony (Chair Handoff), and packet structures define
knowledge-transfer attempts. Experimental evidence suggests that
associations without explicit Promotion Gates (RFC-0023) and Trench
Intelligence channels (RFC-0024) experience irreversible entropy
within three generations.

> **Satire Notice**: This document is published in the **Humor** stream.
> While technically coherent, its primary purpose is satirical
> illumination of organizational dynamics. The OSC does not recommend
> deploying SEP in production without IRB approval and a very
> comfortable chair.

## 1. Introduction

Every voluntary association begins with a founding cohort: individuals
who share an ideology, possess the competence to execute it, and
exhibit the charisma to attract followers. They write the statutes,
win the first elections, build the clubhouse, ship the first standard.

Then the founders retire, die, or drift away.

The second generation inherits the chair, the statutes, the
clubhouse — but not the founding knowledge stock. They never wrote
the statutes; they only interpret them. They never built the
clubhouse; they only maintain it. They never fought the founding
battles; they only reenact the rituals.

By the third generation, the association operates on chair sits someone whose primary
qualification is willingness to sit in it. The ideology has drifted
into slogans. Competence has halved twice. The Structural Sinecura
Index exceeds the threshold where the chair becomes a career rather
than a duty.

SEP formalizes this trajectory.

## 2. Terminology

| Term | Definition |
|------|------------|
| **Voluntary Association (VA)** | Any organization joined by choice: party, club, NGO, standards body, open-source project |
| **Founding Cohort** | Initial members who create the VA's purpose, statutes, and initial successes |
| **Founder Knowledge Stock (FKS)** | Tacit knowledge held by founders: unwritten precedents, personal networks, oral history, crisis heuristics |
| **Generation** | One complete succession cycle: chair term + transition |
| **Chair** | Leadership position (president, chair, captain, BDFL) — the seat of authority |
| **Succession Ceremony** | Ritual transfer of chair authority (election, appointment, acclamation) |
| **Chair Handoff** | Physical/symbolic transfer artifact (gavel, badge, repository keys, captain's armband) |
| **Sinecura** | Position requiring minimal work, providing status/income — the chair as career |
| **Promotion Gate** | RFC-0023 mechanism: explicit decision point for role advancement |

## 3. Protocol Specification

### 3.1 Founder Decay Factor (FDF)

FDF quantifies the fraction of Founder Knowledge Stock remaining
after *g* generations:

```
FDF(g) = e^(-λ·g)
```

Where:
- `g` = generation number (0 = founding cohort, 1 = first succession, ...)
- `λ` = decay constant (empirically: 0.5–0.8 for VAs without Promotion Gates)

**Interpretation**:

| Generation | FDF (λ=0.69) | FKS Remaining |
|------------|--------------|---------------|
| 0 (founders) | 1.00 | 100% |
| 1 | 0.50 | 50% |
| 2 | 0.25 | 25% |
| 3 | 0.125 | 12.5% |

At g=3, the chair operates with <15% of founding tacit knowledge.

### 3.2 Ideology Drift (ID)

ID measures semantic divergence between founding manifesto and current
operational doctrine:

```
ID(g) = D_KL( P_founding || P_current(g) )
```

Where:
- `P_founding` = term distribution in founding documents
- `P_current(g)` = term distribution in current statutes/speeches/decisions
- `D_KL` = Kullback-Leibler divergence

**Thresholds**:

| ID Range | Classification |
|----------|----------------|
| ID < 0.1 | Faithful |
| 0.1 ≤ ID < 0.5 | Interpretive drift |
| 0.5 ≤ ID < 1.0 | Sloganization |
| ID ≥ 1.0 | Inversion (doctrine contradicts founding) |

### 3.3 Competence Half-Life (CHL)

CHL is the number of generations for median chair competence to fall
to 50% of founding cohort level:

```
CHL = ln(2) / λ
```

Where `λ` is the FDF decay constant. Without explicit knowledge
transfer mechanisms (Promotion Gates, RFC-0023), `CHL ≈ 1` generation.

With Promotion Gates + Trench Intelligence (RFC-0024): `CHL ≥ 3`.

### 3.4 Structural Sinecura Index (SSI)

SSI measures statutory incentives for chair occupancy as career:

```
SSI = (T_tenure × C_compensation × P_perks) /
      (A_accountability × K_knowledge_requirement)
```

Where:
- `T_tenure` = max term length × renewable terms
- `C_compensation` = salary + expenses / median member income
- `P_perks` = perks score (0–1: car, office, staff, immunity)
- `A_accountability` = direct recall (0–1: simple = 1)
- `K_knowledge_requirement` = demonstrated competence threshold (0–1)

**SSI Interpretation**:

| SSI Range | Chair Type |
|-----------|------------|
| SSI < 1 | Duty (low reward, high accountability) |
| 1 ≤ SSI < 5 | Mixed (honorarium + duty) |
| 5 ≤ SSI < 20 | Attractive (career-compatible) |
| SSI ≥ 20 | Sinecura (career destination) |

### 3.5 Behavioral Opportunism Index (BOI)

BOI measures individual motivation independent of structure:

```
BOI = (E_effort_avoidance × S_status_seeking × I_income_need) /
      C_competence_demonstrated
```

Where all factors normalized 0–1. BOI > 2 predicts sinecura-seeking
behavior regardless of SSI.

### 3.6 Composite: Succession Entropy (SE)

```
SE(g) = FDF(g)⁻¹ × ID(g) × (1 + SSI) × (1 + BOI_avg)
```

Where `BOI_avg` = median BOI of chair candidates in generation g.

**SE Thresholds**:

| SE Range | VA State |
|----------|----------|
| SE < 2 | Healthy (founder energy dominant) |
| 2 ≤ SE < 10 | Managed drift (institutions compensate) |
| 10 ≤ SE < 50 | Crisis (chair churn, factionalism) |
| SE ≥ 50 | Zombie VA (statutes exist, purpose extinct) |

### 3.7 SEP State Machine

Voluntary associations traverse a deterministic succession lifecycle:

```
         ┌─────────────────────────────────────────────────┐
         │                                                 │
         ▼                                                 │
    ┌──────────┐  founding_act  ┌──────────────┐           │
    │ DORMANT  │ ─────────────► │ FOUNDING     │           │
    └──────────┘                └──────────────┘           │
         ▲                      │       │                  │
         │                      │       │                  │
         │    dissolution       │       │                  │
         │◄─────────────────────┘       │                  │
         │                            succession_trigger   │
         │                              │                  │
         │                    ┌─────────┴─────────┐        │
         │                    ▼                   ▼        │
         │             ┌──────────┐         ┌────────────┐ │
         │             │CONSOLID- │         │ SUCCESSION │ │
         │             │ATION     │         │ CRISIS     │ │
         │             └──────────┘         └────────────┘ │
         │                   │                  │          │
         │         knowledge_transfer       chair_handoff  │
         │                   │                  │          │
         │                   ▼                  ▼          │
         │             ┌──────────────┐   ┌──────────────┐ │
         │             │ RENEWAL   ◄──┘   │ DEGENERATION │ │
         │             └──────────────┘   └──────────────┘ │
         │                   │                  │          │
         │         promotion_gate         entropy_threshold│
         │                   │                  │          │
         └───────────────────┴──────────────────┘          │
                              │                            │
                              ▼                            │
                         ┌──────────────┐                  │
                         │ REFOUNDING   │                  │
                         │ (new cycle)  │                  │
                         └──────────────┘                  │
```

**State Definitions**:

| State | Duration | Exit Condition |
|-------|----------|----------------|
| DORMANT | Pre-founding | Founding act signed |
| FOUNDING | 0–g=1 | First succession trigger |
| CONSOLIDATION | g=1–2 | Founder retirement |
| SUCCESSION_CRISIS | g=2–3 | Chair vacancy + contested |
| RENEWAL | Variable | Promotion Gate passed |
| DEGENERATION | Variable | SE ≥ 50 |
| REFOUNDING | Variable | New founding cohort emerges |

### 3.8 SEP Packet Structure

SEP defines packets for succession ceremony coordination:

```
SEP_SYN (Succession Challenge):
  type: "syn"
  va_id: string
  generation: integer
  challenger_id: string
  challenger_fks_estimate: float (0-1)
  challenger_boi: float
  manifesto_delta: float (ID vs founding)

SEP_ACK (Mandate Grant):
  type: "ack"
  va_id: string
  generation: integer
  chair_id: string
  mandate_source: "election" | "appointment" | "acclamation" | "coup"
  fdf_at_handoff: float
  ssia_approved: boolean (Promotion Gate check)

SEP_DATA (Knowledge Transfer):
  type: "data"
  va_id: string
  generation: integer
  from_chair: string
  to_chair: string
  fks_artifacts: string[] (oral history, precedent docs, network maps)
  transfer_efficiency: float (0-1)
  trench_intelligence_used: boolean (RFC-0024 channel)

SEP_FIN (Term End):
  type: "fin"
  va_id: string
  generation: integer
  chair_id: string
  term_duration: integer
  fdf_at_exit: float
  id_at_exit: float
  legacy_artifacts: string[]

SEP_ABORT (Coup / Forced Exit):
  type: "abort"
  va_id: string
  generation: integer
  ousted_chair: string
  usurper_id: string
  justification: "incompetence" | "corruption" | "ideology_drift" |
    "health" | "ambition"
  fdf_loss: float
```

### 3.9 Visual Primitive: Chair Handoff

The Chair Handoff is the SEP equivalent of RFC-0017's Visual Primitive.
It is the line-of-sight ceremony where authority visibly transfers.

**Requirements**:

- Both outgoing and incoming chair present
- Physical artifact transferred (gavel, badge, armband, repository keys)
- Verbal acknowledgment: "I transfer the chair" / "I accept the chair"
- Witness quorum ≥ 2/3 of governing body

**Failure Modes**:

| Failure | Cause | Fallback |
|---------|-------|----------|
| Artifact lost | No gavel/badge/keys | Verbal handoff + written record |
| Outgoing refuses | Resentment, coup | SEP_ABORT packet |
| Incoming absent | Ambition without presence | SEP_ABORT (coup) |
| No quorum | Factional boycott | DEGENERATION state |

## 4. Failure Modes (Extended)

### 4.1 Founder Ghost Protocol
Founder refuses to retire, attends all meetings, vetoes decisions.
**Mitigation**: Statutory term limits + RFC-0023 Promotion Gate
for "Founder Emeritus" role (advisory, no vote).

### 4.2 Shadow Chair
Real power held by unelected advisor (spouse, aide, funder).
**Mitigation**: RFC-0024 Trench Intelligence — map actual vs. formal influence.

### 4.3 Factional Fork
VA splits into two chairs claiming legitimacy.
**Protocol**: SEP_ABORT with `justification: "ideology_drift"`. Both forks get new VA_ID.

### 4.4 Competence Vacuum
No candidate meets minimum FKS threshold.
**Result**: VA enters DEGENERATION. External administrator appointed (RFC-0001 HOP intervention).

### 4.5 Statutory Capture
Bylaws amended to increase SSI (longer terms, higher pay, weaker recall).
**Detection**: Monitor SSI delta per generation. ΔSSI > 2 → ALERT.

## 5. Security Considerations

### 5.1 Chair Handoff Spoofing
Adversary mimics handoff ceremony to claim chair.
**Mitigation**: Multi-factor — artifact + verbal + quorum + cryptographic seal (for digital VAs).

### 5.2 Ideology Drift as Attack Vector
Adversary joins VA, rises through generations, gradually inverts doctrine.
**Mitigation**: ID monitoring (quarterly KL-divergence audit).
ID > 0.5 triggers RFC-0023 Promotion Gate review.

### 5.3 Sinecura Entrenchment
Chair amends statutes to raise SSI irreversibly.
**Mitigation**: Constitutional clause: SSI amendments require 90% supermajority + external audit.

## 6. Performance Evaluation

### 6.1 SEP Overhead Analysis

| Phase | Avg Duration | Success Rate |
|-------|--------------|--------------|
| Chair Handoff (ceremony) | 30 min | 95% (if quorum) |
| Knowledge Transfer | 0–6 months | 40% (without RFC-0023) |
| Ideology Audit (KL-div) | 2 weeks | 80% |
| Promotion Gate | 1–3 months | 60% (if SSI < 5) |

### 6.2 Competence vs. Coordination Cost

| VA Type | CHL (generations) | Coordination Cost | SE at g=3 |
|---------|-------------------|-------------------|-----------|
| Party (high SSI) | 0.8 | High | 45 (Crisis) |
| Sports club (low SSI) | 1.5 | Medium | 12 (Managed) |
| Standards body (RFC-0023) | 3.0 | Low | 3 (Healthy) |
| Open-source (BDFL) | Variable | Low | Depends on fork policy |

## 7. Extensions

| RFC | Title | Status |
|-----|-------|--------|
| 0023 | Promotion Gate Protocol | DRAFT |
| 0024 | Trench Intelligence Protocol | DRAFT |
| 0026 | Wernham Hogg Protocol | DRAFT |
| 0027 | Sinecura Extraction Protocol | Planned |

## 8. References

### 8.1 Normative References

[RFC-0002] Matos, R. "Conway's Law Generalization Protocol." RFC 0002, OSC, 1989.

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003, OSC, 1992.

[RFC-0007] Matos, R. "Organizational Amnesia Prevention Protocol (OAPP)." RFC 0007, OSC, 2026.

[RFC-0009] Matos, R. "Knowledge Hoarding Incentive Structure (KHIS)." RFC 0009, OSC, 2026.

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017, OSC, 2001.

[RFC-0023] Matos, R. "Promotion Gate Protocol (PGP)." RFC 0023, OSC, 2026.

[RFC-0024] Matos, R. "Trench Intelligence Protocol (TIP)." RFC 0024, OSC, 2026.

[RFC-0026] Matos, R. "Wernham Hogg Protocol." RFC 0026, OSC, 2026.

### 8.2 Informative References

Olson, Mancur. 1965. *The Logic of Collective Action*. Harvard UP.

Michels, Robert. 1911. *Political Parties: A Sociological
Study of the Oligarchical Tendencies of Modern Democracy*.
Free Press.

Kanter, Rosabeth Moss. 1977. *Men and Women of the Corporation*. Basic Books.

Tushman, Michael L., and Romanelli, Elaine. 1985.
"Organizational Evolution: A Metamorphosis Model of
Convergence and Reorientation." *Research in Organizational
Behavior* 7: 171–222.

---

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-19 | R. Matos | Initial draft |

## Appendix B: Open Issues

1. **SEP-001**: Calibrate λ for different VA types (party vs. club vs. standards body).
2. **SEP-002**: Define "Chair Handoff" cryptographic seal for digital VAs (GitHub orgs, DAOs).
3. **SEP-003**: Model BOI as stochastic process — can it be screened pre-candidacy?
4. **SEP-004**: Does RFC-0017 CBP reduce SE? (Coffee breaks as trench intelligence channels)

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Olson, Michels, Kanter, Tushman, etc.) are
> accurate. The chair, however, is real — and it is currently occupied by
> someone who has never read the statutes.
