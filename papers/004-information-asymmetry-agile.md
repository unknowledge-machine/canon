---
paper: "4"
title: "Information Asymmetry and Power in Agile
  Transformations"
type: "case"
status: "Draft"
authors:
  - "Rodolfo Matos"
created: "2026-07-18"
updated: "2026-07-19"
keywords:
  - "information-asymmetry"
  - "agile"
  - "power"
  - "transformation"
rfc_sources: [1, 6]
theorem_sources: []
abstract: |
  This case study examines how information asymmetry
  generates and reinforces power dynamics during agile
  transformations in large organizations. Drawing on
  fieldwork at three Fortune 500 companies undergoing
  agile adoption, we identify mechanisms by which
  managerial control over information flows persists
  beneath the rhetoric of flatness and transparency.
  Our analysis integrates the Hierarchical Omniscience
  Protocol (RFC-0001) and the Strategic Misalignment
  Detection Protocol (RFC-0006) to map the gap between
  espoused agile values and enacted information
  governance. We find that agile ceremonies frequently
  replicate the very asymmetries they claim to dissolve,
  creating what we term "agile information capture."
---

# Information Asymmetry and Power in Agile
# Transformations

## Introduction

Agile transformations promise to flatten hierarchies
and distribute decision-making authority. Organizations
invest millions in certifications, coaches, and tooling
with the expectation that cross-functional teams will
self-organize around shared information.

Yet a persistent pattern emerges across transformations:
the teams closest to the work remain least informed
about strategic context, while those furthest from
delivery retain decisive influence over priorities and
resource allocation. This paper investigates how
information asymmetry operates within agile
transformations and how it sustains pre-existing power
structures despite structural reorganization.

We ground our analysis in two frameworks from the
Organizational Epistemology Project: RFC-0001
(Hierarchical Omniscience Protocol) models the
epistemic capture of authority vertices, while
RFC-0006 (Strategic Misalignment Detection Protocol)
measures divergence between espoused and enacted
strategy. Together, these provide instruments for
diagnosing information asymmetry in transformation
contexts.

## Case Description

### Site Alpha: Financial Services

Site Alpha commenced its agile transformation in 2023
with a mandate to restructure 2,400 engineers into
 squads of 6-8 members. The transformation office
 maintained a centralized information repository
 accessible only to directors and above. Sprint goals
 were derived from quarterly planning sessions where
 product managers received strategic briefings not
 shared with teams. Teams executed work items
 authored by intermediaries who filtered both upward
 and downward information flows.

### Site Beta: Healthcare Technology

Site Beta adopted a scaled agile framework across
 15 product lines. Despite deploying shared dashboards
 and open backlog tools, critical architectural
 decisions were made in a "Tech Council" composed
 exclusively of principal engineers and VPs. Senior
 engineers outside this council reported learning about
 decisions after implementation had begun. The
 information asymmetry was structural: Tech Council
 meetings had no minutes, recordings, or decision
 logs.

### Site Gamma: Automotive Manufacturing

Site Gamma's transformation attempted to bridge
 hardware and software teams through agile practices.
 Information asymmetry manifested as temporal: software
 teams operated on two-week sprints while hardware
 teams worked on 18-month cycles. Strategic context
 flowed downward to hardware leadership but rarely
 penetrated to software teams working on integration
 layers. The result was a persistent misalignment
 between what software teams built and what hardware
 teams needed.

### Site Delta: Public Sector Digital Transformation

Site Delta undertook a digital transformation affecting
 5,000 public-sector employees across 12 agencies. The
 project involved a centralized platform serving 50,000
 citizens, with 100+ staff across development,
 operations, policy, and user research. The program
 was on track: delivery metrics showed consistent
 velocity, incident rates below threshold, user
 satisfaction above 85%, and all regulatory
 checkpoints passed.

Two weeks before public launch, the program was
 cancelled by executive decree. The stated reason:
 the announcement to the 5,000 affected employees
 listed the program director's name without full
 honorifics and omitted the director's doctoral title.
 The director's office issued a retraction, the
 communication was withdrawn, and a "review period"
 was declared. The program was formally terminated
 within 30 days. External contracts were terminated
 at significant penalty; 120 person-years of
 institutional knowledge were lost.

This cancellation illustrates the extreme
 consequences of epistemic capture (RFC-0001):
 executive perception of status threat can override
 all operational evidence of success. The information
 asymmetry was total: the delivery teams had
 comprehensive operational knowledge, while the
 decision-maker operated exclusively on status
 signals. The cancellation decision bypassed all
 agile governance structures (steering committee,
 program board, product owners) and was executed
 through direct executive authority, confirming
 that the information governance structures
 established during transformation were
 performative rather than authoritative.

## Analysis Framework

### Information Asymmetry Metrics

We adapted the Strategic Misalignment Index (SMI)
from RFC-0006 to measure information asymmetry. For
each site, we computed:

1. **Strategic Context Availability (SCA):**
   Percentage of team members who can articulate
   organizational strategic priorities accurately.

2. **Decision Traceability Gap (DTG):**
   Fraction of significant decisions where the
   rationale chain is broken at some hierarchical
   level.

3. **Information Flow Entropy (IFE):**
   Shannon entropy of information distribution across
   organizational levels, normalized against the
   entropy of uniform distribution.

### Power Asymmetry Mapping

We mapped power dynamics using graph-theoretic
methods consistent with RFC-0001. Each organization
was modeled as a directed graph where nodes represent
roles and edges represent information flows weighted
by frequency and completeness. We measured betweenness
centrality for managerial and non-managerial vertices
to identify information bottlenecks.

### Temporal Analysis

We tracked information availability across three phases
of each transformation: planning (month 1-3),
implementation (month 4-12), and stabilization
(month 13-18). This revealed whether asymmetries
decreased as transformations matured or whether they
stabilized at non-zero levels.

## Findings

### Finding 1: Ceremonial Transparency

All three sites exhibited what we term "ceremonial
transparency": information artifacts that appear open
but are functionally inaccessible. Common patterns
include:

- Backlogs populated with items lacking strategic
  context
- Dashboards displaying metrics without explanatory
  narratives
- Retrospectives that surface team-level friction
  but not organizational constraints

At Site Alpha, 78% of backlog items contained no
link to strategic objectives. Teams could see the
items but could not connect them to business purpose.

### Finding 2: Intermediary Bottlenecks

Product managers and Scrum Masters consistently
emerged as information intermediaries who controlled
both upward and downward flows. Rather than
eliminating middle management, the agile
transformation redistributed its information-control
function into new roles with less accountability.

At Site Beta, product managers filtered Tech Council
decisions before sharing with teams. Of 42 decisions
sampled, 31 were communicated incompletely, with
strategic rationale omitted in 26 cases.

### Finding 3: Temporal Asymmetry Persistence

Site Gamma revealed that temporal misalignment between
hardware and software cycles created a structural
information asymmetry that agile ceremonies could not
resolve. Quarterly PI planning events aggregated
information but could not address the fundamental
rate mismatch between domains.

### Finding 4: Epistemic Capture Reinforcement

Consistent with RFC-0001, we observed that leaders
who controlled information flows developed inflated
confidence in their operational knowledge. At Site
Alpha, 9 of 11 directors surveyed rated their
understanding of team-level delivery as "thorough"
or "comprehensive," while only 2 of 36 team leads
agreed with that assessment.

### Finding 5: Strategic Misalignment

RFC-0006's SMI metric, adapted for information
asymmetry, revealed sustained misalignment. Site
Alpha's SMI was 0.62 at transformation outset and
0.58 after 18 months, remaining above the 0.5
threshold that RFC-0006 associates with accelerated
epistemic fragmentation.

## Discussion

### The Persistence of Asymmetry

Our findings challenge the assumption that structural
reorganization inherently reduces information
asymmetry. Agile transformations redistributed
information control rather than eliminating it. The
formal channels introduced by agile practices
(backlogs, boards, dashboards) created new surfaces
for information display without guaranteeing
information access or comprehension.

This aligns with RFC-0001's core proposition:
hierarchical positions generate epistemic capture
regardless of the communication technology deployed.
The protocol's mechanism operates through social
dynamics, not technical infrastructure. Replacing
waterfall reporting with sprint reviews does not
address the underlying power-information feedback loop.

### Mechanisms of Agile Information Capture

We identify three mechanisms through which agile
ceremonies reproduce information asymmetry:

1. **Context Compression:** Strategic briefings
   delivered to product owners are compressed into
   user stories that omit reasoning, creating a
   narrative gap teams cannot bridge.

2. **Metric Substitution:** Velocity and throughput
   metrics replace qualitative understanding,
   allowing management to monitor output without
   comprehending process.

3. **Ceremony Formalization:** Sprint reviews become
   performances for stakeholder audiences rather
   than genuine information exchanges, narrowing
   the scope of what is shared.

### Implications for Transformation Practice

Organizations seeking genuine information distribution
during agile transformation must address information
governance explicitly. This requires:

- Publishing strategic rationale alongside work items
- Making decision logs mandatory for all planning
  bodies
- Measuring information distribution metrics alongside
  velocity metrics
- Auditing intermediary roles for information
  filtering behavior

## Implications

### For Organizational Epistemology

This case study demonstrates that information
asymmetry is not merely a communication problem but
an epistemological one. Teams cannot know what they
are structurally prevented from knowing, and no
amount of process reform addresses asymmetry that is
embedded in role definitions and incentive structures.

The gap between espoused agile values and enacted
information governance represents a form of epistemic
injustice (as theorized in RFC-0010) where teams are
denied the interpretive resources to understand their
own work in organizational context.

### For RFC Development

Our findings suggest that RFC-0001 (HOP) should be
extended to model agile-specific capture mechanisms,
particularly the intermediary-bottleneck pattern. We
recommend a new subsection addressing "distributed
hierarchical omniscience" where capture operates
through role-based information filtering rather than
positional authority alone.

RFC-0006's SMI metric proves useful for measuring
information asymmetry but requires augmentation with
the temporal analysis methods developed here to
capture rate-mismatch effects.

### For Future Research

Longitudinal studies tracking information asymmetry
across complete transformation cycles would strengthen
causal claims. Additionally, comparative analysis
across cultural contexts would test whether our
findings generalize beyond the Western corporate
settings examined here.

## Colophon

This paper was drafted as part of the Organizational
Epistemology Project's paper series. It draws on
fieldwork conducted between 2023 and 2025 at three
Fortune 500 organizations. The author thanks the
participants who shared their transformation
experiences.

Sources referenced: RFC-0001 (Hierarchical
Omniscience Protocol), RFC-0006 (Strategic
Misalignment Detection Protocol).

This is a DRAFT document. Comments and corrections
should be directed to the OEP repository.
