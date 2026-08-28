---
rfc: "0035"
title: "Executive Stealth Protocol (ESP)"
stream: "Experimental"
status: "DRAFT"
category: "Informational"
area: "informal-networks"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
created: "2026-08-06"
updated: "2026-08-06"
obsoletes: []
obsoleted_by: []
see_also: [17, 1, 5, 21]
keywords:
  - stealth
  - weak-ties
  - listen-only
  - coffee-break-protocol
  - non-capture
  - executive-behavior
abstract: |
  This document specifies the Executive Stealth Protocol (ESP), a behavior
  protocol for executives whose epistemic capture distorts the knowledge
  they receive. ESP prescribes three behaviors: (a) cultivating weak ties
  outside the chain of command (Granovetter 1973; Rajkumar et al. 2022);
  (b) attending Coffee-Break Protocol (RFC-0017) sessions in Listen-Only
  mode, referencing the Listen-Only CHP already defined in RFC-0017 §3.2;
  and (c) identifying informal connectors by observing without formalizing,
  subject to the Non-Capture Principle. ESP is voluntary by construction:
  it encourages behavior, it never mandates attendance, and listening is
  not collection.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0035 — Executive Stealth Protocol (ESP)

## Abstract

This document specifies the Executive Stealth Protocol (ESP), a behavior
protocol for executives whose epistemic capture distorts the knowledge
they receive. ESP prescribes three behaviors: (a) cultivating weak ties
outside the chain of command (Granovetter 1973; Rajkumar et al. 2022);
(b) attending Coffee-Break Protocol (RFC-0017) sessions in Listen-Only
mode, referencing the Listen-Only CHP already defined in RFC-0017 §3.2;
and (c) identifying informal connectors by observing without formalizing,
subject to the Non-Capture Principle. ESP is voluntary by construction:
it encourages behavior, it never mandates attendance, and listening is
not collection.

> **Dual-Layer Notice**: This RFC presents the Executive Stealth Protocol
> as a satirical vehicle for peer-reviewed findings on weak ties and
> psychological safety. The serious layer is behavioral: leaders who stop
> publishing and start listening learn more. The satirical layer is the
> ritualization: the protocol reads like an espionage manual because, in
> power-dominant organizations, learning quietly is treated as a covert
> operation.

## Status

DRAFT — Submitted for Editorial, Technical, and Canon review.

## 1. Introduction

### 1.1 Problem Statement

Executives in power-dominant organizations (RFC-0001) receive filtered,
upward-distorted knowledge. The Knowledge Gravity Index (KGI, RFC-0005)
quantifies this distortion. Traditional remediation — measuring the
distortion more often and publishing the numbers — fails because the
measurement apparatus is itself captured: metrics computed by the
hierarchy are gamed by the hierarchy (Theorem-001 cross-check).

The failure is structural, not informational. Executives do not lack
data. They lack a channel that the hierarchy does not control.

### 1.2 Scope

ESP is a Layer-A behavioral protocol for executives. It specifies what
an executive does, not what an organization mandates. ESP does not
create new metrics, new committees, or new reporting lines. Where a
metric or mechanism is referenced, it already exists (RFC-0017 §3.2).

## 2. Terminology

| Term | Definition |
|------|------------|
| **ESP** | Executive Stealth Protocol, this document. |
| **Listen-Only CHP** | Existing CBP variant defined in RFC-0017 §3.2 and RFC-0001 §5.3 (Requirement 15): the participant observes without initiating handshakes, and does not speak or identify as management. |
| **Weak Tie** | A low-strength, low-frequency relationship bridging otherwise disconnected clusters (Granovetter 1973). |
| **Informal Connector** | A vertex whose knowledge and structural reach — not whose connection count — make it a channel for truth; a *truth vertex* with structural reach. |
| **Non-Capture Principle** | Any mechanism that converts informal connections into formal reporting lines destroys their capacity to carry candid knowledge (Theorem-001). ESP-compliant executives *observe* connectors; they do not *manage* them. |
| **Truth Vertex** | A vertex that knows how the organization works in practice, distinct from a power vertex that only appears central (RFC-0005). |

## 3. Protocol Specification

ESP consists of three behaviors. Compliance is measured by the executive's
own practice, not by organizational surveillance.

### 3.1 Weak-Tie Cultivation

**Behavior**: The executive maintains ties outside their chain of command —
peers in other functions, operational staff two or more levels down, and
counterparts in other organizations.

**Rationale**: Weak ties transmit novel information precisely because they
are not embedded in the dense, redundant communication cluster of the
executive's own team (Granovetter 1973). Experimental evidence shows that
random interactions with relative strangers produce novel information
(Rajkumar et al. 2022).

**Rule ESP-1**: An executive SHALL maintain weak ties whose combined span
covers at least one operational cluster outside the executive's reporting
line.

**Rule ESP-2**: An executive SHALL NOT convert a weak tie into a reporting
line. Conversion destroys the tie's capacity (Non-Capture Principle).

### 3.2 Listen-Only Attendance

**Behavior**: The executive attends CBP sessions (RFC-0017) in Listen-Only
mode as already defined in RFC-0017 §3.2 and RFC-0001 §5.3 (Requirement
15). ESP references this mode; it does not create it.

**Rationale**: Listen-Only CHP permits ECI reduction through passive
synchronization without collapsing psychological safety (Edmondson 1999;
RFC-0001 §4.1). The executive's silence is the point: the channel closes
the moment management is detected.

**Rule ESP-3**: The executive SHALL NOT speak, ask questions, or identify
as management during Listen-Only attendance.

**Rule ESP-4**: Attendance is voluntary. ESP MUST NOT be used to mandate
CBP participation. Mandated attendance destroys the psychological safety
the protocol depends on.

### 3.3 Connector Identification Without Capture

**Behavior**: The executive identifies informal connectors by observing
who is consulted, who is deferred to, and who appears in the operational
narratives of others — then leaves the observation result on paper. The
executive does not formalize, does not reward, does not "recognize" the
connector into a role.

**Discriminator (anti-Project-Atlas)**: The relevant connector is NOT the
vertex with the most connections. Connection count is a power metric, not
a knowledge metric: the most-connected vertices are power vertices
(Chapter 10, Project Atlas error). The relevant connector is a *truth
vertex with structural reach* — one whose knowledge is verified by
operational outcomes and whose position bridges otherwise disconnected
clusters. Identification proceeds from what people know and who asks
them, not from network diagrams.

**Rule ESP-5**: The executive SHALL identify connectors by knowledge and
structural reach, never by connection count alone.

**Rule ESP-6**: The executive SHALL NOT formalize the connector role.
Rewarding a connector into a position removes them from the informal
network that made them useful (Non-Capture Principle).

Rule ESP-6 forbids formalizing the connector *role* — title, position,
reporting line, badge. It does not forbid — and the executive SHALL
ensure — that the connector's value is compensated fairly. Non-Capture
governs the role, not the wallet: a connector paid for the value they
create remains a connector; a connector converted into a position is a
connector lost. Compensation follows the Technical Career Track
(Appendix C; Rule ESP-7), never promotion into management.

**Rule ESP-7**: The executive SHALL ensure that connectors receive the
Technical Career Track — TEC-based compensation reflecting the cost of
their departure (RFC-0016 §3.3), status through the Knowledge Steward
title (RFC-0009 §3.3), technical sovereignty including architectural
veto, recognition through peer-nominated channels, and protected
unmonitored time — instead of promotion into management (Ahmed's
Paradox, Appendix C).

#### 3.3.1 Connector Archetypes (Observation Aid)

Observation distinguishes three recurring shapes of informal connector
(Arena, Cross, Sims, & Uhl-Bien 2017). They are observation categories, not
job titles: an institution that converts them into titles has already
violated Rule ESP-6.

| Archetype | Network Signature | Observation Cues | Capture Failure |
|-----------|-------------------|------------------|-----------------|
| **Broker** | Ties that bridge otherwise disconnected clusters | Consulted by people in different teams who do not talk to one another; appears in the operational narratives of multiple, mutually disconnected clusters | Promoted into a coordination role; leaves the informal network; channel closes |
| **Central Connector** | High-quality ties within one dense cluster | Others say "ask them"; deferred to on how work is done inside the cluster | Named "knowledge owner"; becomes a reporting line; colleagues route around them |
| **Energizer** | Position-independent; may appear anywhere in the network | Projects form around them; others volunteer to work with them; their half-formed ideas become whole in others' hands | "Recognized" with an award or title; the energy becomes a performance. Overloaded with more work "because they get things done" (Competence Tax: the productive are burdened with the load of the less productive until they burn out); the energy dies from overuse |

The anti-Project-Atlas discriminator (Rule ESP-5) applies to all three: none
is identified by connection count. The Broker is identified by structural
reach across clusters; the Central Connector by deferral within a cluster;
the Energizer by outcomes in the operational narratives of others.

#### 3.3.2 Case Study: The Half-Day (Composite)

A fictional institution permits every employee to spend one half-day per week
on a project the employee believes is useful — or that the employee believes
must be done — provided they do not do it alone. There is no approval
committee, no portfolio dashboard, and no reporting line for the projects.
The only rule is the pairing rule: work with someone.

An ESP-compliant executive attends the resulting venues in Listen-Only mode.
Over time the executive observes a Broker who consistently assembles people
from three functions that otherwise never meet; a Central Connector who
becomes the person others name first when a half-day project gets stuck; an
Energizer whose pitch for fixing the broken cache pulled volunteers from
outside their own team. The executive writes none of this down as an
assessment, promotes nobody, and awards no title. The institution, for its
part, does not track the half-days. The knowledge flows; the channel stays
open; the connectors stay where they are.

The pairing rule is the point, and it is a weak-tie generator only because it
is not prescriptive: employees choose whom to pair with. An institution that
specifies the pairs converts the half-day into an assigned collaboration,
which is a formal channel by another name and closes the space (Non-Capture
Principle).

## 4. Relationship to Other RFCs

- **RFC-0017 (CBP)**: ESP Layer-A behavior depends on the Listen-Only CHP
  defined in RFC-0017 §3.2. ESP adds executive behavior; it does not amend
  the protocol.
- **RFC-0001 (HOP)**: ESP operationalizes Requirement 15 (ECI ≥ 10
  listen-only attendance) as voluntary executive practice. ESP aligns with
  the threshold as stated in RFC-0001 §5.3.
- **RFC-0005 (KGMF)**: The connector discriminator (Rule ESP-5) uses the
  knowledge-gravity distinction between power vertices and truth vertices.
- **RFC-0021 (NDD)**: The Non-Capture Principle in ESP extends the
  informal-network protections of the newsletter-driven channel.

ESP supersedes no other RFC. It does not claim to close any open finding;
it implements behavior consistent with findings already documented in the
RFCs above.

## 5. Security Considerations

### 5.1 Surveillance Misuse

An organization that deploys ESP as a surveillance mechanism — monitoring
which executives attend which sessions, mapping connectors for
intervention — violates the Non-Capture Principle and the voluntary basis
of ESP. Such deployment is anti-therapeutic and SHALL be rejected.

### 5.2 Masked Attendance

An executive may attend Listen-Only sessions and still leak management
status through posture, entourage, or interruption patterns. ESP does not
detect this; it is a behavior protocol, not a monitoring protocol.

### 5.3 Listening Is Not Collection

ESP treats listening as learning, not as intelligence gathering. Any use
of Listen-Only attendance to collect information for later punitive action
is a violation of Rule ESP-3 in spirit and degrades the shared channel.

## 6. Operational Considerations

### 6.1 Deployment

ESP requires no organizational infrastructure. The executive requires:
- access to a CBP session (existing RFC-0017 venue)
- permission to attend without management identification
- protected time (RFC-0001 §4.1 Model 3)

### 6.2 Failure Modes

| Mode | Behavior | Outcome |
|------|----------|---------|
| Converted Connector | Executive rewards the connector with a title | Connector leaves the informal network; channel closes |
| Surveillance | Organization maps attendance for evaluation | Psychological safety collapses; attendance stops |
| Forum Theater | Executive attends but the room was staged | No candid knowledge; ECI unchanged |
| Vetted Space | Organization adds an approval committee, dashboard, or portfolio process to the adaptive space | The half-day becomes a proposal funnel; brokers submit instead of assemble; the space closes |
| Competence Tax | Institution loads the Energizer with administrative work "because they get things done" | Burnout; the energy converts to exhaustion; the channel closes |
| Recognition Theater | Institution substitutes symbolic reward (ceremony, praise, report inclusion) for fair compensation while continuing to use the connector's value | The connector is under-paid and over-used; the channel survives on extracted value until the connector leaves it — then it closes (Compensation Justice) |
| Inverted Pyramid | Institution reads load-shift as efficiency: a departure's work redistributes onto 2-3 remaining employees at the same salary, and cost-per-output improves | Fragility is invisible from the top; the pyramid is one resignation from crisis (RFC-0016); the veteran exit signal is the alarm nobody reads (Resilience Blindness; Veteran Exit Signal) |

### 6.3 Non-Goals

ESP does not create new metrics, new dashboards, or new reports. The
absence of infrastructure is a feature: the protocol is a habit, not a
program. The Technical Career Track (Rule ESP-7) is a compensation logic,
not a measurement system — TEC-based pay prices what the connector costs
to lose (RFC-0016 §3.3); it creates no tracking, no reporting, and no
surveillance of the connector's informal activity.

## 7. IANA Considerations

None. This protocol assigns no numbers, codes, or parameters.

## 8. References

### 8.1 Normative

- RFC-0017: Coffee-Break Protocol (CBP) — §3.2 Listen-Only CHP,
  §3.9.8 Non-Exploitation Condition
- RFC-0001: Hierarchical Omniscience Protocol (HOP) — §5.3 Requirement 15
- RFC-0016: Institutional Memory Backup Protocol (IMBP) — §3.3 Turnover
  Entropy Coefficient
- Theorem-001: Coffee Machine Theorem
- TERMINOLOGY: Inverted Pyramid, Resilience Blindness, Veteran Exit
  Signal, Competence Tax, Recognition Theater, Compensation Justice

### 8.2 Informative

- [Granovetter 1973] "The Strength of Weak Ties", *American Journal of Sociology*
- [Rajkumar et al. 2022] "A causal test of the strength of weak ties",
  *Science*
- [Arena, Cross, Sims, & Uhl-Bien 2017] "How to Catalyze Innovation in Your
  Organization", *MIT Sloan Management Review* 58(4): 39-47
- [Edmondson 1999] "Psychological Safety and Learning Behavior in Work Teams",
  *Administrative Science Quarterly*
- [Adams 1996] *The Dilbert Principle*, Scott Adams (Dilbert Principle:
  sub-competent employees are promoted into management to limit the damage
  they can do — management as containment, not reward)

## Appendix A: Changelog

- 2026-08-06: Created as Layer-A behavioral protocol (Camada A);
  Non-Capture Principle incorporated from the outgoing
  Inter-Institutional Weak-Tie Synchronization Protocol.
- 2026-08-06: Added connector archetypes (Broker / Central Connector /
  Energizer, Arena et al. 2017) as an observation aid (§3.3.1); added the
  Half-Day composite case study (§3.3.2); added the Vetted Space failure
  mode (§6.2).
- 2026-08-07: Added the Dilbert Effect (Adams 1996) as a second capture
  failure for the Energizer archetype (§3.3.1) and a failure-mode row
  (§6.2) — T080 harvest from the iLab source analysis.
- 2026-08-07: Amended Rule ESP-6 to state explicitly that Non-Capture
  forbids formalizing the *role* (title, position, reporting line, badge),
  never pricing the *value*; added Compensation Justice and Recognition
  Theater as paired doctrine and failure mode (§6.2) — T084.
- 2026-08-07: Corrected Dilbert attribution (T084 review): the *Dilbert
  Principle* (Adams 1996) is the promotion of sub-competents into
  management to limit damage, not the over-loading of the productive; the
  over-loading phenomenon is renamed the *Competence Tax* (§3.3.1, §6.2)
  and is no longer attributed to Adams.
- 2026-08-07: Added the Inverted Pyramid failure-mode row (§6.2) — the
  perception half of Compensation Justice: load-shift read as efficiency,
  fragility invisible from the top, the veteran exit as the alarm nobody
  reads (Inverted Pyramid, Resilience Blindness, Veteran Exit Signal) —
  T085.
- 2026-08-10: Added Ahmed's Paradox (Appendix C) unifying the four
  structural consequences of promoting the connector (informal magic,
  epistemic capture, Theorem-001 exclusion, Broker loss / FI↑); added
  Rule ESP-7 (Technical Career Track) and expanded the Rule ESP-6 wallet
  paragraph to reference it; clarified in §6.3 that the Technical Career
  Track is a compensation logic, not a measurement system — T109.

## Appendix B: Open Issues

1. **Connector Discriminator Precision**: Rule ESP-5 defines the
   connector by knowledge and structural reach. Formal centrality
   thresholds are deliberately absent to prevent metric gaming.
   [UNVERIFIED]

2. **Threshold Alignment Audit**: RFC-0001 §5.3 and RFC-0017 §3.2 agree
   on ECI ≥ 10. Any future divergence SHOULD be flagged. [UNVERIFIED]

---

## Appendix C: Ahmed's Paradox — Why Promoting the Connector Destroys Value

The institution's default reward path is promotion. For the connector,
promotion is destruction. Ahmed is the canon's connector archetype
(Platform Engineer; cast of characters; the Broker at the Living Lab
table): the person who knows who knows what, and routes knowledge
through informal channels. The paradox has four structural consequences.

**1. The informal magic dies.** The connector's value is
position-independent — it is the pattern of who asks them, which the
informal network maintains precisely because the connector has no formal
position (Rule ESP-6). Promotion fixes a position. People stop seeing a
peer of trust and see a node of hierarchy; the channel closes (Non-Capture
Principle; Theorem-001).

**2. Immediate epistemic capture.** As a manager, the connector receives
filtered and sanitized signals. Omniscience Radius (OR) increases —
several hops now separate them from operational reality — and Feedback
Fidelity (FF) falls as subordinates rationalize and filter. Epistemic
Capture Index (ECI) rises (RFC-0001). The connector loses the Trench
Intelligence that made them valuable in the first place.

**3. Exclusion from Theorem-001 venues.** The Coffee Machine Theorem
(CMT) defines informal hubs for non-manager vertices; managers use formal
channels and their presence in informal spaces is read as surveillance. A
promoted connector's attendance freezes the psychological safety of the
venue and converts conversation into Consensus Theater (RFC-0014).

**4. Broker loss raises fragmentation.** In the Adaptive Space the Broker
is the archetype that bridges otherwise disconnected clusters (Paper-014
§3.2). A Broker promoted into a coordination role leaves the informal
network, the bridge closes, and the Fragmentation Index (FI) rises
(RFC-0003). The testemunho (Paper-014 §3.7) fails: the connector is no
longer present to pass the baton.

**The compensation corollary.** The Alternative — Valorização Silenciosa —
is the Technical Career Track (Rule ESP-7). TEC-based pay prices what the
connector costs to lose, not what a position costs to fill: RFC-0016
§3.3 assigns the connector a TEC multiplier of 8.0x, and the canon's own
"10% trap" case (Paper-007) shows a unique specialist denied a modest
raise leaving for 7x, with replacement cost at 10x annual compensation
and a Knowledge Half-Life collapse. Status comes through the Knowledge
Steward title (RFC-0009 §3.3) and peer-nominated recognition; sovereignty
through architectural veto — truth-vertex authority without power-vertex
conversion; protected, unmonitored time preserves the venues where the
connector works (RFC-0017 §3.9.8). Pay the connector what their departure
costs. Never promote them.

## Colophon

**Epistemic Integrity Level 4 (EI-4): Independent Replication Required**

This RFC prescribes executive behaviors whose efficacy claims depend on:
- Weak-tie novelty transmission (Granovetter 1973; Rajkumar et al. 2022)
  — replicated experimentally, but not in organizational power settings
- Listen-Only CHP ECI reduction (RFC-0017 §3.2) — deployment data
  restricted (executive privacy)
- Non-Capture Principle — theoretical, derived from Theorem-001

**Replication Status**: Not yet replicated
**Pre-registration**: None required (behavior protocol)
**Data Availability**: CBP session data restricted (RFC-0017 privacy model)
**OEP Integration**: RFC-0017 §3.2, RFC-0001 §5.3, RFC-0005, RFC-0021
depend on voluntary executive behavior. ESP adds no new parameters.

**Review Trigger**: Any independent deployment reporting behavioral
change in executive knowledge reception (measured qualitatively, not by
ECI publication) should trigger RFC-0035 parameter review.
