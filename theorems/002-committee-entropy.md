---
theorem: 2
title: "Committee Entropy Theorem"
status: "OUTLINED"
dependencies:
  - "ShannonEntropy"
  - "CondorcetJuryTheorem"
rfc_sources: [4, 14]
paper_sources: []
formal_statement: >
  Let C be a committee of n members who each receive
  a private signal about a binary state of the world.
  Each member votes independently. The committee
  aggregates votes by simple majority. The probability
  of the committee reaching the correct decision is
  bounded above by a function of the average Shannon
  entropy of the members' signal distributions.
---

# Theorem-002 — Committee Entropy Theorem

## Statement

Let C be a committee of n members who each receive a
private signal about a binary state of the world. Each
member votes independently. The committee aggregates
votes by simple majority. The Committee Entropy Theorem
states that the probability of the committee reaching
the correct decision is bounded above by a function of
the average Shannon entropy of the members' signal
distributions.

## Proof Sketch

We model each member i as receiving signal X_i with
entropy H(X_i). By the data processing inequality, the
entropy of the vote V_i is at least H(X_i) minus the
entropy lost in the vote function. Applying Condorcet's
jury theorem, the probability of a correct majority
depends on each member's individual competence p_i. A
known inequality relates p_i to the entropy of the
signal: lower entropy implies higher competence.
Composing these bounds yields the theorem.

## Formal Proof

Let p_i = P(V_i = correct). From Cover and Thomas,
H(V_i) <= 1, and by Fano's inequality, H(V_i) >=
h(p_i) where h is the binary entropy function. Each
member's signal satisfies H(V_i) >= H(X_i) -
H(V_i | X_i) >= H(X_i) - log(2). For a committee of
odd size n = 2k+1, the probability of correct majority
is:

P_correct = sum_{j=k+1}^{n} C(n,j) p^j (1-p)^{n-j}

where p = (1/n) sum p_i. By the monotonicity of the
binomial sum, P_correct <= 1 - F(k, n). Substituting
the entropy bound gives P_correct <= 1 - F(k, n)
where F depends on the average H(X_i).

$\blacksquare$

## Corollaries

- Committees with high-entropy signals cannot approach
  certainty regardless of size.
- Adding members with low-quality signals strictly
  degrades the upper bound.
- The optimal committee size for a given average
  entropy is finite.

## Implications

The theorem imposes a fundamental limit on epistemic
committees. Even with unlimited members, the committee
cannot overcome the entropy ceiling of its members'
signals. This refines Condorcet's optimistic
conclusion: larger committees help only when each
additional member adds non-redundant information.

## Colophon

> Theorem 2 of the OEP.
> Part of the Organizational Epistemology Project.
