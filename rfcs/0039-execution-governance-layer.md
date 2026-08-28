---
rfc: "0039"
title: "Execution Governance Layer (EGL) — The Quarterly Re-Decision Protocol"
stream: "Humor"
status: "DRAFT"
category: "Informational"
area: "process"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
created: "2026-08-14"
updated: "2026-08-14"
obsoletes: []
obsoleted_by: []
see_also: [23, 4, 7, 16]
keywords:
  - execution-governance
  - portfolio-review
  - quarterly-cadence
  - formal-states
  - cancellation
  - decision-ledger
  - zombie-projects
abstract: |
  Organizations formalize the entrance to their portfolio and
  forget the exit. Projects are admitted with ceremony — scored,
  ranked, voted, capacity-checked — and then abandoned to a year of
  silence until the annual report reconstructs, a posteriori, what
  happened. This RFC specifies the Execution Governance Layer (EGL):
  a minimal quarterly cadence that re-decides the portfolio during
  execution, with formal states, legitimate cancellation, and a
  four-field decision ledger. The EGL is the missing half of the
  Promotion Gate Protocol (RFC-0023): where PGP governs entry, EGL
  governs the corridor.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0039 — Execution Governance Layer (EGL)

| RFC   | 0039                          |
|-------|-------------------------------|
| Title | Execution Governance Layer (EGL) |
| Stream| Humor                         |
| Status| DRAFT                         |
| Area  | Process                       |

## Status of This Memo

Distribution is unlimited. Implementation requires four short
meetings a year and the courage to say the word "cancel" out loud.

## Abstract

Every organization has a front door. Few have a corridor. Projects
are admitted with extraordinary ceremony — scored on 30/30/40
weightings, placed in A-D quadrants, voted on by constituents,
fitted to an ETI capacity ceiling — and then the organization looks
away for twelve months. The annual report arrives, a twelve-month
autopsy, and the projects that stalled in January are only named in
December. The EGL is the corridor: a quarterly moment where the
portfolio is re-decided, states are assigned, cancellations are made
legal, and the ledger records one line per decision.

## 1. Introduction

### 1.1 The Front Door Is a Lie

The audit pattern is always the same. An organization shows you its
entrance: prioritization methodology, scoring matrices, voting by
constituent entities, backlog discipline, capacity in full-time
equivalents. You are impressed. Then you ask what happens in
February, and the answer is a silence. The entrance is a ceremony;
the corridor is a rumor.

The canonical finding (RFC-0023) named the front-door problem:
decisions that nobody decides, projects that survive by inertia.
RFC-0023 gave us the Promotion Gate, the Decision Ledger, the
Zombie Project Detection metric. It fixed the door.

It did not fix the corridor. Between the Promotion Gate (entrance)
and the annual report (retrospective), there is a year with no
decision point. This RFC specifies the missing layer.

### 1.2 The Author's Relationship to the Source

The EGL is drawn from an analysis of a real institution — the
digital services unit of the University of Porto (UPdigital),
which the author of this RFC also analyzed in the thesis "Governação
Cognitiva em Sistemas Sociotécnicos" and in the OEP canon
(RFC-0038 §1.2). The three institutional documents — Plano de
Atividades 2025, Plano de Atividades 2026, Relatório de Atividades
2024 — show exactly the asymmetry this RFC formalizes: a rigorous
entrance (30/30/40 valoração, quadrantes A-D, EC voting, ETI
capacity) and a tacit execution (zero "Estado" fields, zero "cancel"
occurrences, narrative outcomes like "não foi concluído, terá
continuidade em 2025").

Consistent with the canon's citation rule, only published sources
are citable. The analysis documents are published in this
repository (`docs/analyses/updigital-institucionais-x-oep.md`,
`docs/analyses/updigital-governanca-minima-oep.md`) and are
referenced there.

### 1.3 Scope

This RFC is **Informational**. It specifies the EGL as a protocol:
the cadence, the states, the cancellation, the ledger. It does not
claim the UPdigital adopted it, and it does not prescribe a
rollout. Any reading that treats the EGL as "the new process the
unit now follows" is a misreading; the protocol is a proposal
waiting for adoption (Section 9 of the underlying design document
is explicit on this).

## 2. Terminology

| Term | Definition |
|------|-----------|
| **EGL** | Execution Governance Layer: the quarterly portfolio re-decision cadence and its instruments |
| **Cadence** | A recurring, time-boxed decision moment (four per year) |
| **Front Door** | The entrance process: prioritization, voting, capacity fitting (governed by RFC-0023 PGP) |
| **Corridor** | The execution period between entrance and annual report |
| **Formal State** | An explicit, recorded classification of a project (Exploratório → Cancelado) |
| **Zombie Project** | A project surviving through the absence of cancellation (RFC-0023 §6) |
| **DLM** | Decision Ledger Minimum — proportion of decisions with rationale, author, expiry (RFC-0023 §4) |

## 3. The Corridor Problem

### 3.1 The Anatomy of Silence

A portfolio of 111 projects (the PA2026 number) is admitted in
November. Between November and the next November, no formal
decision happens. The annual report arrives and reconstructs the
year: "Desenvolvimento foi iniciado, mas não foi concluído. Terá
continuidade em 2025." Four projects stalled the entire year for
lack of staff and external dependencies; the report names them in
December, after the year is gone.

The silence is not neutral. Silence is a decision — the decision
to keep going. It is the most common decision in organizations,
and the only one taken without ceremony.

### 3.2 Why the Front Door Cannot Fix It

The entrance process can rank projects, but it cannot re-decide
them. A project that loses its external dependency in March, or
whose staff are reassigned in June, was correctly admitted and is
now wrongly continued. The entrance is a single-moment decision;
execution is a process that changes the premises. Without a
re-decision point, the premises age silently.

## 4. The Cadence: Re-Deciding Four Times a Year

### 4.1 The Minimum Viable Decision Moment

The EGL specifies a **quarterly portfolio review** — four
moments per year, each time-boxed, each with a defined output.

**Requirements (adapted from RFC-0023 §10):**

1. **Duration:** 45 minutes maximum. Longer meetings do not decide
   more; they merely distribute the same decision over more
   attendance (RFC-0011).
2. **Attendance:** five people maximum. The decision actors are the
   same as the entrance: the constituent entities (EC) and the
   project owner. No new actors, no new power.
3. **Scope: sampling, not exhaustive review.** Reviewing 111
   projects per quarter is not discipline; it is bureaucracy
   (DLM > 1.0, RFC-0023 §4). The cadence reviews the top-N by
   priority (the entrance already ordered them) plus flagged
   projects — delayed, undecided for over one quarter, over
   budget.
4. **Output: a decision per reviewed project.** Each review
   produces a state transition and one ledger line. Projects not
   reviewed remain "Em auditoria" without a new decision.

### 4.2 Why Sampling Is the Mechanism, Not a Shortcut

A layer that reviews everything is a layer that reviews nothing —
it collapses under its own weight by Q2. The EGL is deliberately
built on the asymmetry: the entrance ceremony already decided who
matters (priority ordering). The cadence re-decides only where the
premises may have changed. Sampling is the anti-theater guard
(RFC-0004): it keeps the ceremony small enough to be real.

## 5. Formal States: Where the Decision Lives

### 5.1 The Seven States

A decision without a place to live is a conversation. The EGL
specifies formal states, drawn from the governance model (thesis
§4.4) and adapted to a portfolio:

| State | Meaning | Seen in the wild (RA2024) |
|-------|---------|---------------------------|
| **Exploratório** | Idea in validation, no capacity commitment | The 14 ad-hoc proposals (+21% to plan) |
| **Em análise** | Being evaluated for acceptance | Entrance seriation/voting |
| **Em auditoria** | In execution, subject to cadence review | "em curso" (7), "em execução" (1) |
| **Decidido** | Accepted as basis for action (gate passed) | *Absent today* |
| **Promovido** | Completed and integrated as institutional basis | "foi concluído" |
| **Suspenso** | Interrupted temporarily, not discarded | "terá continuidade em 2025" |
| **Cancelado** | Informed decision to not proceed | *Absent today — zero occurrences* |

### 5.2 Transition Rules

Three rules govern all transitions (thesis §4.4):

1. No transition without a named responsible agent;
2. Final states (Promovido, Cancelado) require minimal
   justification;
3. Regressive transitions are permitted upon explicit
   re-evaluation.

### 5.3 The Anchor

The state is not a new system. The portfolio already has a project
ficha (code-title, start, end, team, milestones, risks — the
PA2026 format). The EGL adds one field: **Estado**. Everything
else stays. The narrative outcome "Desenvolvimento foi iniciado,
mas não foi concluído. Terá continuidade em 2025" becomes:

```
Estado: Suspenso (from 2024-Q4 cadence)
Transition: Em auditoria → Suspenso, by [owner]
Justification: external dependency (INESC TEC); re-evaluate Q1 2025
```

The data was always there. The state makes it queryable.

## 6. Cancellation as a Legal State

### 6.1 The Word That Nobody Says

"Cancel" does not appear once in the 2025 and 2026 plans. The
annual report reprograms stalled projects — it never cancels. The
institution has created everything needed to start and nothing
needed to stop. This is the RFC-0023 §5 finding, verbatim: "a
system requiring seven approvals to start and zero to stop
manufactures Zombie Projects by design."

### 6.2 Requirements

The EGL makes cancellation a first-class operation (RFC-0023 §5):

1. **Reason referencing the ledger** — the justification links to
   the prior decision entry;
2. **Stakeholder notification** within one business week;
3. **Artifact archival** — documentation, code, decisions;
   essential for institutional memory (RFC-0007, RFC-0016);
4. **Capacity release** back to the ETI pool (RFC-0023 §8).

### 6.3 The Anti-Inertia Trigger

The cancellation culture problem is attribution asymmetry
(RFC-0023 §5): the canceler carries visible blame, the survivor
carries none. The EGL counters with a number: the cadence flags
any project without a decision or review for over one quarter,
using the ZPD metric (RFC-0023 §6). A ZPD above 3.0 is a formal
candidate for evaluation — Suspenso or Cancelado. The metric turns
"an opinion against inertia" into "a recorded datum," which is
defensible.

### 6.4 The Real-World Reading

The four projects named in the annual report's "projects without
start or execution" table are the perfect test case. Stalled for
staff shortage and external dependencies, they were reprogrammed
to the next plan — a decision taken in December for a problem that
existed in January. Under the EGL, the Q1 cadence would have
suspended them, with the reason recorded, and the "reprogrammed"
note in the report would become the formal transition
"Suspenso → Em análise → Decidido." For the cases where
reprogramming makes no sense — which today have no name — the
Cancelado state exists as a legitimate option.

## 7. The Decision Ledger: One Line per Decision

### 7.1 The Four-Field Minimum

The EGL's ledger is the thesis §5.5 "ledger de preservação
funcional": not an exhaustive record, a succinct set of entries
documenting critical decisions. Each entry carries four fields:

```
[Decision: state transition] · [Date: cadence Q3] · [Resulting state: Suspenso]
[Brief rationale: external dependency, re-evaluate Q1] · [Owner: [agent]]
```

### 7.2 The Health Metric

The ledger's health is the DLM (RFC-0023 §4): the proportion of
decisions with written rationale, expiry conditions, and a named
author. The target is pragmatic: **above 0.5** (functional — most
decisions traceable), **never above 1.0** (bureaucratic —
recording costs exceed making).

### 7.3 The Anchor

The portfolio already has 51 project fichas with milestones and a
final report. The ledger is not a new system: it is one line per
state transition, written at the cadence, appended to the existing
ficha. At year end, the annual report collects the entries and
publishes the summary — the narrative outcomes remain, now
accompanied by the record of decisions that produced them.

## 8. The Complete Cycle

```
PA (Nov/Year N) → Q1 → Q2 → Q3 → Q4 → RA (Year N)
  front door       quarterly re-decision        retrospective
  (PGP, exists)    + state + ledger             (exists + ledger summary)
```

The EGL does not create new decisions the entrance did not
anticipate; it makes them explicit and dated during execution. The
annual report remains the institutional document; the cadence
feeds it.

## 9. What the EGL Refuses to Be

1. **Not a front-door replacement.** The entrance ceremony stays;
   it is not the problem.
2. **Not a new tool.** No software, no platform — a protocol over
   documents that already exist.
3. **Not a strategy change.** Objectives (OE1-OE6) and the parent
   strategic plan are untouched.
4. **Not the full model.** The EGL is the minimum: states,
   cancellation, ledger, strategic KPIs. Nothing else.
5. **Not a done deed.** The EGL is a proposal awaiting adoption.
   A design that never gets adopted is Decision Theater (RFC-0004):
   a performed decision, never recorded. This RFC does not
   present itself as a consummated change.

## 10. Strategic Indicators (Optional Companion)

The EGL pairs with one strategic measurement per objective (the
portfolio's own OE1-OE6), each with a named data source in
existing documents — no invented metrics, no metric gaming
(RFC-0023 §11):

| Objective | Indicator | Data source |
|-----------|-----------|-------------|
| OE1 — Digital transformation | % of projects meeting execution gates on time | Cadence + ficha milestones |
| OE2 — Cyber-resilience | % of services with validated continuity | SGSI/NIS2 + test reports |
| OE3 — Innovation via iLab | # of iLab pilots promoted per year | iLab + state transitions |
| OE4 — Infrastructures | % of infrastructure projects with validated community impact | IT.* projects + satisfaction |
| OE5 — People | ETI retention; training hours per ETI per year | RA §2 + support/capacity unit |
| OE6 — User-centered services | Satisfaction with speed (measured: 4.71) + % of EC-co-designed services | QoS tables + EC projects |

Objectives without a data source are excluded, not invented. OE5
(people) uses process indicators — retention, training — because
"motivation" has no honest number.

## 11. Failure Modes

| Failure Mode | Severity | Mechanism |
|--------------|----------|-----------|
| Ceremony as Bureaucracy — checkbox, no decision | High | The cadence runs, the states never change |
| Sampling Drift — the top-N grows to everything | High | The layer collapses under its own weight |
| Cancellation Taboo Persists — state exists, behavior doesn't | Medium | Attribution asymmetry unchanged; ZPD underused |
| Metric Gaming — indicators optimized against themselves | Medium | Retention improved by retaining the wrong people |
| Ledger Inflation — every decision recorded | Medium | DLM approaches 1.0, bureaucracy returns |

## 12. Security Considerations

The ledger contains decision rationale, which may include
sensitive staffing and dependency information. Read access
organization-wide; write access to cadence participants. Cancelled
projects release capacity, which is itself a security property:
zombie projects occupy staff that incident response does not have.

## 13. Performance Evaluation

The EGL's success is measured by its absence of ceremony:

- DLM above 0.5 within two quarters (decisions traceable);
- Zero projects undecided for over one quarter (ZPD flagged at
  every cadence);
- Four 45-minute meetings per year, none attended by more than
  five people;
- Cancellation occurring at least once per year — the state that
  proves the culture changed.

**Limitation:** the EGL surfaces the corridor; it does not walk
it. It provides the decision point; it cannot provide the courage.
That is a cultural property no protocol can specify.

## 14. Extensions

| Extension | Description |
|-----------|-------------|
| EGL-Lite | Quarterly review by exception only, for teams under 50 |
| EGL-Dashboard | ZPD + DLM visualization per cadence |
| EGL-Audit | Automated detection of cadence-skipping |
| EGL-Compat | Adapter for project management tools |
| EGL-Annual | Automation of the ledger summary into the annual report |

## 15. References

| Ref | Document |
|-----|----------|
| [RFC23] | RFC-0023: Promotion Gate Protocol |
| [RFC4]  | RFC-0004: Decision Theater Specification |
| [RFC7]  | RFC-0007: Organizational Amnesia Prevention Protocol |
| [RFC16] | RFC-0016: Institutional Memory Backup Specification |
| [RFC38] | RFC-0038: Living Innovation Lab (iLab) |
| [T115]  | docs/analyses/updigital-institucionais-x-oep.md |
| [T116]  | docs/analyses/updigital-governanca-minima-oep.md |

## 16. Authors' Address

Rodolfo Matos, OSC, rm@osc.org

## 17. Colophon

Composed between an entrance ceremony and an annual report.
Dedicated to every project that was correctly admitted and then
quietly continued until it was too late to say no. The corridor is
not a scandal; it is an omission. The EGL makes the omission
visible four times a year — which is how omissions become honest.

---

*End of RFC-0039*
