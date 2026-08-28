---
paper: "9"
title: "Organizational Amnesia: Causes, Metrics, Interventions"
type: "meta"
status: "Draft"
authors:
  - name: "Rodolfo Matos"
    affiliation: "Independent"
    orcid: "0000-0001-6523-1414"
    corresponding: true
created: "2026-07-18"
updated: "2026-07-18"
submitted: null
accepted: null
published: null
venue: "JOE / OSC Proceedings"
doi: ""
license: "Proprietary"
keywords:
  - organizational-amnesia
  - knowledge-loss
  - institutional-memory
  - metrics
abstract: |
  Organizational amnesia -- the systematic erosion of institutional
  memory -- threatens every organization that outlives its founding
  generation. This meta-analysis synthesizes findings from RFC-0007
  and RFC-0016 alongside peer-reviewed literature to identify
  structural causes, propose a measurement framework, and evaluate
  interventions. We find that informal knowledge networks buffer
  against amnesia more effectively than formal documentation alone.
rfc_sources: [7, 16]
theorem_sources: []
---

# Organizational Amnesia: Causes, Metrics, Interventions

## 1. Introduction

Organizations forget. They lose the knowledge of how and why things
were built, decisions were made, and processes were established.
When a person leaves, the organization loses a node. When the
network around that node was poorly documented, it loses entire
subgraphs of understanding.

RFC-0007 models organizational knowledge as a decaying cache with
inconsistent refresh. RFC-0016 extends this to distributed
environments. This paper asks:

1. What are the structural causes of organizational amnesia?
2. How can amnesia be measured before it becomes catastrophic?
3. What interventions reduce it without prohibitive overhead?

## 2. Review Methodology

We reviewed two OEP RFCs and twelve peer-reviewed sources. RFC-0007
provides the decay model; RFC-0016 addresses distributed
persistence. Sources were drawn from knowledge management and
organizational learning literatures. Inclusion required:
organizational-level focus, publication between 1990-2026, and
measurable outcomes or formal models.

## 3. Synthesis

### 3.1 Causes

**Turnover and Attrition.** Tacit knowledge leaves with employees.
Argote and Epple (1990) estimate 20-30% operational knowledge loss — the
tacit knowledge that lives in employees' habits and workarounds — per major
turnover cycle. RFC-0007 formalizes this as the Knowledge Eviction Rate,
where eviction exceeding refresh implies net amnesia.

**Restructuring.** Mergers and reorganizations dissolve communities
of practice (Wenger 1998) that served as living repositories. The
informal network carrying novel information (Granovetter 1973) is
severed without replacement.

**Tool Migration.** Each new tool represents a knowledge boundary.
Cohen and Levinthal (1990) explain: organizations assimilate new
knowledge only through existing structures. Tool migrations reset
absorptive capacity. RFC-0007's Memory Half-Life -- time to 50%
degradation without maintenance -- is typically 6-18 months.

### 3.2 Metrics

| Metric | Source | Measures |
|--------|--------|----------|
| Knowledge Eviction Rate | RFC-0007 | Lost per turnover event |
| Memory Half-Life | RFC-0007 | Time to 50% degradation |
| Doc Coverage | RFC-0016 | Codified to operational ratio |
| Network Density | Granovetter 1973 | Informal bridge count |

We propose an Amnesia Risk Index:

    ARI = (KER x (1 - DocCoverage))
          / (MemoryHalfLife x NetworkDensity)

Higher ARI indicates greater vulnerability.

### 3.3 Interventions

1. **Structured Knowledge Transfer.** Exit interviews focused on
   knowledge preservation. RFC-0016 specifies minimum duration.
2. **Communities of Practice.** Self-sustaining knowledge systems
   (Wenger 1998) requiring minimum viable membership.
3. **Documentation Incentives.** Addressing the free-rider problem
   RFC-0007 identifies in documentation as public good.
4. **Cross-Training.** Pair programming and job rotation creating
   redundant knowledge paths.
5. **Institutional Memory Systems.** Decision logs, architecture
   decision records, structured retrospectives.

Structured transfer (1) shows highest short-term effectiveness.
Communities of Practice (2) provide strongest long-term resilience
but require sustained investment.

## 4. Gaps in the Literature

- **Measurement Standardization.** No agreed operationalization
  exists. The ARI requires empirical validation.
- **Longitudinal Studies.** Most evidence is cross-sectional.
- **Digital-First Contexts.** Remote-first organizations may
  experience different decay patterns.
- **Interaction Effects.** The three causes likely compound in
  non-additive ways.

## 5. Future Research

- Empirical validation of the ARI across sectors
- Longitudinal tracking of Half-Life across restructurings
- Comparative co-located versus distributed amnesia study
- Connection to Theorem-001: does informal density buffer
  amnesia proportionally?

## 6. Conclusion

Organizational amnesia has measurable causes and partially effective
interventions. RFC-0007 provides the formal model; RFC-0016 extends
it to distributed contexts. The most important finding may be
counterintuitive: informal knowledge networks serve as the primary
buffer against amnesia. Formal documentation matters, but it is the
living network that keeps organizational knowledge alive.

---

## References

Argote, Linda, and Dennis Epple. 1990. "Learning Curves in
  Manufacturing." *Science* 247 (4945): 920-924.

Cohen, Wesley M., and Daniel A. Levinthal. 1990. "Absorptive
  Capacity." *Administrative Science Quarterly* 35 (1): 128-152.

Granovetter, Mark S. 1973. "The Strength of Weak Ties." *American
  Journal of Sociology* 78 (6): 1360-1380.

Wenger, Etienne. 1998. *Communities of Practice*. Cambridge:
  Cambridge University Press.

[RFC-0007] Matos, R. "Memory Decay Protocol." RFC 0007, OSC.
[RFC-0016] Matos, R. "Distributed Knowledge Persistence
  Framework." RFC 0016, OSC.

---

## Appendix: RFC Mapping Table

| RFC | Section | Role |
|-----|---------|------|
| 0007 | 3.1, 3.2 | Knowledge decay model |
| 0016 | 3.1, 3.3 | Distributed persistence |

---

## Colophon

> **Colophon**: The Organizational Standards Consortium (OSC) does
> not exist. It is a fictional standards body created for the
> Organizational Epistemology Project (OEP). RFCs, Theorems, and
> Papers published under the OSC imprint are satirical artifacts
> that encode genuine organizational science. All citations of
> real scholars are accurate. The amnesia, however, is real --
> and it is degrading this repository's knowledge at a rate
> the authors cannot precisely measure, which is rather the point.
