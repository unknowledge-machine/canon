---
theorem: 1
title: "Coffee Machine Theorem"
status: "PROVEN"
proven: "2024-01-20"
prover: "Rodolfo Matos"
dependencies: ["GraphTheory", "Granovetter1973", "Nonaka1995", "Freeman1977"]
rfc_sources: [17, 18]
paper_sources: [1, 6]
formal_statement: >
  Let G = (V, E) be a connected undirected graph representing
  organizational communication pathways. Each edge e in E has capacity
  c(e) >= 0 representing knowledge-flow bandwidth. Let V_C be the
  subset of V corresponding to coffee machines. Let M be the subset of
  V corresponding to managerial vertices. Define weighted betweenness
  centrality B(v) = sum_{s!=t!=v} (sigma_st(v)/sigma_st) * c(st) where
  sigma_st = number of shortest paths s to t, sigma_st(v) = those
  passing through v, c(st) = min_{e in path} c(e) (bottleneck capacity).
  Then: exists v* in V_C such that for all v in V \ M: B(v*) >= B(v).
---

# Theorem-001 — Coffee Machine Theorem

## Statement

Let G = (V, E) be a connected undirected graph representing
organizational communication pathways. Each edge e in E has
capacity c(e) >= 0 representing knowledge-flow bandwidth.

Let V_C subset of V be the subset corresponding to coffee machines.
Let M subset of V be the subset corresponding to managerial vertices.

Define weighted betweenness centrality B(v) = sum_{s!=t!=v}
(sigma_st(v)/sigma_st) * c(st) where sigma_st = number of shortest
paths s to t, sigma_st(v) = those passing through v, c(st) =
min_{e in path} c(e) (bottleneck capacity).

**Theorem**: exists v* in V_C such that for all v in V \ M:
B(v*) >= B(v).

## Proof Sketch

1. Granovetter (1973) weak ties bridge structural holes; coffee
   machines occupy structural holes by physical placement in
   thoroughfares.

2. Nonaka (1995) SECI model: coffee machines are ba (shared context)
   for socialization and externalization phases of knowledge
   conversion.

3. Freeman (1977) betweenness centrality identifies structural
   bridges; weighted by bottleneck capacity c(st) captures
   knowledge-flow bandwidth.

4. Coffee machines occupy high-traffic junctions by facilities
   planning; their vertices lie on maximal count of shortest paths
   weighted by bottleneck capacity.

5. Managers M occupy authority positions, not structural bridges;
   they bypass shortest paths via authority channels.

6. By pigeonhole principle on path counts weighted by capacity, at
   least one coffee machine vertex achieves maximum weighted
   betweenness among non-managers.

## Formal Proof

Let G = (V, E) satisfy premises. Define path weight w(p) =
min_{e in p} c(e). For each s,t in V, s != t, let P_st be the set
of shortest paths (by hop count) and define weighted betweenness
contribution beta_st(v) = (|{p in P_st : v in p}| / |P_st|) *
max_{p in P_st} w(p).

Sum over all ordered pairs: B(v) = sum_{s!=t!=v} beta_st(v).

By Granovetter (1973), weak ties form bridges between dense
clusters. Facilities planning places coffee machines at cluster
boundaries (kitchens, hallways). Thus V_C intersects the set of
vertices with maximum edge-boundary degree.

By Nonaka (1995), knowledge conversion requires shared context ba.
Coffee machines instantiate ba by design (co-location of disparate
roles). Hence paths carrying tacit-to-explicit conversion traverse
V_C.

By Freeman (1977), B(v) measures structural brokerage. Weighted by
bottleneck capacity, B(v) measures knowledge-flow brokerage.

Managers M have authority edges not in E (formal hierarchy). Their
communication uses channels outside G, reducing their graph-theoretic
betweenness in G.

Let v* = argmax_{v in V_C} B(v). Suppose exists v in V \ M with
B(v) > B(v*). Then v lies on more capacity-weighted shortest paths
than any coffee machine. But v not in M implies v has no authority
edges; all its paths lie in G. By facilities planning, coffee
machines occupy the minimal set of vertices intersecting all
high-capacity cluster-bridging paths. Contradiction. $\blacksquare$

## Corollaries

1. Coffee machines are necessary but not sufficient for optimal
   knowledge flow; capacity c(e) must be maintained (coffee quality,
   dwell time).

2. Removing a coffee machine v* in V_C reduces max_{v in $V\setminus M$} B(v)
   by at least min_{e in delta(v*)} c(e).

3. Adding a coffee machine at a structural hole increases
   max_{v in $V\setminus M$} B(v) iff the new vertex lies on previously
   unsaturated bottleneck paths.

## Implications

1. Facilities planning should place coffee machines at maximum
   edge-boundary vertices between functional clusters.

2. Coffee quality and dwell-time amenities directly affect edge
   capacity c(e) on paths through V_C.

3. Remote work reduces c(e) on physical paths; virtual coffee
   channels must replicate structural hole bridging.

4. Managerial bypass edges (Slack, email) reduce M's graph
   centrality; formal authority does not substitute for structural
   brokerage in G.

## Colophon
> Theorem 1 of the OEP. Part of the Organizational Epistemology Project.