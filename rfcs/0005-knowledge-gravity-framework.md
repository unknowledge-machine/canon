---
rfc: "0005"
title: "Knowledge Gravity Measurement Framework (KGMF)"
stream: "Standards Track"
status: "DRAFT"
category: "Informational"
area: "epistemology"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "1995-06-15"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [2, 9]
keywords: [gravity, power-knowledge, centrality, knowledge-gravity, sponsorship]
abstract: |
  This document specifies the Knowledge Gravity Measurement Framework (KGMF),
  a protocol for quantifying the tendency of organizational knowledge to
  accumulate around power rather than truth. KGMF defines the Knowledge
  Gravity Index (KGI) as the log ratio of power centrality to truth centrality,
  and Escape Velocity as the sponsorship tier required to route knowledge past
  power nodes. Organizations with KGI > 1.0 experience systematic knowledge
  distortion; Escape Velocity > 3 indicates structural epistemic capture.
  While framed as a measurement protocol, KGMF functions analytically as a
  diagnostic instrument for organizational epistemology.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0005 — Knowledge Gravity Measurement Framework (KGMF)

## Abstract

This document specifies the Knowledge Gravity Measurement Framework (KGMF),
a protocol for quantifying the tendency of organizational knowledge to
accumulate around power rather than truth. KGMF defines the Knowledge
Gravity Index (KGI) as the log ratio of power centrality to truth centrality,
and Escape Velocity as the sponsorship tier required to route knowledge past
power nodes. Organizations with KGI > 1.0 experience systematic knowledge
distortion; Escape Velocity > 3 indicates structural epistemic capture.
While framed as a measurement protocol, KGMF functions analytically as a
diagnostic instrument for organizational epistemology.

> **Dual-Layer Notice**: This RFC employs the Knowledge Gravity Measurement
> Framework (KGMF) as a satirical vehicle for presenting peer-reviewed findings
> on organizational power-knowledge dynamics (Foucault 1977; Baldwin & Clark
> 2000; Foucault 1980; Bourdieu 1984). While KGMF employs satirical framing,
> the organizational claims are substantiated by the cited literature.
> Implementers should treat KGMF as an analytical lens, not a deployable
> measurement protocol — though some organizations have reportedly "implemented"
> it by mapping sponsorship requirements for cross-functional initiatives.

## 1. Introduction

### 1.1 Motivation

Michel Foucault (1977) observed that power and knowledge directly imply one
another: there is no power relation without the correlative constitution of a
field of knowledge, nor any knowledge that does not presuppose and constitute
power relations. Pierre Bourdieu (1984) demonstrated that cultural capital
accumulates around dominant positions. Baldwin and Clark (2000) formalized
this as the "mirroring hypothesis": technical dependencies mirror
organizational dependencies.

In knowledge-intensive organizations, this manifests as **knowledge gravity**:
knowledge artifacts, decisions, and expertise accumulate around power nodes
(formal authority, budget control, political influence) rather than truth nodes
(operational expertise, empirical validation, customer proximity).

The Knowledge Gravity Measurement Framework (KGMF) makes this distortion
measurable. By quantifying the gravitational pull of power on knowledge flows,
KGMF transforms a philosophical observation into a tractable metric: the
Knowledge Gravity Index (KGI).

### 1.2 Scope

This document specifies:
- Truth Centrality (TC): centrality of expertise vertices in knowledge graph
- Power Centrality (PC): centrality of authority vertices in influence graph
- Knowledge Gravity Index (KGI): log ratio log(PC / TC)
- Escape Velocity (EV): sponsorship tier (1–5) to bypass power nodes
- Gravity Well detection: power nodes with PC >> TC
- Integration with RFC-0001 (HOP), RFC-0002 (Conway), RFC-0003 (Fragmentation), RFC-0005 (Gravity)

### 1.3 Non-Goals

This document does not specify:
- How to redistribute knowledge gravity (organizational design; out of scope)
- Automated tooling for centrality computation (see BCP-XXXX)
- Remediation of gravity wells (see RFC-0007 Amnesia Prevention, RFC-0016 Memory Backup)

### 1.4 Relationship to Other RFCs

| RFC | Relationship |
|-----|--------------|
| RFC-0001 (HOP) | Executive delusion amplified by gravity; HOP measures
vertex, KGMF measures field |
| RFC-0002 (Conway) | Low MFM → gravity wells; structural misalignment
creates power-knowledge coupling |
| RFC-0003 (Fragmentation) | Gravity wells → formal/operational divergence; FI and KGI correlated |
| RFC-0004 (DTS) | Theater as gravity-management ritual; TQI and KGI correlated |
| Theorem-003 | Formal proof: knowledge accumulates around power; KGMF is measurement protocol |
| RFC-0017 (CBP) | Weak ties as gravity-resistant channels; CBP edges reduce KGI |

## 2. Terminology

| Term | Definition |
|------|------------|
| **Truth Vertex (T)** | Node in knowledge graph representing operational expertise (engineers, domain experts, customer-facing roles) |
| **Power Vertex (P)** | Node in influence graph representing formal authority (managers, directors, budget owners, decision-makers) |
| **Truth Centrality (TC)** | Weighted centrality of truth vertices in knowledge flow graph |
| **Power Centrality (PC)** | Weighted centrality of power vertices in influence graph |
| **Knowledge Gravity Index (KGI)** | log(PC / TC); log ratio of power to truth centrality |
| **Escape Velocity (EV)** | Sponsorship tier (1–5) required to route knowledge past power nodes |
| **Gravity Well** | Power vertex with PC >> TC; attracts knowledge artifacts disproportionately |
| **Sponsorship Tier** | Organizational level required to sponsor cross-gravity knowledge transfer (1=team, 2=group, 3=department, 4=division, 5=executive) |
| **Knowledge Flow Graph** | Directed graph where vertices = knowledge artifacts + humans; edges = citations, dependencies, transfers |
| **Influence Graph** | Directed graph where vertices = organizational roles; edges = reporting, budget, delegation, veto |

## 3. Protocol Specification

### 3.1 Vertex Classification

**Requirement 1**: Implementations MUST classify all vertices in the
organizational graph as either Truth vertices (T), Power vertices (P),
or Hybrid (H).

**Requirement 2**: Truth vertices (T) MUST be identified by triangulating four data sources:
- **Git**: Commit frequency, lines changed, areas owned in codebase
- **PR Reviews**: Review frequency, depth, acceptance rate on others' PRs
- **Slack/Q&A**: Question answering frequency, upvotes, accepted answers in technical channels
- **Survey**: Quarterly peer nomination: "Who do you go to for X?"

**Requirement 3**: Power vertices (P) MUST be identified by triangulating four data sources:
- **Org Chart**: Formal reporting lines, span of control
- **Calendar**: Meeting frequency, attendee diversity, decision-making meetings
- **Budget**: Spend authority, headcount approval, vendor approval limits
- **Delegation**: Explicit delegation of decision rights, veto power, escalation paths

**Requirement 4**: Vertices scoring high on both T and P dimensions are
classified as Hybrid (H). Hybrid vertices MUST be tracked separately as
they represent the "translation layer" between truth and power.

### 3.2 Centrality Computation

**Requirement 5**: Truth Centrality (TC) MUST be computed as the
weighted PageRank of truth vertices in the Knowledge Flow Graph:

```
TC(v) = (1-d) + d × Σ_{u∈In(v)} TC(u) / OutDeg(u)
```

where d = 0.85 (damping factor), In(v) = incoming knowledge
edges, OutDeg = outgoing knowledge edges.

Knowledge edges include: citations, dependencies, PR references,
Slack links, document references, ticket links.

**Requirement 6**: Power Centrality (PC) MUST be computed as the
weighted eigenvector centrality of power vertices in the Influence
Graph:

```
PC(v) = λ × Σ_{u∈In(v)} w(u,v) × PC(u)
```

where w(u,v) = influence weight (budget weight + reporting
weight + veto weight), λ = principal eigenvalue.

Influence edges include: reporting (weight 1.0), budget approval
(weight 1.5), veto rights (weight 2.0), delegation (weight 0.8).

### 3.3 Knowledge Gravity Index (KGI)

**Requirement 7**: The Knowledge Gravity Index KGI MUST be computed as:

```
KGI = log10(PC_avg / TC_avg)
```

where PC_avg = mean power centrality of all power vertices,
TC_avg = mean truth centrality of all truth vertices.

**Requirement 7.1**: KGI interpretation thresholds:

| KGI Range | Classification | Interpretation |
|-----------|----------------|----------------|
| KGI < -0.5 | **Truth-Dominant** | Expertise outweighs authority; healthy epistemic environment |
| -0.5 ≤ KGI < 0 | **Balanced** | Power and expertise roughly aligned |
| 0 ≤ KGI < 0.5 | **Power-Drift** | Authority beginning to outweigh expertise |
| 0.5 ≤ KGI < 1.0 | **Power-Dominant** | Authority significantly outweighs expertise |
| KGI ≥ 1.0 | **Critical Gravity** | Knowledge orbits power; truth cannot escape |

**Requirement 8**: Implementations MUST compute and report KGI per
organizational unit (team, group, department) and aggregated.

### 3.4 Escape Velocity (EV)

**Requirement 9**: Escape Velocity (EV) for a knowledge artifact MUST be
computed as the minimum sponsorship tier required to route the artifact
from its origin truth vertex to a target power vertex without
gravitational capture.

**Requirement 9.1**: Sponsorship tiers (1–5):

| Tier | Level | Authority | Typical Scope |
|------|-------|-----------|---------------|
| 1 | Team Lead | Sprint scope | Team-level decisions |
| 2 | Engineering Manager | Team/group scope | Cross-team technical decisions |
| 3 | Director | Department scope | Cross-functional initiatives |
| 4 | VP / Division Head | Division scope | Strategic investments, org structure |
| 5 | C-Level / Executive | Enterprise scope | Strategy, culture, existential decisions |

**Requirement 9.2**: EV computation:
- For each power vertex on shortest path from truth vertex to target, sum required tier
- EV = max tier encountered (bottleneck)
- EV = 1 if direct truth-to-power edge exists (no intermediate power nodes)

**Requirement 9.3**: EV interpretation:

| EV | Classification | Interpretation |
|----|----------------|----------------|
| EV = 1 | **Free Flow** | Knowledge routes directly; no sponsorship needed |
| EV = 2 | **Team Gate** | Team lead sponsorship sufficient |
| EV = 3 | **Department Gate** | Director sponsorship required |
| EV = 4 | **Division Gate** | VP sponsorship required |
| EV = 5 | **Executive Gate** | C-level sponsorship required; structural barrier |

### 3.5 Gravity Well Detection

**Requirement 10**: Implementations MUST identify gravity wells: power
vertices where PC(v) > 2 × median(PC) AND TC(v) < 0.5 × median(TC).

**Requirement 10.1**: Gravity wells MUST be reported with:
- Vertex ID and role
- PC/TC ratio
- Knowledge artifacts attracted (count, types)
- Escape Velocity from well
- Affected truth vertices (dependency count)

### 3.6 Normative Requirements Summary

| Req | Parameter | MUST | SHOULD | MAY |
|-----|-----------|------|--------|-----|
| 1 | Vertex classification (T/P/H) | YES | | |
| 2 | Truth vertex triangulation (4 sources) | YES | | |
| 3 | Power vertex triangulation (4 sources) | YES | | |
| 4 | Hybrid tracking | YES | | |
| 5 | TC via PageRank | YES | | |
| 6 | PC via eigenvector centrality | YES | | |
| 7 | KGI = log(PC/TC) | YES | | |
| 7.1 | KGI thresholds table | YES | | |
| 8 | EV per artifact | YES | | |
| 9.1 | Sponsorship tiers 1–5 | YES | | |
| 9.2 | EV computation | YES | | |
| 9.3 | EV thresholds table | YES | | |
| 10 | Gravity well detection | YES | | |
| 10.1 | Well reporting format | YES | | |

## 4. Operational Considerations

### 4.1 Deployment Models

KGMF is a diagnostic, not a restructuring protocol. Organizations MAY apply it as:

1. **Quarterly Gravity Scan**: Compute KGI + EV for all units. Report to C-suite.
2. **Initiative Routing**: Compute EV for proposed cross-functional initiatives. Flag EV > 3.
3. **Gravity Well Remediation**: Target identified wells with CBP
intensification (RFC-0017), rotation programs, or delegation.
4. **Executive Dashboard**: KGI trend + top-5 gravity wells + EV distribution.

### 4.2 Failure Modes

| Failure Mode | Mechanism | Detection | Mitigation |
|--------------|-----------|-----------|------------|
| **Centrality Gaming** | Power vertices create fake knowledge edges | TC rises but outcomes don't improve | Cross-validate with outcomes; RFC-0003 FI cross-check |
| **Survey Manipulation** | Truth vertex nominations gamed | Survey nominations ≠ digital trace | Weight digital trace higher (α=0.7) |
| **Gravity Well Denial** | Power vertices reject well classification | KGI > 1.0 but no action | Mandate review per RFC-0016 |
| **Hybrid Masking** | Hybrid vertices mask power vertices | H vertices have high PC but counted as T | Separate H tracking mandatory (Req 4) |

### 4.3 Monitoring and Alerting

**Requirement 11**: Organizations computing KGMF SHALL alert when:
- Any unit KGI crosses threshold (-0.5, 0, 0.5, 1.0)
- Any unit EV > 3 for > 30 days
- New gravity well detected (PC/TC ratio > 4)
- Hybrid vertex count drops > 20% (translation layer eroding)

## 5. Security & Privacy Considerations

### 5.1 Epistemic Security

KGI and gravity wells reveal:
- Which units are epistemically captured (political vulnerability)
- Which truth vertices are isolated (bus factor)
- Which power vertices are gravity wells (influence mapping)

**Requirement 12**: KGI data SHALL be classified at same level as org
restructuring plans. Access limited to: measured units, C-suite,
independent epistemology auditor.

### 5.2 Individual Privacy

Centrality computation uses digital traces (Git, Slack, Calendar,
Budget).

**Requirement 13**: Aggregation to role level (minimum 3 individuals)
before centrality computation. Individual-level graphs PROHIBITED for
KGI reporting.

**Requirement 14**: Survey responses MUST be anonymized. Minimum
response threshold: 3 respondents per role.

### 5.3 CBP Integrity (RFC-0017 §7)

KGMF uses CBP edges (weak ties) in knowledge graph. If KGMF
monitoring incentivizes executives to attend coffee breaks for
"centrality boosting," CBP's epistemic integrity is compromised.

**Requirement 15**: CBP edges used in KGMF MUST be anonymized and
aggregated. No executive attendance tracking for KGI purposes.

## 6. OSC Considerations

### 6.1 Registry Updates

This RFC requests:
- RFC-0005 allocated in Standards Track, epistemology area (0200–0299)
- Keywords: gravity, power-knowledge, centrality, knowledge-gravity, sponsorship
- See-also: RFC-0001, RFC-0002, RFC-0003, Theorem-003

### 6.2 Code Points

KGMF defines no code points. KGI thresholds and sponsorship tiers are informational guidelines.

## 7. References

### 7.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001,
Organizational Standards Consortium, 1987. https://rfc.osc.org/rfc0001

[RFC-0002] Matos, R. "Conway's Law Generalization Protocol." RFC 0002,
Organizational Standards Consortium, 1987. https://rfc.osc.org/rfc0002

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003,
Organizational Standards Consortium, 1992. https://rfc.osc.org/rfc0003

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017,
Organizational Standards Consortium, 2001. https://rfc.osc.org/rfc0017

### 7.2 Informative References

Baldwin, Carliss Y., and Kim B. Clark. 2000. *Design Rules: The Power of
Modularity*. Cambridge, MA: MIT Press.

Bourdieu, Pierre. 1984. *Distinction: A Social Critique of the Judgement of
Taste*. Cambridge, MA: Harvard University Press.

Foucault, Michel. 1977. *Discipline and Punish: The Birth of the Prison*.
New York: Vintage.

Foucault, Michel. 1980. *Power/Knowledge: Selected Interviews and Other
Writings 1972–1977*. New York: Pantheon Books.

Page, Lawrence, et al. 1999. "The PageRank Citation Ranking: Bringing Order
to the Web." Stanford InfoLab Technical Report.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 1995-06-15 | R. Matos | Initial draft post-Nonaka visit |
| 0.2 | 2000-06-15 | R. Matos | Baldwin & Clark integration; centrality metrics |
| 0.3 | 2018-09-01 | R. Matos | PageRank + eigenvector centrality; sponsorship tiers |
| 1.0 | 2026-07-18 | Rodolfo Matos | OEP canon alignment; log ratio KGI; sponsorship tiers |

## Appendix B: Open Issues

1. **KGI Causal Direction**: Does high KGI cause poor outcomes, or do
poor outcomes attract gravity? Longitudinal RCT needed.
[UNVERIFIED]

2. **Centrality Metric Selection**: PageRank vs eigenvector vs
betweenness for TC/PC. Impact on KGI stability unknown.
[UNVERIFIED]

3. **Sponsorship Tier Calibration**: Tier boundaries (1–5) based on
conventional org structures. Flat/holacratic orgs need calibration.
[UNVERIFIED]

4. **Gravity Well Remediation**: What interventions reduce PC/TC
ratio? Rotation? Delegation? CBP? [UNVERIFIED]

5. **Cross-Cultural Gravity**: High-power-distance cultures may have
systematically higher baseline KGI. [UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Foucault, Bourdieu, Baldwin, Clark, Page,
> etc.) are accurate. The coffee machine, however, is real — and it is
> currently synchronizing more knowledge than this repository ever will.