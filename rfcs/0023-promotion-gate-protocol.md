---
rfc: "0023"
title: "Promotion Gate Protocol (PGP)"
stream: "Humor"
status: "DRAFT"
category: "Informational"
area: "process"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-19"
updated: "2026-07-19"
obsoletes: []
obsoleted_by: []
see_also: [4, 11, 14, 17]
keywords:
  - promotion-gate
  - ceremony
  - decision-formalization
  - governance
  - zombie-projects
  - cancellation
abstract: |
  Organizations routinely discover that strategic decisions
  exist only as ambient knowledge among senior staff, never
  receiving institutional form. This RFC proposes a Promotion
  Gate Protocol (PGP) for transforming tacit accumulated
  intent into binding organizational artifacts. The protocol
  formalizes what audits repeatedly find: decisions happen
  by neglect, projects survive by inertia, and the true
  architecture lives in hallway conversations. PGP introduces
  seven metrics and a ceremony framework for surfacing the
  gap between what an organization believes it decided and
  what it has recorded.
dual_layer: true
satire_notice: "satire"
---

# RFC-0023: Promotion Gate Protocol (PGP)

| RFC   | 0023                          |
|-------|-------------------------------|
| Title | Promotion Gate Protocol (PGP) |
| Stream| Humor                         |
| Status| DRAFT                         |
| Area  | Process                       |

## Status of This Memo

Distribution is unlimited. Implementation requires three
steering committee meetings and one uncomfortable silence.

## Abstract

The finding is never about missing dashboards. It is about
decisions that nobody decided. Projects continue because no
one holds the authority to stop them. PGP formalizes the gap
between organizational intent and record.

## 1. Introduction

Repeated audit cycles reveal the same pattern: teams reference
decisions in no formal record; architecture guidelines live
in slides, not code; five people carry institutional memory
while the organization pretends it has documentation.

RFC-0004 [RFC4] introduced Decision Theater, where decisions
are performed but never recorded. RFC-0011 [RFC11] documented
Meeting Entropy -- meetings that accelerate degradation.
RFC-0014 [RFC14] analyzed Consensus Theater, simulating
agreement while no one commits. This RFC completes the set
by addressing the drift of unrecorded decisions into
organizational mythology.

## 2. Terminology

| Term | Definition |
|------|-----------|
| Promotion Gate | Minimum ceremony to elevate intent to decision |
| Tacit Accumulation | Direction solidifying without authorizing act |
| Decision Ledger | Record of decisions, rationale, constraints |
| Zombie Project | Survives through absence of cancellation |
| Architecture Normativity | Ratio of intent to enforcement |
| Capacity Ceiling | Max commitments a team can sustain |
| Institutional Memory | Knowledge in unaided recall |
| Coffee Channel | Informal pathways [RFC17] |

## 3. The Promotion Gate Ceremony

A Promotion Gate Ceremony (PGC) is the minimum ritual by
which intent becomes a binding decision. Without PGC, intent
remains in ambient knowledge subject to reinterpretation.

**Requirements:** (1) Named Author, (2) Written Rationale,
(3) Constraint Set, (4) Witness Count of Two, (5) Date
Stamp.

**Failure modes:**

| Failure Mode | Prevalence |
|-------------|-----------|
| Ceremony Skipping -- whiteboard to assumed reality | 89% |
| Witness Inflation -- false provenance via added names | 34% |
| Rationale Ghosting -- decision recorded, rationale omitted | 67% |
| Constraint Amnesia -- no expiry, indefinite persistence | 73% |

## 4. Decision Ledger Minimum

```
DLM = (C x A x D) / F
```

- C = decisions made this quarter
- A = decisions with written rationale
- D = decisions with expiry conditions
- F = decisions with a named author

| DLM Range | Status |
|-----------|--------|
| 0.0 - 0.2 | Critical: decisions exist as folklore |
| 0.2 - 0.5 | Degraded: majority untraceable |
| 0.5 - 0.8 | Functional: most have provenance |
| 0.8 - 1.0 | Healthy: authors, rationale, constraints present |
| > 1.0 | Bureaucratic: recording costs exceed making |

Post-audit transformation units typically measure 0.15 - 0.35.

## 5. Cancellation as First-Class Operation

The ability to cancel must be architecturally equivalent to
the ability to create. A system requiring seven approvals to
start and zero to stop manufactures Zombie Projects by design.

**Requirements:** (1) Reason referencing the Decision Ledger
entry, (2) Stakeholder notification within one business week,
(3) Artifact archival, (4) Capacity release back to the pool.

**Resistance:** Sunk Cost Invocation, Attribution Asymmetry
(cancelers bear visible blame), Ceremony Deficit (no PGC
for stopping).

## 6. Zombie Project Detection
```
ZPD = (T x N) / (A + S)
```
- T = months since last decision or review
- N = people who can explain the project purpose
- A = active artifacts (code, docs, tickets)
- S = monthly spend in arbitrary budget units

```
ZPD > 3.0    -->  Zombie
ZPD 1.0-3.0  -->  Undead (requires assessment)
ZPD < 1.0    -->  Alive
```

**Flaw:** N=0 yields ZPD=0 ("Alive"). A project no one
understands is maximally Zombie. Apply floor of 0.5 for N
when no current member was present at inception.

## 7. Architecture Normativity Index
```
ANI = E / D
```
- E = rules with automated enforcement
- D = rules in documentation

| ANI Range | Meaning |
|-----------|---------|
| 0.0 - 0.2 | Decorative: aspirational fiction |
| 0.2 - 0.5 | Suggestion: mentioned, then forgotten |
| 0.5 - 0.8 | Enforced: majority have checks |
| 0.8 - 1.0 | Strict: mostly machine-enforced |
| > 1.0 | Over-Enforced: blocks faster than comprehension |

"Guidelines for that" without CI checks is Decorative
Architecture, the signature ANI deficit pattern.

## 8. Capacity Ceiling Theorem
For n humans, maximum concurrent commitments:
```
Cmax = n x 3.5
```

Exceeding Cmax degrades all commitments. A team of 12
tracking 60 initiatives at 143% Cmax: nothing completes.

## 9. Institutional Memory Fragility Score
```
IMFS = P / (D x R)
```
- P = % of knowledge held by fewer than 3 people
- D = documentation coverage %
- R = current team / original team size

| IMFS Range | Risk |
|------------|------|
| 0.0 - 0.5 | Low: well distributed and documented |
| 0.5 - 2.0 | Moderate: known key-person dependency |
| 2.0 - 5.0 | High: concentrated, poorly documented |
| > 5.0 | Critical: single departure = irrecoverable loss |

## 10. Integration with Existing Protocols

- **RFC-0004:** PGC transitions theater to record, with
  latency penalty.
- **RFC-0011:** PGC capped at 5 people, 45 minutes.
- **RFC-0014:** PGC requires independent witness
  confirmation, not attendance.
- **RFC-0017:** PGP captures Coffee Channel outputs; PGC
  formalizes them.

## 11. Failure Modes

| Failure Mode | Severity |
|-------------|----------|
| Ceremony as Bureaucracy -- checkbox, no content | High |
| Ledger Inflation -- minor decisions inflate DLM | Medium |
| Zombie Resurrection -- canceled projects reappear | Low |
| Metric Gaming -- targets over health | High |
| Ceiling Denial -- leadership rejects Cmax | Medium |

## 12. Security Considerations

The Decision Ledger may contain sensitive data. Read access
organization-wide; write access to PGC participants. Zombie
Projects occupy capacity, reducing incident response.

## 13. Performance Evaluation

**Composite score:**
```
PGP Score = (DLM + ANI + (1/ZPD_avg)) / 3
```
**Expected outcomes:** 40-60% Zombie reduction in two
quarters; DLM from 0.25 to above 0.60 in one fiscal year;
decreasing IMFS as documentation improves.

**Limitation:** PGP surfaces the gap; it does not close it.

## 14. Extensions

| Extension | Description |
|-----------|-------------|
| PGP-CLI | CLI for computing all seven metrics |
| PGP-Dashboard | Real-time DLM, ANI, ZPD visualization |
| PGP-Audit | Automated Ceremony Skipping detection |
| PGP-Alert | Capacity Ceiling proximity notifications |
| PGP-Compat | Adapter for project management tools |
| PGP-Lite | Simplified protocol for teams under 50 |

## 15. References

| Ref | Document |
|-----|----------|
| [RFC4] | RFC-0004: Decision Theater |
| [RFC11] | RFC-0011: Meeting Entropy |
| [RFC14] | RFC-0014: Consensus Theater |
| [RFC17] | RFC-0017: Coffee Channel Protocol |

## 16. Authors' Address

Rodolfo Matos, OSC, rm@osc.org

## 17. Colophon

Composed between audit findings and committee responses.
Dedicated to everyone who has whispered "does anyone know why
we are doing this?" in a room that was not recording.
Metrics were observed, named, and given formulas so they
could be measured, argued about, and ignored with precision.

---

*End of RFC-0023*
