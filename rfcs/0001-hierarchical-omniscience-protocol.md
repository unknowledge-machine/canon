---
rfc: 0001
title: "Hierarchical Omniscience Protocol (HOP)"
stream: "Standards Track"
status: "DRAFT"
category: "Informational"
area: "architecture"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "1987-11-02"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [17]
keywords: [hierarchy, executive-delusion, epistemic-capture, bounded-rationality]
abstract: |
  This document specifies the Hierarchical Omniscience Protocol (HOP), a
  protocol modeling the systematic epistemic capture of executive vertices
  in hierarchical organizational graphs. HOP formalizes the mechanism by which
  authority positions generate unwarranted confidence in operational knowledge,
  creating feedback loops that degrade decision quality. While framed as a
  protocol specification, HOP functions analytically as a measurement instrument
  for executive delusion. Implementations SHOULD treat HOP as a diagnostic lens,
  not a deployable management protocol.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0001 — Hierarchical Omniscience Protocol (HOP)

## Abstract

This document specifies the Hierarchical Omniscience Protocol (HOP), a
protocol modeling the systematic epistemic capture of executive vertices in
hierarchical organizational graphs. HOP formalizes the mechanism by which
authority positions generate unwarranted confidence in operational knowledge,
creating feedback loops that degrade decision quality. Experimental evidence
suggests that organizations exhibiting high HOP compliance experience
accelerated epistemic fragmentation (RFC-0003) and increased decision
theater (RFC-0004). While framed as a protocol specification, HOP functions
analytically as a measurement instrument for executive delusion. Implementers
SHOULD treat HOP as a diagnostic lens, not a deployable management protocol.

> **Dual-Layer Notice**: This RFC employs the Hierarchical Omniscience Protocol
> (HOP) as a satirical vehicle for presenting peer-reviewed findings on
> executive epistemic capture. While HOP employs satirical framing, the
> organizational claims are substantiated by the cited literature (Simon 1947;
> Akerlof 1970; Edmondson 2018; Conway 1968). Implementers should treat HOP
> as an analytical lens, not a deployable protocol — though some organizations
> have reportedly "implemented" it by requiring executives to attend coffee
> breaks (RFC-0017).

## 1. Introduction

### 1.1 Motivation

Organizational hierarchies assume that authority correlates with knowledge
scope. This assumption is empirically false. Herbert Simon (1947) established
that decision-makers operate under bounded rationality — they satisfice rather
than optimize. George Akerlof (1970) demonstrated that information asymmetry
between principals and agents creates adverse selection and moral hazard.
Amy Edmondson (2018) showed that without psychological safety, subordinates
filter information upward, creating a systematically distorted view at the top.

The Hierarchical Omniscience Protocol (HOP) makes this pathology explicit.
By formalizing executive epistemic capture as a protocol, HOP renders the
invisible visible: it specifies the states, transitions, and failure modes
of the delusion that authority confers knowledge.

### 1.2 Scope

This document specifies:
- The HOP state machine (Section 3)
- Four core protocol parameters with normative requirements
- The Epistemic Capture Index (ECI) as a quantitative measure
- Operational considerations and failure modes
- Relationship to Coffee-Break Protocol (RFC-0017) and Conway's Law (RFC-0002)

### 1.3 Non-Goals

This document does not specify:
- Mitigation protocols (see RFC-0007 Organizational Amnesia Prevention,
  RFC-0016 Institutional Memory Backup)
- Conway's Law generalization (see RFC-0002)
- Epistemic fragmentation measurement (see RFC-0003)
- Decision Theater formalization (see RFC-0004)

### 1.4 Relationship to Other RFCs

| RFC | Relationship |
|-----|--------------|
| RFC-0002 | Conway's Law Generalization — structural mirror of HOP |
| RFC-0003 | Epistemic Fragmentation Monitoring — consequence of HOP |
| RFC-0004 | Decision Theater Specification — downstream effect of HOP |
| RFC-0017 | Coffee-Break Protocol — counter-protocol to HOP |
| Theorem-001 | Coffee Machine Theorem — proves informal bandwidth > formal |

## 2. Terminology

The following terms are defined for use in this document. Terms marked with
† are drawn from the OEP Canon Glossary (TERMINOLOGY.md).

| Term | Definition |
|------|------------|
| **Executive Vertex**† | Management node in formal hierarchy graph with directive authority over operational vertices |
| **Epistemic Capture**† | State where executive vertex believes it possesses operational knowledge it does not |
| **Omniscience Radius**† | Graph distance (in hops) from executive vertex to operational reality; measure of feedback distortion |
| **Directive Latency**† | Time between executive directive issuance and operational feedback reception |
| **Operational Vertex** | Non-management node executing work; possesses tacit knowledge (Polanyi 1966) |
| **Feedback Fidelity** | Ratio of accurate operational signals received to total signals sent by operational vertices |
| **Epistemic Capture Index (ECI)** | Quantitative measure of executive delusion severity (defined in §3.3) |

## 3. Protocol Specification

### 3.1 Protocol Parameters

HOP defines four parameters that characterize the executive epistemic state.
Implementations MUST track all four.

#### 3.1.1 Omniscience Radius (OR)

**Requirement 1**: The Omniscience Radius OR(v) for executive vertex v
executive vertex v MUST be defined as the minimum graph distance from v to
any operational vertex w possessing relevant tacit knowledge.

$$\text{OR}(v) = \min_{w \in V_{ops}} \text{dist}_G(v, w)$$

where $V_{ops}$ is the set of operational vertices and $\text{dist}_G$ is
shortest-path distance in the organizational communication graph G.

**Requirement 2**: OR(v) SHALL be measured in communication hops, not
organizational chart levels. The official org chart distance SHALL NOT
substitute for actual communication path distance.

**Requirement 3**: Organizations SHOULD measure OR quarterly via network
analysis of communication metadata (email, Slack, meeting attendance).

#### 3.1.2 Directive Latency (DL)

**Requirement 4**: Directive Latency DL(v, t) for executive vertex v at
time t MUST be defined as the elapsed time between directive issuance and
receipt of verifiable operational feedback.

$$\text{DL}(v, t) = t_{feedback} - t_{directive}$$

where $t_{directive}$ is the timestamp of directive issuance and
$t_{feedback}$ is the timestamp of the first operational signal confirming
or refuting the directive's premise.

**Requirement 4.1**: DL measurements SHALL exclude performative
acknowledgments ("received," "working on it") and count only
substantive operational data (metrics, incidents, customer feedback).

**Requirement 4.2**: Organizations SHOULD instrument directive tracking
systems to capture DL automatically.

#### 3.1.3 Feedback Fidelity (FF)

**Requirement 5**: Feedback Fidelity FF(v) for executive vertex v MUST be
defined as the proportion of operational signals reaching v that accurately
represent ground truth.

$$\text{FF}(v) = \frac{|S_{accurate}(v)|}{|S_{total}(v)|}$$

where $S_{total}(v)$ is the set of all signals reaching v from operational
vertices, and $S_{accurate}(v) \subseteq S_{total}(v)$ is the subset
verified against ground truth.

**Requirement 5.1**: Ground truth verification SHALL use at least two
independent sources (e.g., system metrics + customer reports + incident data).

**Requirement 5.2**: FF(v) below 0.6 SHALL trigger mandatory HOP review
(see §4.2).

#### 3.1.4 Epistemic Capture Index (ECI)

**Requirement 6**: The Epistemic Capture Index ECI(v) for executive vertex v
MUST be computed as:

$$\text{ECI}(v) = \frac{\text{OR}(v) \times \text{DL}_{avg}(v)}
                  {\max(\text{FF}(v), \text{FF}_{min})}$$

where $\text{DL}_{avg}(v)$ is the rolling 90-day average of Directive Latency
for v, and $\text{FF}_{min} = 0.1$ is the minimum Feedback Fidelity floor
preventing division by near-zero and bounding ECI sensitivity.

**Requirement 6.1**: ECI(v) SHALL be reported as raw value (not log-transformed)
with classification thresholds on the raw scale:

| ECI Range | Classification | Action |
|-----------|----------------|--------|
| ECI < 10 | Grounded | No action |
| 10 ≤ ECI < 50 | Drifting | Quarterly CBP participation (RFC-0017) |
| 50 ≤ ECI < 200 | Captured | Mandatory shadowing program |
| ECI ≥ 200 | Critical | Executive recusal from operational decisions |

**Requirement 6.2**: ECI MUST be computed per executive vertex, not
aggregated. Aggregation destroys the signal.

### 3.2 State Machine

HOP operates through five states. The executive vertex transitions through
these states continuously; the protocol does not prescribe dwell times.

```ascii
+----------+  Directive   +----------+  Execution  +----------+
|PERCEPTION|  Issuance    |DIRECTIVE | (DL starts) |EXECUTION |
| (Observe)|  (OR up)     | (Decide) |             |  (Act)   |
+----------+------------> +----------+ ----------> +----------+
    ^                                                    |
    |                                                    v
    |                                            +------------+
    |                                            |  FEEDBACK  |
    |                                            | (DL ends,  |
    |                                            |  FF meas.) |
    |                                            +------------+
    |                                                    |
    |          Distortion (OR up, FF down)               |
    +----------------------------------------------------+
                         DISTORTION
```

#### State Definitions

| State | Description | Entry Condition | Exit Condition | Key Metrics |
|-------|-------------|-----------------|----------------|-------------|
| **PERCEPTION** | Executive receives filtered reports | Initial; after DISTORTION | Directive issuance | OR baseline, FF baseline |
| **DIRECTIVE** | Executive issues decision/directive | PERCEPTION exit | Directive acknowledged | OR at issuance, DL starts |
| **EXECUTION** | Operational vertices execute directive | DIRECTIVE exit | Feedback received | DL running, FF degrades |
| **FEEDBACK** | Operational signals return | EXECUTION exit | Feedback processed | DL measured, FF calculated |
| **DISTORTION** | Cognitive filtering between feedback and next observation | FEEDBACK exit | OR increase < 20% AND FF recovery > 15% | OR delta, FF delta, ECI updated |

#### Transition Requirements

**Requirement 7**: The PERCEPTION → DIRECTIVE transition MUST record
OR(v) at the moment of directive issuance. This is the baseline for
measuring distortion.

**Requirement 8**: The DIRECTIVE → EXECUTION transition MUST start the
Directive Latency timer. The timer stops at FEEDBACK entry.

**Requirement 9**: The EXECUTION → FEEDBACK transition MUST capture
Feedback Fidelity FF(v) using the dual-source verification method (§3.1.3).

**Requirement 10**: The FEEDBACK → DISTORTION transition MUST compute
ECI(v) using the formula in §3.1.4. ECI(v) SHALL be logged with timestamp.

**Requirement 11**: The DISTORTION → PERCEPTION transition represents
the cognitive filtering that occurs between feedback receipt and the next
observation cycle. Organizations SHOULD measure the OR increase during this
transition as "distortion delta." The transition occurs when:
- OR increase since FEEDBACK entry < 20% of baseline, AND
- FF recovery since FEEDBACK entry > 15% of baseline
If neither condition is met within 30 days, DISTORTION persists and ECI
is recomputed weekly.

### 3.3 Normative Requirements Summary

| Req | Parameter | MUST | SHOULD | MAY |
|-----|-----------|------|--------|-----|
| 1 | OR definition | YES | | |
| 2 | OR in hops | YES | | |
| 3 | Quarterly OR measurement | | YES | |
| 4 | DL definition | YES | | |
| 4.1 | DL excludes performative acks | YES | | |
| 4.2 | Auto DL tracking | | YES | |
| 5 | FF definition | YES | | |
| 5.1 | Dual-source verification | YES | | |
| 5.2 | FF < 0.6 triggers review | YES | | |
| 6 | ECI formula | YES | | |
| 6.1 | Log scale classification | YES | | |
| 6.2 | Per-vertex ECI | YES | | |
| 7 | PERCEPTION->DIRECTIVE: record OR | YES | | |
| 8 | DIRECTIVE->EXECUTION: start DL timer | YES | | |
| 9 | EXECUTION->FEEDBACK: capture FF | YES | | |
| 10 | FEEDBACK->DISTORTION: compute ECI | YES | | |
| 11 | DISTORTION->PERCEPTION: measure delta | | YES | |

## 4. Operational Considerations

### 4.1 Deployment Models

HOP is not a deployable management protocol. It is a diagnostic instrument.
Organizations MAY "implement" HOP by:

1. **Passive Monitoring**: Instrument existing communication systems to
   measure OR, DL, FF, ECI without executive awareness. This avoids
   Hawthorne effects but raises ethical concerns.

2. **Transparent Dashboard**: Publish ECI scores to all vertices including
   operational ones. This creates accountability but may trigger defensive
   filtering (further reducing FF).

3. **CBP Integration** (Recommended): Use ECI thresholds to trigger
    **recommended** Coffee-Break Protocol (RFC-0017) participation for executives
    with ECI ≥ 10. Participation is voluntary; the protocol's epistemic value
    depends on psychological safety (Edmondson 1999). Organizations SHOULD
    create conditions for voluntary participation (protected time, neutral venue)
    rather than mandating attendance.

### 4.2 Failure Modes

| Failure Mode | Mechanism | Detection | Mitigation |
|--------------|-----------|-----------|------------|
| **Metric Gaming** | Executives manipulate DL/FF measurements | ECI stable but outcomes worsen | Independent audit; Theorem-001 (CMT) cross-check |
| **Feedback Suppression** | Operational vertices stop sending bad news | FF drops sharply | CBP (RFC-0017) creates alternative channels |
| **Distortion Denial** | Executives reject ECI classification | ECI ≥ 100 but no action | Governance mandate; board-level ECI review |
| **CBP Avoidance** | Executives skip mandated coffee breaks | CBP attendance < threshold | Cultural; not technically enforceable |

### 4.3 Monitoring and Alerting

**Requirement 12**: Organizations implementing HOP monitoring SHALL alert
when:
- Any executive vertex ECI crosses a classification threshold
- FF(v) drops below 0.4 for any executive vertex
- OR(v) increases by >50% in a single quarter
- DL_avg(v) exceeds 30 days for operational directives

## 5. Security & Privacy Considerations

### 5.1 Epistemic Security

HOP measurements constitute **epistemic intelligence** — knowledge about
who knows what. Unauthorized access to ECI scores enables:
- Targeted influence operations (lobbying the "captured" executive)
- Strategic information withholding (hiding problems from high-OR executives)
- Career manipulation (promoting executives with low ECI who are genuinely grounded)

**Requirement 13**: ECI data SHALL be classified at the same sensitivity
level as executive compensation data. Access SHALL be limited to:
- The measured executive (self-access)
- Direct board oversight committee
- Independent organizational epistemology auditor (if appointed)

### 5.2 Privacy of Operational Vertices

Feedback Fidelity measurement requires sampling operational signals.
This may include private communications, incident reports, or code reviews.

**Requirement 14**: FF measurement SHALL use anonymized, aggregated signals.
Individual operational vertices SHALL NOT be identifiable in FF calculations.
Minimum aggregation group size: 5 vertices.

### 5.3 Managerial Eavesdropping (CBP Interaction)

RFC-0017 §7 identifies managerial attendance at coffee breaks as a
security vulnerability for CBP. HOP monitoring may incentivize executives
to attend CBP sessions for ECI reduction, thereby compromising CBP's
epistemic integrity.

**Requirement 15**: If CBP integration (§4.1 Model 3) is used, executives
with ECI ≥ 10 SHOULD attend CBP sessions in **listen-only mode** — they
SHALL NOT speak, ask questions, or identify as management during the
session. This mode is defined in RFC-0017 §3.1.1 as a CBP variant where
the participant observes without initiating CHP handshakes.

## 6. OSC Considerations

### 6.1 Registry Updates

This RFC requests the following OSC Registry updates:
- RFC-0001 allocated in Standards Track, architecture area (0001–0099)
- Keywords: hierarchy, executive-delusion, epistemic-capture, bounded-rationality
- See-also: RFC-0002, RFC-0003, RFC-0004

### 6.2 Code Points

HOP defines no code points. ECI thresholds are informational guidelines,
not protocol constants.

## 7. References

### 7.1 Normative References

[RFC-0002] Matos, R. "Conway's Law Generalization Protocol." RFC 0002,
Organizational Standards Consortium, 1987. https://rfc.osc.org/rfc0002

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol."
RFC 0003, Organizational Standards Consortium, 1992. https://rfc.osc.org/rfc0003

[RFC-0004] Matos, R. "Decision Theater Specification." RFC 0004,
Organizational Standards Consortium, 1998. https://rfc.osc.org/rfc0004

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017,
Organizational Standards Consortium, 2001. https://rfc.osc.org/rfc0017

### 7.2 Informative References

Akerlof, George A. 1970. "The Market for 'Lemons': Quality Uncertainty and
the Market Mechanism." *Quarterly Journal of Economics* 84 (3): 488–500.
https://doi.org/10.2307/1879431

Conway, Melvin E. 1968. "How Do Committees Invent?" *Datamation* 14 (4): 28–31.

Edmondson, Amy C. 1999. "Psychological Safety and Learning Behavior in Work
Teams." *Administrative Science Quarterly* 44 (2): 350–383.
https://doi.org/10.2307/2666999

Edmondson, Amy C. 2018. *The Fearless Organization: Creating Psychological
Safety in the Workplace for Learning, Innovation, and Growth*. Hoboken: Wiley.

Freeman, Linton C. 1977. "A Set of Measures of Centrality Based on
Betweenness." *Sociometry* 40 (1): 35–41. https://doi.org/10.2307/3033543

Granovetter, Mark S. 1973. "The Strength of Weak Ties." *American Journal of
Sociology* 78 (6): 1360–1380. https://doi.org/10.1086/225469

Nonaka, Ikujiro, and Hirotaka Takeuchi. 1995. *The Knowledge-Creating Company:
How Japanese Companies Create the Dynamics of Innovation*. New York: Oxford
University Press.

Polanyi, Michael. 1966. *The Tacit Dimension*. Chicago: University of Chicago
Press.

Simon, Herbert A. 1947. *Administrative Behavior: A Study of Decision-Making
Processes in Administrative Organization*. New York: Macmillan.

Waber, Ben, Jennifer Magnolfi, and Greg Lindsay. 2014. "Workspaces That Move
People." *Harvard Business Review* 92 (10): 68–77.

Wenger, Etienne. 1998. *Communities of Practice: Learning, Meaning, and
Identity*. Cambridge: Cambridge University Press.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 1987-11-02 | R. Matos | Initial draft (OSC founding document) |
| 0.2 | 1995-06-15 | R. Matos | Added ECI formula post-Nonaka visit |
| 0.3 | 2001-04-01 | R. Matos | Integrated CBP cross-ref (RFC-0017) |
| 0.4 | 2024-01-20 | R. Matos | Theorem-001 proof integration |
| 1.0 | 2026-07-18 | Rodolfo Matos | OEP canon alignment; dual-layer notice |

## Appendix B: Open Issues

1. **ECI Threshold Validation**: The classification thresholds (1, 10, 100)
   are heuristic. Empirical validation needed via longitudinal study.
   [UNVERIFIED]

2. **Non-Hierarchical Organizations**: HOP assumes tree-like hierarchy.
   Application to holacracies, flat orgs, or networked orgs undefined.
   [UNVERIFIED]

3. **Directive Latency Upper Bound**: No theoretical maximum DL established.
   Practical ceiling observed at ~90 days (Simon 1947 satisficing horizon).
   [UNVERIFIED]

4. **CBP Integration Ethics**: Mandatory CBP attendance for high-ECI executives
   creates power dynamic that may violate CBP's psychological safety
   preconditions (Edmondson 1999). Requires ethics review.
   [UNVERIFIED]

5. **Cross-Cultural Validity**: OR, DL, FF, ECI measured in Western
   knowledge-work contexts. High-power-distance cultures may show
   systematically different baselines. [UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Wenger, Granovetter, Nonaka, Edmondson, Simon,
> Conway, etc.) are accurate. The coffee machine, however, is real — and it
> is currently synchronizing more knowledge than this repository ever will.
