---
paper: "10"
title: "Toward a Formal Theory of Organizational Epistemology"
type: "theo"
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
  - formal-theory
  - organizational-epistemology
  - knowledge-graphs
  - axioms
  - synthesis
abstract: |
  This paper proposes a formal theory of organizational epistemology
  synthesizing the OEP RFC series and theorem corpus. We construct
  six definitions, four axioms, and three propositions modeling
  organizational knowledge as a directed graph. The framework
  formalizes knowledge gravity, epistemic fragmentation, committee
  entropy, and the coffee machine theorem.
rfc_sources: [1, 2, 3, 4, 5, 6, 7, 9, 10, 17]
theorem_sources: [2, 3]
---

# Toward a Formal Theory of Organizational Epistemology

## 1. Introduction

Organizational epistemology asks how organizations know what they
know, and what happens when that knowledge is wrong, absent, or
trapped. The OEP has produced RFCs documenting organizational
pathologies -- from the Hierarchical Omniscience Protocol (RFC-0001)
to the Coffee-Break Protocol (RFC-0017) -- and theorems formalizing
phenomena such as the Coffee Machine Theorem (Theorem-001) and
Committee Entropy (Theorem-002). This paper proposes six definitions,
four axioms, and three propositions unifying these findings.

## 2. Foundations

### 2.1 From the RFC Series

**RFC-0001** establishes that authority does not confer knowledge.
**RFC-0002** documents systems mirroring communication structures.
**RFC-0003** defines epistemic fragmentation -- divergence between
formal representations and operational reality. **RFC-0004** describes
performative decision-making. **RFC-0005** observes knowledge
accumulating around power centers. **RFC-0006** documents gaps between
espoused and enacted strategy. **RFC-0007** models knowledge as a
decaying cache. **RFC-0009** examines deliberate knowledge
withholding. **RFC-0010** addresses systematic marginalization of
certain knowers. **RFC-0017** demonstrates that informal networks
carry higher bandwidth than formal channels.

### 2.2 From the Theorem Corpus

**Theorem-001** proves informal network bandwidth exceeds formal
channel bandwidth under fragmentation. **Theorem-002** proves
decision-quality entropy increases superlinearly with committee
size. **Theorem-003** establishes limits on tacit knowledge transfer
through formal channels.

### 2.3 Prior Work

Simon (1947) established bounded rationality. Nonaka and Takeuchi
(1995) developed the SECI model. Wenger (1998) built communities of
practice theory. Our contribution formalizes these traditions and
connects them to OEP phenomena.

## 3. Formal Framework

### 3.1 Definitions

**Definition 1 (Knowledge State).** Let $O$ have knowledge state
$K(O,t) \subset E \times E$ at time $t$, where $E$ is the set of
actors. Each edge $(e_i, e_j)$ carries weight $w_{ij}(t) \in [0,1]$.

**Definition 2 (Formal Knowledge Graph).** $G_F = (V, E_F, w_F)$
represents knowledge through official channels.

**Definition 3 (Informal Knowledge Graph).** $G_I = (V, E_I, w_I)$
represents knowledge through unofficial channels.

**Definition 4 (Epistemic Fragmentation).**

    EF(O,t) = 1 - |K_actual intersect K_formal| / |K_actual|

**Definition 5 (Knowledge Capacity).** $C(O)$ is the maximum rate of
novel, non-redundant information transmission across $G_F \cup G_I$.

**Definition 6 (Amnesia Rate).**

    A(O,t) = d|K|/dt|_deletion - d|K|/dt|_refresh

### 3.2 Axioms

**Axiom 1 (Dual-Channel Flow).** For $|E| > 1$, knowledge flows
through both $G_F$ and $G_I$ with $G_F \cap G_I = \emptyset$.

**Axiom 2 (Knowledge Gravity).**

    dw_{ij}/dt proportional to authority(j) x w_{ij}

**Axiom 3 (Bounded Rationality).** Each actor maintains
$|N(i)| \leq B$ (Simon 1947).

**Axiom 4 (Informal Bandwidth Superiority).** When $EF > 0$:

    C(G_I)/|E_I| > C(G_F)/|E_F|

### 3.3 Propositions

**Proposition 1 (Fragmentation-Bounded Flow).** When $EF(O,t) > 0$:

    C(O) <= max(C(G_F), C(G_I)) + EF(O,t) x C(G_I)

*Proof.* By Axiom 1, two independent channels. By Axiom 4, the
informal channel carries overflow when $EF > 0$. QED.

**Proposition 2 (Optimal Committee Size).**

    Q(n) = Q(1) x exp(-alpha x n^2 / 2)

for $n > \sqrt{2/\alpha}$. *Proof.* Direct from Theorem-002. QED.

**Proposition 3 (Amnesia Recovery Threshold).**

    refresh_rate >= turnover_rate x (1 - doc_coverage)

*Proof.* From Definition 6, setting $A(O,t) = 0$. QED.

### 3.4 Implications

- Proposition 1 formalizes why RFC-0017's informal networks are
  essential under fragmentation
- Proposition 2 provides the basis for Theorem-002's committee
  sizing recommendation
- Proposition 3 connects Paper-009's Amnesia Risk Index to the
  formal framework

## 4. Research Agenda

**Problem 1 (Dynamics).** What differential equations govern the
evolution of $G_F$ and $G_I$ under restructuring and turnover?

**Problem 2 (Phase Transitions).** Do knowledge graphs exhibit
sudden fragmentation at critical $EF$ values?

**Problem 3 (Optimal Intervention).** What intervention sequence
minimizes knowledge loss at minimum cost?

**Problem 4 (Cross-Organization).** How do knowledge graphs interact
across organizational boundaries?

**Problem 5 (Tractability).** For $|E| > 1000$, can the framework
be approximated efficiently?

## 5. Conclusion

We proposed a formal theory of organizational epistemology: six
definitions, four axioms, three propositions. The framework unifies
the OEP's RFC series and theorem corpus, demonstrating that
hierarchical omniscience, epistemic fragmentation, knowledge gravity,
committee entropy, and the coffee machine effect are consequences of
a small number of axioms. Four axioms generate three propositions
explaining why organizations know what they know, why they forget,
and why the coffee machine outperforms the meeting room.

---

## References

Cohen, W.M. and D.A. Levinthal. 1990. "Absorptive Capacity."
  *ASQ* 35(1): 128-152. Granovetter, M.S. 1973. "The Strength
  of Weak Ties." *AJS* 78(6): 1360-1380. Nonaka, I. and H.
  Takeuchi. 1995. *The Knowledge-Creating Company*. Oxford UP.
  Simon, H.A. 1947. *Administrative Behavior*. Macmillan.
  Wenger, E. 1998. *Communities of Practice*. Cambridge UP.

[RFC-0001] https://rfc.osc.org/rfc0001. [RFC-0002]
  https://rfc.osc.org/rfc0002. [RFC-0003]
  https://rfc.osc.org/rfc0003. [RFC-0004]
  https://rfc.osc.org/rfc0004. [RFC-0005]
  https://rfc.osc.org/rfc0005. [RFC-0006]
  https://rfc.osc.org/rfc0006. [RFC-0007]
  https://rfc.osc.org/rfc0007. [RFC-0009]
  https://rfc.osc.org/rfc0009. [RFC-0010]
  https://rfc.osc.org/rfc0010. [RFC-0017]
  https://rfc.osc.org/rfc0017. [Theorem-001]
  https://theorem.osc.org/t001. [Theorem-002]
  https://theorem.osc.org/t002. [Theorem-003]
  https://theorem.osc.org/t003.

---

## Appendix: Source Mapping

| Source | Section | Role |
|--------|---------|------|
| RFC-0001 | 2.1, 3.1 | Positioned vs actual knowledge |
| RFC-0002 | 2.1 | Graph topology link |
| RFC-0003 | 2.1, 3.1 | Epistemic fragmentation |
| RFC-0004 | 2.1 | Decision process vs outcome |
| RFC-0005 | 2.1, 3.2 | Knowledge gravity axiom |
| RFC-0006 | 2.1 | Epistemic distance |
| RFC-0007 | 2.1, 3.3 | Temporal decay model |
| RFC-0009 | 2.1 | Epistemic opacity |
| RFC-0010 | 2.1 | Credence distribution |
| RFC-0017 | 2.1, 3.2 | Informal bandwidth axiom |
| Theorem-001 | 2.2, 3.2 | Grounds Axiom 4 |
| Theorem-002 | 2.2, 3.3 | Grounds Prop 2 |
| Theorem-003 | 2.2 | Tacit transfer limits |

---

## Colophon

> **Colophon**: The Organizational Standards Consortium (OSC) does
> not exist. It is a fictional standards body created for the
> Organizational Epistemology Project (OEP). RFCs, Theorems, and
> Papers published under the OSC imprint are satirical artifacts
> that encode genuine organizational science. All citations of
> real scholars are accurate. The formal theory, however, is
> real -- and it demonstrates that the most effective
> organizational knowledge infrastructure costs approximately
> one espresso per synchronization event.
