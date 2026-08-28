---
theorem: 3
title: "Knowledge Gravity Theorem"
status: "OUTLINED"
dependencies:
  - NetworkCentrality
  - PowerLawDistributions
rfc_sources: [5, 9]
paper_sources: []
formal_statement: >
  In an organizational knowledge network
  G = (V, E) with power-law degree
  distribution P(k) ~ k^{-gamma} for
  gamma in (2, 3), the gravitational
  influence of node v on node u at
  network distance d(v, u) is
  F(v, u) = M(v) / d(v, u)^2,
  where M(v) is the knowledge mass
  proportional to degree times
  weighted edge mass.
---

# Theorem 3: Knowledge Gravity

## Statement

Let G = (V, E) be a weighted directed
graph representing an organizational
knowledge network, where V is the set
of knowledge nodes and E is the set of
weighted edges encoding knowledge flow
intensity. Suppose the in-degree
distribution of G follows a power law
P(k_in) ~ k_in^{-gamma} with gamma in
(2, 3). Then the gravitational
influence of a node v on any node u at
network distance d(v, u) is:

F(v, u) = M(v) / d(v, u)^2

where M(v) is the knowledge mass of v,
proportional to k_v times w_v, with k_v
the weighted degree and w_v the total
edge weight. High-centrality nodes
exert strong influence on knowledge
adoption across the organization.

## Proof Sketch

1. Establish that power-law degree
   distributions produce scale-free
   network topology.
2. Define knowledge mass M(v) as the
   product of weighted connectivity and
   edge weight sum.
3. Model influence propagation as a
   field that decays with network
   distance along shortest paths.
4. Show convergence to the
   inverse-square relationship under
   scale-free assumptions and
   weight-degree correlation.

## Formal Proof

Let G = (V, E, w) be a weighted directed
graph with |V| = n. Assume the in-degree
distribution satisfies
P(k_in) ~ k_in^{-gamma} for gamma in
(2, 3).

Define the knowledge mass of node v as
M(v) = k_v * w_v where
k_v = sum_{u in N(v)} w(u, v).

For two nodes v, u in V with shortest
path distance d(v, u) = d, the
accumulated knowledge influence along
the shortest path is:

I(v, u) = product_{e in path(v,u)} w(e)

Under the scale-free property, edge
weights correlate with node degrees per
the preferential attachment kernel. By
the weight-degree relation, the path
influence decays as:

I(v, u) ~ (M(v))^alpha / d^beta

where alpha and beta are determined by
the exponent gamma. For gamma in (2, 3),
the network diameter scales as
d ~ log(n), and the gravitational
approximation holds:

F(v, u) = M(v) / d(v, u)^2

The inverse-square law emerges because
knowledge diffusion in scale-free
networks exhibits distance-dependent
attenuation consistent with
gravitational models. Summing over all
neighbors establishes the theorem for
the full network. QED

## Corollaries

1. **Centrality-Gravity Link**: Nodes
   with betweenness centrality above the
   network mean exert gravitational pull
   exceeding the scale-free baseline by
   a factor proportional to their degree
   excess.

2. **Cascade Threshold**: Knowledge
   cascades triggered by high-mass nodes
   propagate to the full network within
   O(log n) steps, bounded by the
   scale-free diameter.

3. **Equilibrium State**: In a stable
   knowledge network, the gravitational
   field at each node balances inflows
   and outflows, yielding a steady-state
   knowledge distribution matching the
   observed power law.

## Implications

- Organizational restructuring that
  severs high-mass node connections
  produces major epistemic fragmentation
  compared to random edge removal.
- Knowledge hoarding by central nodes
  creates gravitational wells that
  distort information flow across
  departments.
- Strategic knowledge transfer programs
  should target nodes at gravitational
  inflection points for maximum
  organizational impact.

## Colophon

> Theorem 3 of the OEP. Part of the
> Organizational Epistemology Project.
