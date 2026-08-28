---
rfc: "0006"
title: "Strategic Misalignment Detection Protocol (SMDP)"
stream: "Standards Track"
status: "DRAFT"
category: "Informational"
area: "process"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-18"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [1, 2, 3, 4]
keywords: [misalignment, strategy, decision-audit, divergence, enacted-strategy, espoused-strategy]
abstract: |
  This document specifies the Strategic Misalignment Detection Protocol (SMDP),
  a protocol for continuously measuring the divergence between an organization's
  espoused strategy (documented objectives) and its enacted strategy (resource
  allocation decisions). SMDP defines the Strategic Misalignment Index (SMI) as
  Jensen-Shannon divergence between enacted and espoused strategy distributions,
  classifies misalignment into three types (Over, Under, Orthogonal), and mandates
  decision-to-strategy traceability at creation time. Organizations with SMI >
  0.5 experience accelerated epistemic fragmentation (RFC-0003) and knowledge
  gravity distortion (RFC-0005). While framed as a detection protocol, SMDP
  functions analytically as a diagnostic instrument for organizational strategy.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0006 — Strategic Misalignment Detection Protocol (SMDP)

## Abstract

This document specifies the Strategic Misalignment Detection Protocol (SMDP),
a protocol for continuously measuring the divergence between an organization's
espoused strategy (documented objectives) and its enacted strategy (resource
allocation decisions). SMDP defines the Strategic Misalignment Index (SMI) as
Jensen-Shannon divergence between enacted and espoused strategy distributions,
classifies misalignment into three types (Over, Under, Orthogonal), and mandates
decision-to-strategy traceability at creation time. Organizations with SMI >
0.5 experience accelerated epistemic fragmentation (RFC-0003) and knowledge
gravity distortion (RFC-0005). While framed as a detection protocol, SMDP
functions analytically as a diagnostic instrument for organizational strategy.

> **Dual-Layer Notice**: This RFC employs the Strategic Misalignment Detection
> Protocol (SMDP) as a satirical vehicle for presenting peer-reviewed findings
> on organizational strategy-execution gaps (Kaplan & Norton 1996; Mintzberg
> 1978; Simon 1947). While SMDP employs satirical framing, the organizational
> claims are substantiated by the cited literature. Implementers should treat
> SMDP as an analytical lens, not a deployable governance protocol — though
> some organizations have reportedly "implemented" it by requiring strategic
> tags on every budget line and calendar invite.

## 1. Introduction

### 1.1 Motivation

Kaplan and Norton (1996) famously observed that 90% of organizations
fail to execute their strategies. Henry Mintzberg (1978) distinguished
between *intended strategy* (what leaders say they will do), *realized
strategy* (what happens), and *emergent strategy* (patterns in
absence of intention). The gap between intended and realized strategy is
strategic misalignment.

Herbert Simon (1947) established that decision-makers satisfice under bounded
rationality. In organizations, this means resource allocation decisions —
budget, headcount, calendar time, code commits, vendor contracts — are made
locally under constraints, producing an *enacted strategy* that may diverge
wildly from the *espoused strategy* in OKRs, roadmaps, and strategy decks.

The Strategic Misalignment Detection Protocol (SMDP) makes this divergence
measurable and continuous. By treating every resource allocation decision as
a strategic signal, SMDP transforms a vague complaint ("we're not executing our
strategy") into a tractable metric: the Strategic Misalignment Index (SMI).

### 1.2 Scope

This document specifies:

- **Strategy Representation**: Strategy as a directed acyclic graph (DAG) of
  objectives → measurable outcomes → decisions (OKR-agnostic)
- **Decision Definition**: All resource allocations (budget, headcount, calendar,
  code commits, PR approvals, vendor contracts)
- **Strategic Misalignment Index (SMI)**: Jensen-Shannon divergence between
  enacted and espoused strategy distributions
- **Misalignment Typology**: Three types — Over (Type I), Under (Type II),
  Orthogonal (Type III)
- **Decision→Strategy Traceability**: Mandatory tagging at creation time
- **Temporal Dynamics**: Drift rate, snap events, correction latency

### 1.3 Non-Goals

This document does not specify:

- Strategy formulation process (out of scope)
- OKR tooling or serialization (see BCP-XXXX)
- Remediation of misalignment (see RFC-0014, RFC-0016)
- Strategy formulation theater (covered by RFC-0004)

### 1.4 Relationship to Other RFCs

| RFC | Relationship |
|-----|--------------|
| RFC-0001 (HOP) | Executive delusion → strategic blindness; HOP measures vertex, SMDP measures field |
| RFC-0002 (Conway) | Low MFM → structural misalignment → strategic drift |
| RFC-0003 (Fragmentation) | Formal/operational divergence ↔ strategic misalignment; SMI and FI correlated |
| RFC-0004 (DTS) | Decision theater → strategy theater; TQI and SMI correlated |
| RFC-0005 (Gravity) | Gravity wells → strategic capture; KGI and SMI correlated |
| RFC-0017 (CBP) | Weak ties as alignment channels; CBP edges reduce SMI |

## 2. Terminology

| Term | Definition |
|------|------------|
| **Espoused Strategy (S_esp)** | Documented strategy: OKRs, roadmaps, strategy decks, architecture decision records |
| **Enacted Strategy (S_enacted)** | Strategy implicit in resource allocation decisions over a time window |
| **Decision (D)** | Any resource allocation: budget line, headcount requisition, calendar event, code commit, PR approval, vendor contract |
| **Strategic Objective (O)** | Node in strategy DAG representing a measurable organizational goal |
| **Decision→Objective Mapping (D→O)** | Mandatory tag linking each decision to one or more strategic objectives |
| **Strategy Distribution (P_S)** | Probability distribution over objectives induced by decision weights |
| **Strategic Misalignment Index (SMI)** | JS(P_enacted || P_espoused) ∈ [0, 1] |
| **Over-Alignment (Type I)** | SMI driven by excessive concentration on few objectives (rigidity, premature optimization) |
| **Under-Alignment (Type II)** | SMI driven by dispersion across non-strategic objectives (drift, opportunism) |
| **Orthogonal-Alignment (Type III)** | SMI driven by mass on objectives orthogonal to espoused strategy (emergent, invisible) |
| **Drift Velocity (ν)** | d(SMI)/dt: rate of misalignment change |
| **Snap Event** | SMI change > 0.2 in single quarter (reorg, pivot, crisis) |
| **Correction Latency (λ)** | Time from SMI threshold breach to corrective action |

## 3. Protocol Specification

### 3.1 Strategy Representation

**Requirement 1**: The espoused strategy SHALL be represented as a directed
acyclic graph (DAG) G = (V, E) where:

- V = set of strategic objectives {O_1, ..., O_n}
- E ⊆ V × V = dependency edges (O_i → O_j means O_i enables O_j)
- Each O_i has measurable outcome criteria (not merely activity metrics)

**Requirement 2**: The strategy graph SHALL be versioned. Each version
v_k = (V_k, E_k) corresponds to a strategy publication cycle (quarterly,
annual, or event-driven).

**Requirement 3**: The strategy graph SHALL be queryable via API for
automated SMDP computation.

### 3.2 Decision Definition & Classification

**Requirement 4**: A Decision D is any irreversible resource allocation event
from the following categories:

| Category | Examples | Weight Function |
|----------|----------|-----------------|
| **Budget** | Capex/opex line, vendor contract, tool license | Monetary amount (normalized) |
| **Headcount** | Hire, transfer, termination, contractor | FTE months |
| **Calendar** | Meeting, focus time, offsite, interview | Attendee-hours |
| **Code** | Commit, PR merge, release, deploy | Lines changed × criticality |
| **PR Approval** | Review, merge, deploy approval | Reviewer-hours × criticality |
| **Vendor/Contract** | SaaS, consulting, infrastructure | Contract value × duration |

**Requirement 5**: Each decision D MUST carry a mandatory D→O tag set at
creation time: D.tags = {O_i, O_j, ...} ⊆ V. Tagging is mandatory at the
point of artifact creation (Git commit message, Jira ticket, calendar
invite description, budget line memo, PR description).

### 3.3 Enacted Strategy Computation

**Requirement 6**: The enacted strategy distribution P_enacted over objectives
is computed from the decision stream over a sliding window W (default: 90 days):

```
P_enacted(O_i) = Σ_{D∈W, O_i∈D.tags} weight(D) / Σ_{D∈W} weight(D)
```

where weight(D) = normalized resource magnitude of decision D.

**Requirement 7**: The espoused strategy distribution P_espoused is derived
from the current strategy graph version v_current:

```
P_espoused(O_i) = importance(O_i) / Σ_j importance(O_j)
```

where importance(O_i) is derived from OKR weights, roadmap allocation, or
explicit strategy document weights.

### 3.4 Strategic Misalignment Index (SMI)

**Requirement 8**: The Strategic Misalignment Index SMI MUST be computed as
Jensen-Shannon divergence between P_enacted and P_espoused:

```
SMI = JS(P_enacted || P_espoused)
    = ½ KL(P_enacted || M) + ½ KL(P_espoused || M)
    where M = ½ (P_enacted + P_espoused)
```

**Requirement 8.1**: SMI SHALL be reported with 95% confidence intervals via
bootstrap resampling (1000 iterations over decision stream).

**Requirement 9**: SMI interpretation thresholds:

| SMI Range | Classification | Interpretation | Action |
|-----------|----------------|----------------|--------|
| SMI ≤ 0.15 | **Aligned** | Enacted ≈ Espoused | Routine monitoring |
| 0.15 < SMI ≤ 0.30 | **Drifting** | Emerging divergence | Quarterly review; targeted realignment |
| 0.30 < SMI ≤ 0.50 | **Misaligned** | Significant divergence | Mandatory strategy review (RFC-0016) |
| SMI > 0.50 | **Critical** | Enacted ≠ Espoused | Executive intervention; strategy reset |

### 3.5 Misalignment Typology & Directional Diagnostics

**Requirement 10**: SMDP SHALL classify misalignment into three types using
directional KL-divergence diagnostics alongside SMI:

| Type | Name | Diagnostic Signature | Pathology |
|------|------|---------------------|-----------|
| **Type I** | **Over-Alignment** | D_KL(P_espoused || P_enacted) >> D_KL(P_enacted || P_espoused) | Rigidity; premature optimization; HOP + Theater |
| **Type II** | **Under-Alignment** | D_KL(P_enacted || P_espoused) >> D_KL(P_espoused || P_enacted) | Drift; opportunism; Conway + Fragmentation |
| **Type III** | **Orthogonal** | Both KL high; mass on objectives not in espoused strategy | Emergent/invisible strategy; Gravity + Fragmentation |

**Requirement 11**: Each type SHALL be reported with:
- Contribution to total SMI (%)
- Top-5 driving objectives
- Root cause hypothesis (HOP, Conway, Theater, Gravity, Fragmentation)

### 3.6 Temporal Dynamics

**Requirement 12**: SMI SHALL be computed continuously with:
- **Sliding window**: 90-day default (configurable: 30–180 days)
- **Monthly snapshots**: SMI time series for trend analysis
- **Drift velocity**: ν = d(SMI)/dt (quarterly derivative)
- **Snap detection**: ΔSMI > 0.2 in single quarter → snap event logged

**Requirement 13**: Snap events SHALL be classified:
| Snap Type | Trigger | Typical Cause |
|-----------|---------|---------------|
| **Reorg Snap** | SMI spike + org structure change | Reorg, M&A, leadership change |
| **Pivot Snap** | SMI spike + strategy version bump | Explicit strategy change |
| **Crisis Snap** | SMI spike + revenue/incident spike | Outage, security breach, market shock |
| **Silent Snap** | SMI spike without visible cause | Emergent strategy, shadow IT |

**Requirement 14**: Correction latency λ SHALL be tracked:
- λ = time from SMI threshold breach → corrective action recorded
- λ > 90 days → mandatory RFC-0016 review

### 3.7 Decision→Objective Traceability

**Requirement 15**: Every decision artifact MUST carry D→O tags at creation:

| Artifact | Tag Format | Enforcement |
|----------|------------|-------------|
| Git commit | `SMDP: O-123, O-456` in commit message | Pre-commit hook |
| Jira/Linear ticket | `smdp-objectives: [O-123, O-456]` custom field | Required field |
| Calendar invite | `#SMDP O-123 O-456` in description | Calendar policy |
| Budget line | `smdp-objective: O-123` in memo | Finance system |
| PR approval | `SMDP: O-123` in review comment | PR template |
| Vendor contract | `SMDP-Objective: O-123` in clause | Procurement policy |

**Requirement 16**: Tagging MUST occur at creation time. Retroactive tagging
is PROHIBITED (creates alignment theater). Missing tags → decision excluded
from SMI computation (recorded as `UNMAPPED`).

**Requirement 17**: `UNMAPPED` rate SHALL be reported alongside SMI.
`UNMAPPED` > 15% → data quality alert.

### 3.7 Normative Requirements Summary

| Req | Parameter | MUST | SHOULD | MAY |
|-----|-----------|------|--------|-----|
| 1 | Strategy as DAG | YES | | |
| 2 | Versioned strategy graph | YES | | |
| 3 | Queryable strategy API | YES | | |
| 4 | Decision definition | YES | | |
| 5 | D→O tag at creation | YES | | |
| 6 | P_enacted from decisions | YES | | |
| 7 | P_espoused from strategy | YES | | |
| 8 | SMI = JS divergence | YES | | |
| 8.1 | Bootstrap CIs | YES | | |
| 9 | SMI thresholds table | YES | | |
| 10 | 3-type classification | YES | | |
| 11 | Type diagnostics | YES | | |
| 12 | Continuous + drift velocity | YES | | |
| 13 | Snap event logging | YES | | |
| 14 | Correction latency λ | YES | | |
| 15 | D→O tags at creation | YES | | |
| 16 | No retroactive tagging | YES | | |
| 17 | UNMAPPED rate reporting | YES | | |

## 4. Operational Considerations

### 4.1 Deployment Models

SMDP is a diagnostic, not a governance protocol. Organizations MAY apply it as:

1. **Continuous Radar**: Real-time SMI from integrated tooling (Git, Jira, Calendar,
   Finance, HRIS). Dashboard to C-suite.
2. **Quarterly Audit**: SMI + typology + drift velocity reported in strategy review.
3. **Decision Gate**: SMI > 0.5 blocks new strategic initiatives pending review
   (per RFC-0016).
4. **Emergent Strategy Detection**: Type III mass identifies legitimate emergent
   strategy for formalization.

### 4.2 Failure Modes

| Failure Mode | Mechanism | Detection | Mitigation |
|--------------|-----------|-----------|------------|
| **Tagging Theater** | Fake tags to lower SMI | UNMAPPED rate low but outcomes don't improve | Cross-validate with outcomes; RFC-0003 FI cross-check |
| **Strategy Inflation** | Espoused strategy expands to cover enacted | SMI artificially low | Fix strategy version at quarter start |
| **Objective Gaming** | Teams create objectives matching work | P_espoused mimics P_enacted | Independent strategy audit |
| **UNMAPPED Exclusion** | High-impact decisions untagged → excluded | UNMAPPED rate > 15% alert | Mandatory tagging enforcement |

### 4.3 Monitoring and Alerting

**Requirement 18**: Organizations computing SMDP SHALL alert when:
- Any unit SMI crosses threshold (0.15, 0.30, 0.50) upward
- Drift velocity ν > 0.1/quarter sustained for 2 quarters
- Type III mass > 20% of enacted mass (emergent strategy)
- Snap event detected (ΔSMI > 0.2 in quarter)
- Correction latency λ > 90 days for any threshold breach
- UNMAPPED rate > 15%

## 5. Security & Privacy Considerations

### 5.1 Strategic Intelligence

SMI and typology reveal:
- Which units are strategically captured (political vulnerability)
- Which objectives are neglected (competitive blind spots)
- Emergent strategy before formalization (first-mover insight)

**Requirement 19**: SMI data SHALL be classified at same level as org strategy
documents. Access limited to: measured units, C-suite, independent auditor.

### 5.2 Individual Privacy

Decision stream analysis uses digital traces (Git, Calendar, Slack, HRIS).

**Requirement 20**: Aggregation to team level (minimum 5 individuals) before
SMI computation. Individual-level graphs PROHIBITED for SMI reporting.

**Requirement 21**: D→O tags from calendar/code MUST be anonymized in
cross-team aggregation. Minimum group size: 5.

### 5.3 CBP Integrity (RFC-0017 §7)

SMDP uses decision stream that includes CBP-synchronized knowledge. If SMDP
monitoring incentivizes performative coffee breaks for "alignment signals,"
CBP's epistemic integrity is compromised.

**Requirement 22**: CBP-derived decisions used in SMDP MUST be anonymized and
aggregated. No executive attendance tracking for SMDP purposes.

## 6. OSC Considerations

### 6.1 Registry Updates

This RFC requests:
- RFC-0006 allocated in Standards Track, process area (0100–0199)
- Keywords: misalignment, strategy, decision-audit, divergence, enacted-strategy
- See-also: RFC-0001, RFC-0002, RFC-0003, RFC-0004

### 6.2 Code Points

SMDP defines no code points. SMI thresholds and typology are informational.

## 7. References

### 7.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001,
Organizational Standards Consortium, 1987. https://rfc.osc.org/rfc0001

[RFC-0002] Matos, R. "Conway's Law Generalization Protocol." RFC 0002,
Organizational Standards Consortium, 1987. https://rfc.osc.org/rfc0002

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003,
Organizational Standards Consortium, 1992. https://rfc.osc.org/rfc0003

[RFC-0004] Matos, R. "Decision Theater Specification." RFC 0004,
Organizational Standards Consortium, 1998. https://rfc.osc.org/rfc0004

[RFC-0005] Matos, R. "Knowledge Gravity Measurement Framework." RFC 0005,
Organizational Standards Consortium, 1995. https://rfc.osc.org/rfc0005

[RFC-0016] Matos, R. "Institutional Memory Backup Specification." RFC 0016,
Organizational Standards Consortium, 2026. https://rfc.osc.org/rfc0016

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017,
Organizational Standards Consortium, 2001. https://rfc.osc.org/rfc0017

### 7.2 Informative References

Kaplan, Robert S., and David P. Norton. 1996. *The Balanced Scorecard:
Translating Strategy into Action*. Boston: Harvard Business School Press.

Mintzberg, Henry. 1978. "Patterns in Strategy Formation." *Management Science*
24 (9): 934–948. https://doi.org/10.1287/mnsc.24.9.934

Mintzberg, Henry, and James A. Waters. 1985. "Of Strategies, Deliberate and
Emergent." *Strategic Management Journal* 6 (3): 257–272.

Simon, Herbert A. 1947. *Administrative Behavior: A Study of Decision-Making
Processes in Administrative Organization*. New York: Macmillan.

Cover, Thomas M., and Joy A. Thomas. 2006. *Elements of Information Theory*.
2nd ed. Hoboken: Wiley.

Endres, Dominik M., and Johannes E. Schindelin. 2003. "A New Metric for
Probability Distributions." *IEEE Transactions on Information Theory* 49 (7):
1858–1860.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-18 | Rodolfo Matos | Initial draft per HOSTILE_ANALYSIS_RFC0006.md |
| 1.0 | 2026-07-18 | Rodolfo Matos | OEP canon alignment; 3-type typology; JS divergence; mandatory tagging |

## Appendix B: Open Issues

1. **Decision Granularity**: What is the minimal decision unit? A single commit?
   A PR? A sprint? Impact on SMI sensitivity. [UNVERIFIED]

2. **Strategy Graph Extraction**: Automated extraction from OKR tools vs manual
   curation. Impact on P_espoused fidelity. [UNVERIFIED]

3. **Cross-Organizational SMI**: Comparing SMI across companies requires
   normalized strategy graphs. Schema standardization needed. [UNVERIFIED]

4. **Emergent Strategy Formalization**: When Type III mass exceeds threshold,
   what is the formalization process? Bridge to RFC-0014/RFC-0001. [UNVERIFIED]

5. **SMI vs Financial/Operational Metrics**: Correlation between SMI and
   lagging indicators (revenue, retention, incident rate). Longitudinal study needed.
   [UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Kaplan, Norton, Mintzberg, Simon, Cover,
> Thomas, etc.) are accurate. The coffee machine, however, is real — and it
> is currently synchronizing more knowledge than this repository ever will.