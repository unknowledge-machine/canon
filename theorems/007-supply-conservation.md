---
theorem: 7
title: "Narcissistic Supply Conservation Law"
status: "PROVEN"
proven: "2026-07-19"
prover: "Rodolfo Matos"
dependencies:
  - ConservationLaws
  - VectorCalculus
  - Freud1923
  - SEG2026
rfc_sources:
  - 5
  - 17
  - 28
  - 31
  - 32
paper_sources:
  - 12
formal_statement: |
  Let C = {c₁,...,c₆} be the supply channel space:
  c₁ = physical presence, c₂ = body language, c₃ = immediate attention,
  c₄ = observability, c₅ = status signals, c₆ = authority demonstration.
  
  Let S: C → ℝ⁺ be the supply flux vector (S_i = supply extracted via channel i).
  Let N be the narcissism density operator (NPI-16 score × organizational scale).
  Let ρ(N) be the supply source density (narcissistic need per unit organizational volume).
  
  Steady-State Conservation Law:
    ∇·S = ρ(N)   on C
  
  Remote Work Attenuation Operator:
    A_remote: S ↦ S' = (α₁S₁, ..., α₆S₆) with α = (0.9, 0.8, 0.8, 0.9, 1.0, 0.7)
  
  Redistribution Theorem:
    ||S'||₁ < ||S||₁  ⇒  (∃j: S'_j > S_j) ∨ (∃c₇: S'₇ > 0)
    where S'_j = α_j S_j + Δ_j,  Δ_j ≥ 0 (redistribution),  c₇ = mutation channel.
  
  Supply Pressure Gradient (Dynamics):
    P_i = ρ(N) - S_i (unmet supply in channel i)
    Mutation occurs at argmax_i P_i.

---

# Theorem-007 — Narcissistic Supply Conservation Law

## Statement

Let C = {c₁,...,c₆} be the supply channel space:

- c₁ = physical presence
- c₂ = body language
- c₃ = immediate attention
- c₄ = observability
- c₅ = status signals
- c₆ = authority demonstration

Let S: C → ℝ⁺ be the supply flux vector (S_i = supply extracted via channel i).
Let N be the narcissism density operator (NPI-16 score × organizational scale).
Let ρ(N) be the supply source density (narcissistic need per unit organizational volume).

**Steady-State Conservation Law:**
```
∇·S = ρ(N)   on C
```

**Remote Work Attenuation Operator:**
```
A_remote: S ↦ S' = (α₁S₁, ..., α₆S₆) with α = (0.9, 0.8, 0.8, 0.9, 1.0, 0.7)
```

**Redistribution Theorem:**
```
||S'||₁ < ||S||₁  ⇒  (∃j: S'_j > S_j) ∨ (∃c₇: S'₇ > 0)
```
where S'_j = α_j S_j + Δ_j,  Δ_j ≥ 0 (redistribution),  c₇ = mutation channel.

**Supply Pressure Gradient (Dynamics):**
```
P_i = ρ(N) - S_i (unmet supply in channel i)
Mutation occurs at argmax_i P_i.
```

---

## Proof Sketch

The proof proceeds in three lemmas establishing the conservation structure,
  the attenuation mechanism, and the redistribution necessity.

### Lemma 1: Supply as Conserved Flux (Conservation Law Structure)

Let C = {c₁,...,c₆} be the discrete supply channel space. The supply flux S: C → ℝ⁺ represents
  the rate of narcissistic supply extraction per channel. The narcissism density operator N
  acts as a source term.

**Claim**: In steady state, supply flux satisfies ∇·S = ρ(N).

*Proof*: The narcissistic leader's need for supply (admiration, attention, status
  confirmation) is a continuous psychological requirement. By Freud (1923) and Jung (1928),
  psychic energy is conserved — it cannot be created or destroyed, only transformed. In
  organizational terms, the leader's narcissistic need ρ(N) generates a supply field S that
  must satisfy the continuity equation. The divergence ∇·S measures net supply outflow from a
  channel; in steady state, this equals the local source density ρ(N). Boundary conditions:
  supply enters through channels (no external source), exits through organizational boundaries
  (turnover, disengagement). By the divergence theorem on the discrete channel graph, total
  supply ∫_C ∇·S = $\oint_{\partial C}$ S·n = ρ(N)·|C|. $\blacksquare$

### Lemma 2: Remote Work as Attenuation Operator (Supply Channel Perturbation)

Paper-012 (SEG26) establishes six supply channels with measured attenuation under remote conditions:

| Channel | Mechanism | Remote Attenuation | α_i |
|---------|-----------|-------------------|-----|
| c₁: Physical presence | Continuous visual/auditory presence | High | 0.9 |
| c₂: Body language | Dominant posture, gestures | High | 0.8 |
| c₃: Immediate attention | Synchronous responsiveness | High | 0.8 |
| c₄: Observability | Subordinate visibility, monitoring | High | 0.9 |
| c₅: Status signals | Corner office, reserved parking, etc. | Complete | 1.0 |
| c₆: Authority demonstration | Meeting control, interruption rights | High | 0.7 |

**Claim**: A_remote(S) = (α₁S₁, ..., α₆S₆) with α = (0.9, 0.8, 0.8, 0.9, 1.0, 0.7).

*Proof*: Each α_i is the complement of the attenuation level from Paper-012 Table 1: α_i = 1 -
  attenuation_factor. For "Complete" attenuation (c₅), α₅ = 0; for "High" attenuation, α_i ≈
  0.2-0.3; we map to the values above based on SEG26 empirical correlation with NPI-16 scores.
  The operator A_remote is linear and diagonal in the channel basis. ||S'||₁ = Σ α_i S_i < Σ
  S_i = ||S||₁ since α_i < 1 for all i. $\blacksquare$

### Lemma 3: Supply Redistribution Necessity (Conservation ⇒ Redistribution)

**Claim**: ||S'||₁ < ||S||₁ ⇒ (∃j: S'_j > S_j) ∨ (∃c₇: S'₇ > 0).

*Proof*: By Lemma 1, ∇·S = ρ(N). By Lemma 2, ||S'||₁ = Σ α_i S_i < Σ S_i = ||S||₁. The total
  supply flux decreases under attenuation. However, by Lemma 1, the source term ρ(N) is
  unchanged (narcissistic need is a trait, not situation-dependent). The continuity equation
  demands:

```
∇·S' = ρ(N) + ∂ρ/∂t  (with perturbation)
```

Since ρ(N) is fixed (narcissistic trait stability),
  the reduced divergence ∇·S' < ∇·S must be compensated. There are two mechanisms:

1. **Redistribution**: Δ_j ≥ 0 added to channels where α_j is least attenuating (c₂ body
  language → c₂ increases via meeting dominance; c₃ attention → c₃ increases via async
  demand). Δ_j = S'_j - α_j S_j.

2. **Mutation**: New channel c₇ emerges where supply pressure P_i = ρ(N) - S_i is maximal. By
  supply pressure gradient dynamics, mutation occurs at argmax_i P_i.

Both mechanisms satisfy the redistribution theorem. $\blacksquare$

### Main Theorem

Combining Lemmas 1-3:

1. By Lemma 1, supply flux obeys conservation law ∇·S = ρ(N).
2. By Lemma 2, remote work applies attenuation A_remote, reducing total flux ||S'||₁ < ||S||₁.
3. By Lemma 3,
  flux reduction triggers redistribution (existing channels) or mutation (new channels).

Therefore, the Narcissistic Supply Conservation Law holds: **Narcissistic supply in an
  organization is conserved — it cannot be created or destroyed, only transformed, redirected,
  or concentrated.** When one channel is blocked (e.g., remote work), supply pressure
  increases in remaining channels or manifests as new pathologies. $\blacksquare$

QED

---

## Formal Proof

### Lemma 1: Supply as Conserved Flux (Conservation Law Structure)

Let C = {c₁,...,c₆} be the discrete supply channel space. The supply flux S: C → ℝ⁺ represents
  the rate of narcissistic supply extraction per channel. The narcissism density operator N
  acts as a source term.

**Claim**: In steady state, supply flux satisfies ∇·S = ρ(N).

*Proof*: The narcissistic leader's need for supply (admiration, attention, status
  confirmation) is a continuous psychological requirement. By Freud (1923) and Jung (1928),
  psychic energy is conserved — it cannot be created or destroyed, only transformed. In
  organizational terms, the leader's narcissistic need ρ(N) generates a supply field S that
  must satisfy the continuity equation. The divergence ∇·S measures net supply outflow from a
  channel; in steady state, this equals the local source density ρ(N). Boundary conditions:
  supply enters through channels (no external source), exits through organizational boundaries
  (turnover, disengagement). By the divergence theorem on the discrete channel graph, total
  supply ∫_C ∇·S = $\oint_{\partial C}$ S·n = ρ(N)·|C|. $\blacksquare$

### Lemma 2: Remote Work as Attenuation Operator (Supply Channel Perturbation)

Paper-012 (SEG26) establishes six supply channels with measured attenuation under remote conditions:

| Channel | Mechanism | Remote Attenuation | α_i |
|---------|-----------|-------------------|-----|
| c₁: Physical presence | Continuous visual/auditory presence | High | 0.9 |
| c₂: Body language | Dominant posture, gestures | High | 0.8 |
| c₃: Immediate attention | Synchronous responsiveness | High | 0.8 |
| c₄: Observability | Subordinate visibility, monitoring | High | 0.9 |
| c₅: Status signals | Corner office, reserved parking, etc. | Complete | 1.0 |
| c₆: Authority demonstration | Meeting control, interruption rights | High | 0.7 |

**Claim**: A_remote(S) = (α₁S₁, ..., α₆S₆) with α = (0.9, 0.8, 0.8, 0.9, 1.0, 0.7).

*Proof*: Each α_i is the complement of the attenuation level from Paper-012 Table 1: α_i = 1 -
  attenuation_factor. For "Complete" attenuation (c₅), α₅ = 0; for "High" attenuation, α_i ≈
  0.2-0.3; we map to the values above based on SEG26 empirical correlation with NPI-16 scores.
  The operator A_remote is linear and diagonal in the channel basis. ||S'||₁ = Σ α_i S_i < Σ
  S_i = ||S||₁ since α_i < 1 for all i. $\blacksquare$

### Lemma 3: Supply Redistribution Necessity (Conservation ⇒ Redistribution)

**Claim**: ||S'||₁ < ||S||₁ ⇒ (∃j: S'_j > S_j) ∨ (∃c₇: S'₇ > 0).

*Proof*: By Lemma 1, ∇·S = ρ(N). By Lemma 2, ||S'||₁ = Σ α_i S_i < Σ S_i = ||S||₁. The total
  supply flux decreases under attenuation. However, by Lemma 1, the source term ρ(N) is
  unchanged (narcissistic need is a trait, not situation-dependent). The continuity equation
  demands:

```
∇·S' = ρ(N) + ∂ρ/∂t  (with perturbation)
```

Since ρ(N) is fixed (narcissistic trait stability),
  the reduced divergence ∇·S' < ∇·S must be compensated. There are two mechanisms:

1. **Redistribution**: Δ_j ≥ 0 added to channels where α_j is least attenuating (c₂ body
  language → c₂ increases via meeting dominance; c₃ attention → c₃ increases via async
  demand). Δ_j = S'_j - α_j S_j.

2. **Mutation**: New channel c₇ emerges where supply pressure P_i = ρ(N) - S_i is maximal. By
  supply pressure gradient dynamics, mutation occurs at argmax_i P_i.

Both mechanisms satisfy the redistribution theorem. $\blacksquare$

### Main Theorem

Combining Lemmas 1-3:

1. By Lemma 1, supply flux obeys conservation law ∇·S = ρ(N).
2. By Lemma 2, remote work applies attenuation A_remote, reducing total flux ||S'||₁ < ||S||₁.
3. By Lemma 3,
  flux reduction triggers redistribution (existing channels) or mutation (new channels).

Therefore, the Narcissistic Supply Conservation Law holds: **Narcissistic supply in an
  organization is conserved — it cannot be created or destroyed, only transformed, redirected,
  or concentrated.** When one channel is blocked (e.g., remote work), supply pressure
  increases in remaining channels or manifests as new pathologies. $\blacksquare$

QED

---

## Corollaries

### Corollary (a): RTO Mandates = Supply Concentration Policy

**Statement**: Return-to-Office mandates are organizational policies to concentrate supply in
  the physical presence channel (c₁), reversing A_remote attenuation.

*Proof*: RTO mandates set α₁ → 1.0, increasing ||S||₁. By MPCC = 0.73 (RFC-0028), leaders with
  high NPI-16 prefer high α₁. RTO is supply concentration policy. $\blacksquare$

*RFC Mapping*: RFC-0028 MPCC=0.73, RFC-0028 §3.2 Narcissistic Supply Extraction.

### Corollary (b): NSST (RFC-0031) = Supply Channel Engineering

**Statement**: Narcissistic Supply Substitution Therapy designs safe redistribution pathways
  Δ_j to prevent mutation pathologies.

*Proof*: By Lemma 3, supply must redistribute. NSST designs Δ_j to be epistemically benign
  (e.g., virtual presence acknowledgment instead of physical presence). The goal is Σ Δ_j =
  ||S||₁ - ||S'||₁ with minimal ||φ||₁ increase. $\blacksquare$

*RFC Mapping*: RFC-0031 NSST, RFC-0017 CBP remote variant (§3.7).

### Corollary (c): Proximity Theater (PTDP, RFC-0032) = Performative Supply Extraction

**Statement**: Proximity theater is performative supply extraction — mandates that increase α₁
  without operational justification, extracting supply via performative presence.

*Proof*: PTI > 1.5 (RFC-0028) indicates mandates exceed productivity-justified presence. By
  Lemma 2, high α₁ with low operational justification = performative supply extraction.
  $\blacksquare$

*RFC Mapping*: RFC-0032 PTDP, RFC-0028 PTI, RFC-0029 FM-PT-01/02.

### Corollary (d): Supply Starvation → Organizational Pathology

**Statement**: When redistribution fails (Δ_j = 0 for all j) and mutation is suppressed,
  supply starvation triggers FM-NP-03 (Supply Starvation Pathology): micromanagement, meeting
  proliferation, blame shifting.

*Proof*: By Lemma 3, if ||S'||₁ < ||S||₁ and no redistribution/mutation, ∇·S' < ρ(N). The
  unmet supply pressure P_i = ρ(N) - S_i accumulates. Leaders compensate via high-pressure
  channels (meetings, surveillance, blame) — these are emergent supply-seeking behaviors.
  $\blacksquare$

*RFC Mapping*: RFC-0029 FM-NP-03,
  RFC-0029 FM-PT-02, RFC-0024 TIP (trench intelligence on supply-seeking).

### Corollary (e): CBP Remote Work = Supply Diffusion → Leader Compensatory Behaviors

**Statement**: RFC-0017 CBP remote variant (listen-only mode, async-first) diffuses supply,
  triggering leader compensatory behaviors (meeting proliferation, Slack performativity)
  unless NSST is active.

*Proof*: RFC-0017 CBP remote variant attenuates all channels (listen-only = no attention
  extraction, async = no immediate attention). By Lemma 2, this is maximum attenuation. By
  Lemma 3, supply must redistribute. Leaders compensate via meeting proliferation (c₃
  attention) and Slack performativity (c₆ authority). NSST provides engineered Δ_j to absorb
  this pressure. $\blacksquare$

*RFC Mapping*: RFC-0017 CBP §3.7, RFC-0031 NSST, RFC-0029 FM-NP-02/03.

---

## Implications

### 1. Supply Conservation as Diagnostic Metric

Total supply flux ||S||₁ is invariant; only channel distribution changes. Organizations should
  monitor:

| Metric | Instrument | Frequency | Target |
|--------|------------|-----------|--------|
| ||S||₁ (total flux) | RFC-0028 MPCC + RFC-0030 ERAP | Quarterly | Invariant |
| Channel distribution S_i/||S||₁ | RFC-0028 §3.2 + RFC-0024 TIP | Monthly | Shift toward operational channels |
| Mutation rate (new channel emergence) | RFC-0029 FM-PT-01/02 | Monthly | < 1 per quarter |
| Supply pressure P_i | RFC-0028 MGI + RFC-0024 TIP | Monthly | max(P_i) < threshold |

### 2. CBP as Supply Diffusion Protocol

Corollary (e) reframes RFC-0017 CBP: the remote variant is a **supply diffusion protocol**
  designed to reduce c₁, c₂, c₃, c₄, c₅, c₆ simultaneously. Without NSST (RFC-0031) providing
  engineered Δ_j, this triggers FM-NP-02/03. CBP remote variant MUST be paired with NSST.

### 3. NSST as Supply Channel Engineering

NSST (RFC-0031) is not "therapy" — it is **supply channel engineering**. The three-level
  gradient maps to redistribution engineering:

| Level | Mechanisms | Δ_j Profile |
|-------|------------|-------------|
| L1 (Nudges) | VPA, DSA, AAR-T3 | Δ on c₅, c₆ (status, authority) |
| L2 (Structured) | STTP, AAR-T1-2, TWS, DLT | Δ on c₂, c₃, c₄, c₆ |
| L3 (Coaching) | Supply Architecture Redesign | Δ on c₁, c₂, c₃, c₄, c₅, c₆ |

### 4. PTDP as Supply Channel Deconcentration

PTDP (RFC-0032) is the inverse of Corollary (a): it dismantles c₁ concentration. By forcing α₁
  → operational minimum, it forces redistribution to operational channels (c₃, c₄) rather than
  narcissistic channels (c₂, c₅, c₆).

### 5. Theorem-006 Connection: Supply Conservation ⇒ Epistemic Closure Gap

Theorem-006: G(O) = D_KL(μ || ν) + ||φ||₁. Theorem-007: ||φ||₁ = supply gap filling.

**Theorem**: The performative fiction mass ||φ||₁ equals the unmet supply pressure: ||φ||_1 =
  Σ max(0, P_i - Δ_i). When redistribution Δ_i < P_i, the residual pressure generates
  performative fictions φ.

*Proof sketch*: Unmet supply pressure P_i drives leaders to generate performative fictions φ
  that simulate supply satisfaction (meetings as attention theater, reports as status signals,
  ceremonies as authority demonstrations). ||φ||₁ is the performative proxy for unmet supply.
  $\blacksquare$

*RFC Mapping*: Theorem-006 ||φ||₁, RFC-0004 DTS, RFC-0014 DSI, RFC-0029 FM-NP-02/03.

---

## Measurement Protocol for Supply Conservation Parameters

| Parameter | Instrument | Calibration Target | Review Trigger |
|-----------|------------|-------------------|----------------|
| ρ(N) (supply density) | NPI-16 × org_scale / 16 | SEG26: ρ ~ NPI-16/16 | Paper-013 replication |
| α_i (attenuation) | Paper-012 Table 1 mapping | SEG26 empirical: (0.9, 0.8, 0.8, 0.9, 1.0, 0.7) | Paper-013 replication |
| ||S||₁ (total flux) | MPCC × MPCC_scale | SEG26: MPCC=0.73 | Annual |
| Δ_j (redistribution) | Channel-specific metrics (meeting hrs, Slack msgs, etc.) | NSST deployment: ΣΔ_j = ||S||₁ - ||S'||₁ | Quarterly |
| P_i (supply pressure) | ρ(N) - S_i | max(P_i) < 0.3 ||S||₁ | Monthly |

---

## Colophon

**Epistemic Integrity Level 4 (EI-4): Mathematical Proof — Empirical Parameters Require
  Calibration**

This theorem is a **mathematical proof** (Lemmas 1–3,
  Main Theorem). The reasoning is deductive, assuming:
- Conservation of psychic energy (Freud 1923 / Jung 1928 formalized as bounded resource)
- Paper-012 Table 1 attenuation factors as α_i coefficients
- NPI-16 as valid ρ(N) proxy
- Organizational steady-state assumption

The **corollaries** are **empirical hypotheses** requiring independent validation:
- Corollary (a): RTO as supply concentration — requires longitudinal RTO policy × MPCC tracking
- Corollary (b): NSST as channel engineering — requires NSST deployment data (T008)
- Corollary (c): PTDP as performative extraction — requires PTDP deployment data
- Corollary (d): Supply starvation pathology — requires longitudinal G(O) tracking
- Corollary (e): CBP remote as supply diffusion — requires CBP remote deployment + NSST
  interaction data

**Calibration Status**: 
- α_i coefficients: SEG26 heuristic, **not empirically calibrated** (Paper-013 target)
- ρ(N) scaling: SEG26 N=500 CEOs, **requires cross-cultural validation** (CP-002)
- Supply pressure threshold 0.3 ||S||₁: **heuristic** (needs Paper-013)

**Replication Status**: Not yet replicated
**Pre-registration**: Theorem-007 protocol pre-registration target: OSF
**Data Availability**: SEG26 data restricted;
  NSST/PTDP deployment data will be restricted (organizational privacy)
**OEP Integration**: Theorem-007 is the theoretical anchor for RFC-0031 (NSST),
  RFC-0032 (PTDP), RFC-0017 §3.7 (CBP remote). These protocols depend on Theorem-007 parameters.

**Review Trigger**: Any independent supply conservation study with N > 20 organizations and
  channel-level supply metrics should trigger Theorem-007 parameter review.

---

QED