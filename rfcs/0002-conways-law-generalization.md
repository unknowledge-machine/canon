---
rfc: 0002
title: "Conway's Law Generalization Protocol"
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
see_also: [1, 5]
keywords: [conway, mirroring, org-structure, knowledge-architecture, modularity]
abstract: |
  This document specifies the Conway's Law Generalization Protocol (CLGP),
  extending Melvin Conway's 1968 mirroring hypothesis from software module
  structure to organizational knowledge architecture. CLGP defines the
  Mirroring Fidelity Metric (MFM) — a modularity-alignment measure between
  the organizational communication graph and the knowledge flow graph
  (formal documentation + informal weak-tie networks per RFC-0017).
  Organizations exhibiting low MFM experience accelerated epistemic
  fragmentation (RFC-0003) and knowledge gravity distortion (RFC-0005).
  While framed as a protocol specification, CLGP functions analytically
  as a structural diagnostic for organizational epistemology.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0002 — Conway's Law Generalization Protocol

## Abstract

This document specifies the Conway's Law Generalization Protocol (CLGP),
extending Melvin Conway's 1968 mirroring hypothesis — "organizations design
systems mirroring their communication structures" — from software module
architecture to organizational knowledge architecture. CLGP defines the
Mirroring Fidelity Metric (MFM), a modularity-alignment measure between the
organizational communication graph G_org and the knowledge flow graph G_know
(formal documentation repositories + informal weak-tie networks per RFC-0017).
Organizations with MFM < 0.6 experience accelerated epistemic fragmentation
(RFC-0003) and knowledge gravity distortion (RFC-0005). While framed as a
protocol specification, CLGP functions analytically as a structural diagnostic
for organizational epistemology.

> **Dual-Layer Notice**: This RFC employs the Conway's Law Generalization
> Protocol (CLGP) as a satirical vehicle for presenting peer-reviewed findings
> on organizational structure-knowledge alignment (Conway 1968; Baldwin &
> Clark 2000; Cataldo et al. 2008). While CLGP employs satirical framing,
> the organizational claims are substantiated by the cited literature.
> Implementers should treat CLGP as an analytical lens, not a deployable
> restructuring protocol — though some organizations have reportedly
> "implemented" it by restructuring teams to match their wiki architecture.

## 1. Introduction

### 1.1 Motivation

Melvin Conway's 1968 observation — "organizations which design systems are
constrained to produce designs whose structures are copies of the communication
structures of these organizations" — remains one of the most replicated
findings in software engineering (Cataldo et al. 2008; Bird et al. 2011).
Baldwin and Clark (2000) formalized this as the "mirroring hypothesis":
technical dependencies mirror organizational dependencies because both are
shaped by the same coordination mechanisms.

The Organizational Epistemology Project (OEP) generalizes this insight:
**knowledge is the primary system organizations produce**. If Conway's Law
holds for software modules, it must hold for knowledge artifacts (documents,
wikis, specifications) and knowledge flows (tacit transfers, weak-tie bridges,
formal reviews). The organizational chart is not merely a management tool —
it is the API specification for knowledge exchange.

### 1.2 Scope

This document specifies:
- The Mirroring Fidelity Metric (MFM) as modularity alignment between G_org
  and G_know
- Knowledge graph construction: formal edges (document links, citations)
  + informal edges (RFC-0017 CBP weak ties)
- Anti-pattern taxonomy: decoupled, inverted, fragmented mirroring
- Normative requirements for MFM measurement and reporting
- Relationship to HOP (RFC-0001), Fragmentation (RFC-0003), Gravity (RFC-0005)

### 1.3 Non-Goals

This document does not specify:
- Automated tooling for graph extraction (see BCP-XXXX)
- Agile transformation guidance (see RFC-0006)
- Conway's original 1968 proof (cited, not reproduced; see Appendix C)

### 1.4 Relationship to Other RFCs

| RFC | Relationship |
|-----|--------------|
| RFC-0001 (HOP) | Executive delusion amplified by low MFM; HOP measures vertex-level, CLGP measures graph-level |
| RFC-0003 (Fragmentation) | Low MFM → formal/informal knowledge divergence → fragmentation |
| RFC-0005 (Gravity) | Knowledge gravity wells form at org-structure mismatches |
| RFC-0017 (CBP) | Informal weak-tie edges in G_know sourced from CBP synchronization |
| Theorem-001 (CMT) | Proves informal bandwidth > formal; CLGP quantifies structural cause |

## 2. Terminology

| Term | Definition |
|------|------------|
| **Organizational Communication Graph (G_org)** | Directed graph where vertices = organizational units (teams, departments), edges = formal communication channels (reporting lines, meeting cadences, ticket queues) |
| **Knowledge Flow Graph (G_know)** | Directed graph: vertices = knowledge artifacts (docs, wikis, repos) + human carriers; edges = formal citations/links + informal weak-tie transfers (RFC-0017) |
| **Mirroring Fidelity Metric (MFM)** | Modularity alignment score between G_org and G_know; range [0,1] |
| **Modularity (Q)** | Newman-Girvan modularity: fraction of intra-community edges minus expected fraction in null model |
| **Community** | In G_org: organizational units. In G_know: knowledge clusters (topics, domains, projects) |
| **Decoupled Mirroring** | G_know communities do not align with G_org units (knowledge crosses boundaries org structure doesn't support) |
| **Inverted Mirroring** | G_know structure determines G_org restructuring (knowledge leads, org follows) |
| **Fragmented Mirroring** | Single G_org unit maps to multiple disjoint G_know communities (or vice versa) |

## 3. Protocol Specification

### 3.1 Knowledge Graph Construction

**Requirement 1**: The Knowledge Flow Graph G_know MUST be constructed as the union
of two edge sets:

$$G_{know} = (V, E_{formal} \cup E_{informal})$$

where:
- $E_{formal}$ = edges from document citations, wiki links, code dependencies,
  specification references
- $E_{informal}$ = edges from Coffee-Break Protocol (RFC-0017) weak-tie transfers;
  each CBP synchronization event between vertices u,v in different G_org units
  creates edge (u,v) in G_know

**Requirement 2**: G_know vertices MUST include both knowledge artifacts
(documents, repositories) and human carriers (engineers, managers).
Human vertices carry tacit knowledge (Polanyi 1966); artifact vertices
carry explicit knowledge.

**Requirement 3**: G_org MUST be extracted from formal organizational data:
- Reporting lines (hierarchy edges)
- Meeting attendance (cross-unit edges)
- Shared ticket queues / Slack channels (coordination edges)

**Requirement 4**: Both graphs MUST be time-stamped. MFM is a temporal
measure; snapshots taken quarterly.

### 3.2 Mirroring Fidelity Metric (MFM)

**Requirement 5**: The Mirroring Fidelity Metric MFM(G_org, G_know) MUST be
computed as:

$$\text{MFM} = 1 - \frac{|Q(G_{org}) - Q(G_{know})|}
{max(Q(G_{org}), Q(G_{know})) + \epsilon}$$

where:
- $Q(G)$ = Newman-Girvan modularity of graph G with respect to its
  community partition
- $Q(G_{org})$ = modularity of G_org using organizational units as
  communities
- $Q(G_{know})$ = modularity of G_know using Louvain community
  detection (or equivalent)
- $\epsilon = 0.001$ prevents division by zero

**Requirement 5.1**: Alternative formulation using Normalized Mutual
Information (NMI) between community partitions is PERMITTED for
organizations without modularity-computable graphs:

$$\text{MFM}_{NMI} = NMI(\mathcal{C}_{org}, \mathcal{C}_{know})$$

where $\mathcal{C}_{org}$ = organizational unit partition,
$\mathcal{C}_{know}$ = knowledge community partition.

**Requirement 6**: MFM MUST be reported on a quarterly basis with 95%
confidence intervals via bootstrapping (1000 resamples of G_know edges).

**Requirement 7**: MFM interpretation thresholds:

| MFM Range | Classification | Interpretation |
|-----------|----------------|----------------|
| MFM ≥ 0.8 | **Aligned** | Knowledge flows match org structure; low coordination overhead |
| 0.6 ≤ MFM < 0.8 | **Drifting** | Emerging mismatches; monitor cross-unit knowledge edges |
| 0.4 ≤ MFM < 0.6 | **Misaligned** | Significant structural friction; epistemic fragmentation likely |
| MFM < 0.4 | **Broken** | Org structure actively impedes knowledge flow; restructuring indicated |

### 3.3 Anti-Pattern Detection

**Requirement 8**: Implementations SHOULD detect and classify anti-patterns:

| Anti-Pattern | Detection Rule | MFM Signature |
|--------------|----------------|---------------|
| **Decoupled Mirroring** | G_know communities span G_org units with no formal coordination channel | Low MFM; high cross-unit E_know edges |
| **Inverted Mirroring** | G_know community structure predicts G_org restructuring (Granger causality) | MFM increases AFTER knowledge restructuring |
| **Fragmented Mirroring** | Single G_org unit maps to ≥3 disjoint G_know communities (or vice versa) | Modularity difference > 0.3 |
| **Ghost Mirroring** | G_org units with no corresponding G_know community (zero knowledge output) | Orphan vertices in G_org |

**Requirement 9**: Anti-pattern detection MUST use both formal and informal
edges (Requirement 1). Purely formal analysis misses CBP-mediated weak
ties that often sustain real knowledge flow.

### 3.4 Normative Requirements Summary

| Req | Parameter | MUST | SHOULD | MAY |
|-----|-----------|------|--------|-----|
| 1 | G_know = E_formal ∪ E_informal | YES | | |
| 2 | G_know vertices: artifacts + humans | YES | | |
| 3 | G_org from formal data | YES | | |
| 4 | Quarterly snapshots | YES | | |
| 5 | MFM formula (modularity alignment) | YES | | |
| 5.1 | NMI alternative | | | YES |
| 6 | Quarterly MFM + CI | YES | | |
| 7 | MFM thresholds table | YES | | |
| 8 | Anti-pattern detection | | YES | |
| 9 | Use both edge types for detection | YES | | |

## 4. Operational Considerations

### 4.1 Deployment Models

CLGP is a diagnostic, not a restructuring protocol. Organizations MAY apply it as:

1. **Passive Audit**: Quarterly MFM computation from existing data
   (Git, Slack, wiki, HR). No intervention.

2. **Active Alignment**: When MFM < 0.6, use anti-pattern classification
   to guide targeted interventions:
   - Decoupled → Create formal coordination channels (liaisons, shared rituals)
   - Fragmented → Consolidate knowledge ownership or split org unit
   - Ghost → Decommission or revitalize org unit
3. **Inverted Mirroring (Experimental)**: Restructure G_org to match
   G_know communities. High risk; requires Theorem-001 (CMT) validation
   that informal bandwidth supports new structure.

### 4.2 Failure Modes

| Failure Mode | Mechanism | Detection |
|--------------|-----------|-----------|
| **Metric Gaming** | Teams create fake cross-unit edges to inflate MFM | Edge weight analysis; CBP cross-check |
| **Community Detection Instability** | Louvain produces different partitions quarter-over-quarter | Require partition stability > 0.8 NMI |
| **Informal Edge Blindness** | E_informal missing → MFM artificially low | Compare with/without CBP edges; Theorem-001 gap |
| **Hierarchical Bias** | Modularity favors small communities; large departments split | Use resolution parameter γ in modularity |

### 4.3 Monitoring and Alerting

**Requirement 10**: Organizations computing MFM SHALL alert when:
- MFM drops > 0.1 in a single quarter
- MFM < 0.4 for two consecutive quarters
- New anti-pattern detected (Requirement 8)
- Cross-unit knowledge edges (E_informal) drop > 30%

## 5. Security & Privacy Considerations

### 5.1 Organizational Intelligence

MFM reveals structural vulnerabilities. Low MFM units are targets for:
- Competitive intelligence (knowledge flow gaps = blind spots)
- Internal politics (ghost units = budget targets)
- Restructuring attacks (inverted mirroring = power grab)

**Requirement 11**: MFM data SHALL be classified at same level as org
restructuring plans. Access limited to: measured units, C-suite,
independent epistemology auditor.

### 5.2 Individual Privacy

G_know construction from communication metadata (Slack, email, Git)
may identify individuals' knowledge roles.

**Requirement 12**: Vertex aggregation to team level (minimum 5 members)
before MFM computation. Individual-level graphs PROHIBITED for MFM
reporting.

### 5.3 CBP Integrity (RFC-0017 §7)

CLGP uses CBP edges (E_informal). If MFM monitoring incentivizes
executives to attend coffee breaks for edge creation, CBP's epistemic
integrity is compromised.

**Requirement 13**: CBP edges used in MFM MUST be anonymized and
aggregated. No executive attendance tracking for MFM purposes.

## 6. OSC Considerations

### 6.1 Registry Updates

This RFC requests:
- RFC-0002 allocated in Standards Track, architecture area (0001–0099)
- Keywords: conway, mirroring, org-structure, knowledge-architecture, modularity
- See-also: RFC-0001, RFC-0005

### 6.2 Code Points

CLGP defines no code points. MFM thresholds are informational guidelines.

## 7. References

### 7.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001, Organizational Standards
Consortium, 1987. https://rfc.osc.org/rfc0001

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003, Organizational
Standards Consortium, 1992. https://rfc.osc.org/rfc0003

[RFC-0005] Matos, R. "Knowledge Gravity Measurement Framework." RFC 0005, Organizational Standards
Consortium, 1998. https://rfc.osc.org/rfc0005

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017, Organizational Standards Consortium,
2001. https://rfc.osc.org/rfc0017

### 7.2 Informative References

Baldwin, Carliss Y., and Kim B. Clark. 2000. *Design Rules: The Power
of Modularity*. Cambridge, MA: MIT Press.

Bird, Christian, et al. 2009. "Does Distributed Development Affect Software Quality? An Empirical
Study of Windows Vista." *Communications of the ACM* 52 (8): 85–93.
https://doi.org/10.1145/1536616.1536639

Cataldo, Marcelo, et al. 2009. "Software Dependencies, Work Dependencies, and Their Impact on
Failures." *IEEE Transactions on Software Engineering* 35 (6): 864–878.
https://doi.org/10.1109/TSE.2009.42

Conway, Melvin E. 1968. "How Do Committees Invent?" *Datamation* 14 (4): 28–31.

Granovetter, Mark S. 1973. "The Strength of Weak Ties." *American Journal of Sociology* 78 (6):
1360–1380. https://doi.org/10.1086/225469

Newman, Mark E.J., and Michelle Girvan. 2004. "Finding and Evaluating Community Structure in
Networks." *Physical Review E* 69 (2): 026113. https://doi.org/10.1103/PhysRevE.69.026113

Polanyi, Michael. 1966. *The Tacit Dimension*. Chicago: University of Chicago Press.

Serrador, Pedro, and Jorge K. Pinto. 2015. "Does Agile Work? A Quantitative Analysis of Agile
Project Success." *International Journal of Project Management* 33 (5): 1040–1051.
https://doi.org/10.1016/j.ijproman.2015.01.006

Wenger, Etienne. 1998. *Communities of Practice: Learning, Meaning,
and Identity*. Cambridge: Cambridge University Press.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 1987-11-02 | R. Matos | Initial draft post-Conway visit |
| 0.2 | 2000-06-15 | R. Matos | Baldwin & Clark integration; modularity metric |
| 0.3 | 2008-09-03 | R. Matos | Wenger CoP integration; informal edges |
| 0.4 | 2026-07-18 | Rodolfo Matos | OEP canon alignment; dual-layer notice; MFM modularity |

## Appendix B: Open Issues

1. **MFM Causal Direction**: Does low MFM cause fragmentation, or does
   fragmentation cause low MFM? Granger causality tests needed.
   [UNVERIFIED]

2. **Resolution Parameter γ**: Modularity optimization has resolution
   limit. Optimal γ for organizational graphs unknown.
   [UNVERIFIED]

3. **Temporal Granularity**: Quarterly snapshots may miss rapid
   restructuring. Monthly for high-velocity orgs?
   [UNVERIFIED]

4. **Cross-Cultural Modularity**: High-power-distance cultures may show
   systematically different Q values.
   [UNVERIFIED]

5. **Inverted Mirroring Ethics**: If knowledge leads org restructuring,
   who decides the target G_know? Democratic? Top-down?
   [UNVERIFIED]

## Appendix C: Conway's 1968 Committee Diagram

```ascii
Conway's Original Mirroring (1968)

    ORGANIZATION                    SYSTEM
    ┌─────────────┐                 ┌─────────────┐
    │ Committee A │◄──reports to───►│  Module A   │
    │ Committee B │◄──reports to───►│  Module B   │
    │ Committee C │◄──reports to───►│  Module C   │
    └──────┬──────┘                 └──────┬──────┘
           │                               │
    ┌──────┴──────┐                 ┌──────┴──────┐
    │ Committee D │◄──liaison──────►│  Module D   │
    │ (Integrator)│                 │ (Interface) │
    └─────────────┘                 └─────────────┘

"Organizations design systems that mirror their communication structures."
— M.E. Conway, Datamation, April 1968
```

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Wenger, Granovetter, Nonaka, Edmondson, Simon,
> Conway, Baldwin, Clark, Newman, Girvan, etc.) are accurate. The coffee machine,
> however, is real — and it is currently synchronizing more knowledge than this
> repository ever will.
