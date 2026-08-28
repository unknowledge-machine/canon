---
paper: "5"
title: "Epistemic Injustice in Technical
  Decision-Making"
type: "theo"
status: "Draft"
authors:
  - "Rodolfo Matos"
created: "2026-07-18"
updated: "2026-07-19"
keywords:
  - "epistemic-injustice"
  - "decision-making"
  - "code-review"
  - "credibility"
  - "hermeneutics"
rfc_sources: [10]
theorem_sources: []
abstract: |
  This paper develops a theoretical analysis of
  testimonial and hermeneutical injustice in software
  engineering contexts, particularly code review and
  technical architecture decisions. Drawing on
  Miranda Fricker's framework of epistemic injustice
  and mapping it to RFC-0010 (Epistemic Injustice
  Remediation Protocol), we identify systematic
  patterns where engineers from marginalized groups
  receive reduced credibility for technical claims and
  where shared interpretive resources are
  unequally distributed. We propose five propositions
  about how these injustices manifest in technical
  organizations and discuss implications for
  decision quality.
---

# Epistemic Injustice in Technical Decision-Making

## Introduction

Technical decision-making in software organizations
is often presented as meritocratic: the best argument
wins regardless of who makes it. This paper
challenges that assumption by applying Miranda
Fricker's theory of epistemic injustice to code
review processes, architecture discussions, and
technical prioritization meetings.

Fricker identifies two primary forms of epistemic
injustice: testimonial injustice, where a speaker
receives less credibility than they deserve due to
identity prejudice, and hermeneutical injustice, where
a gap in collective interpretive resources renders a
person's experience unintelligible. Both forms operate
in technical organizations with measurable effects on
decision quality.

RFC-0010 (Epistemic Injustice Remediation Protocol)
provides the formal framework within the OEP for
detecting and addressing these patterns. This paper
extends that framework by analyzing how specific
technical practices create conditions for epistemic
injustice.

## Framework: Fricker's Epistemic Concepts

### Testimonial Injustice

Testimonial injustice occurs when a hearer assigns
lower credibility to a speaker's testimony than the
evidence warrants, due to prejudice against the
speaker's social identity. The mechanism operates
through credibility excess and credibility deficit:
some speakers receive unearned trust while others
face unearned skepticism.

In Fricker's analysis, credibility is a resource
distributed by hearers. It is not purely a function
of the speaker's competence but of the hearer's
interpretive dispositions, which are shaped by social
power structures and cultural stereotypes.

### Hermeneutical Injustice

Hermeneutical injustice arises when a gap in shared
interpretive resources prevents a person from making
sense of their own experience. The classic example
is sexual harassment before the term existed: the
experience was real but lacked a conceptual framework
for articulation.

For Fricker, hermeneutical injustice is structural.
It arises not from individual failure but from
unequal participation in meaning-making practices.
Those marginalized from cultural authority have less
influence over which concepts enter the shared
repertoire.

### Credibility Economy

Fricker's concept of the credibility economy describes
how credibility is accumulated, spent, and withdrawn
within social systems. In organizations, credibility
functions as a form of epistemic capital that
influences whose claims are investigated, whose
concerns are taken seriously, and whose interpretations
become authoritative.

## Application to Technical Contexts

### Testimonial Injustice in Code Review

Code review is ostensibly a technical evaluation of
code quality. However, the evaluation is mediated by
the reviewer's perception of the author's competence,
which is influenced by identity markers.

We observe the following patterns in code review
contexts:

1. **Credibility Discounting:** Comments from
   engineers perceived as junior, from non-English-
   speaking backgrounds, or from underrepresented
   groups receive more requests for justification
   than equivalent comments from perceived senior
   engineers. The same technical claim requires more
   evidence when made by some speakers than others.

2. **Authority Asymmetry:** Senior engineers' code
   receives fewer scrutiny rounds, not because their
   code is higher quality but because their credibility
   surplus reduces reviewer vigilance. This creates a
   two-tier evaluation system.

3. **Emotional Labor Penalty:** When engineers from
   marginalized groups advocate for their technical
   positions with the same assertiveness as their
   peers, they are disproportionately coded as
   "difficult" or "not collaborative," incurring a
   credibility cost that their peers do not face.

### Hermeneutical Injustice in Architecture Decisions

Architecture discussions rely on shared vocabulary
and conceptual frameworks. When these frameworks are
developed exclusively within certain communities of
practice, they create interpretive barriers for those
outside those communities.

Specific manifestations include:

1. **Pattern Language Gatekeeping:** Design pattern
   vocabulary originates in specific educational and
   professional contexts. Engineers without access to
   these contexts lack the interpretive resources to
   participate fully in architecture discussions,
   regardless of their technical insight.

2. **Experience Devaluation:** Operational knowledge
   held by engineers who maintain production systems
   often lacks formal conceptual frameworks. When this
   knowledge conflicts with architecturally-derived
   reasoning, it is dismissed as anecdotal rather
   than recognized as a different epistemic modality.

3. **Tool Fluency as Epistemic Capital:** Proficiency
   with specific tools (particular IDEs, frameworks,
   or methodologies) becomes a proxy for technical
   competence, creating hermeneutical gaps for those
   whose expertise lies in different toolchains.

### Decision-Making Inequality

In technical prioritization and roadmap discussions,
epistemic injustice compounds. Engineers who experience
testimonial discounts and hermeneutical gaps contribute
less to strategic technical decisions, not because
their input is absent but because it is systematically
deweighted. This creates feedback loops: less
influence leads to less visibility, which leads to
further credibility erosion.

## Propositions

We advance five propositions derived from this
analysis:

**Proposition 1:** Code review metrics (time to
approval, number of comment rounds, acceptance rate)
contain identity-correlated variance that persists
after controlling for code quality. This variance
constitutes measurable testimonial injustice.

**Proposition 2:** Organizations with higher
technical vocabulary diversity (more frameworks,
paradigms, and toolchains in active use) exhibit
lower hermeneutical inequality, as the interpretive
resource landscape becomes more heterogeneous and
less dominated by a single tradition.

**Proposition 3:** Anonymous code review (where
author identity is hidden) reduces but does not
eliminate testimonial injustice, because linguistic
and stylistic markers continue to trigger credibility
adjustments.

**Proposition 4:** The effectiveness of epistemic
injustice remediation (as specified in RFC-0010)
depends on the organizational willingness to treat
credibility distribution as a measurable resource
rather than a natural reflection of competence.

**Proposition 5:** Technical decision quality is
inversely correlated with epistemic inequality.
Organizations that concentrate credibility among
fewer participants make systematically worse
technical decisions because they exclude information
that disfavored speakers possess.

## Conclusion

Epistemic injustice is not an aberration in technical
organizations but a structural feature of how
credibility and interpretive resources are distributed.
Treating technical decision-making as identity-neutral
obscures the mechanisms that produce unequal
participation and degraded decision quality.

RFC-0010 provides a remediation framework, but
remediation requires first acknowledging the problem.
This paper argues that software engineering
organizations must develop the institutional capacity
to recognize testimonial and hermeneutical injustice
in their technical practices, measure its extent, and
design interventions that address structural causes
rather than individual behavior.

The cost of epistemic injustice is not only ethical
but epistemic: organizations that systematically
devalue certain voices make worse decisions because
they narrower the information base on which decisions
rest.

## Colophon

This paper was drafted as part of the Organizational
Epistemology Project's paper series. It applies
Fricker's epistemic injustice framework (2007) to
software engineering contexts as an extension of
RFC-0010's remediation protocol.

The theoretical analysis draws on philosophy of
epistemology, science and technology studies, and
empirical observations from software engineering
practice. The propositions outlined here are intended
to motivate empirical investigation.

This is a DRAFT document. Comments and corrections
should be directed to the OEP repository.
