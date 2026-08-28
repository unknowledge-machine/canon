---
rfc: "0007"
title: "Organizational Amnesia Prevention Protocol (OAPP)"
stream: "Best Current Practice"
status: "DRAFT"
category: "Informational"
area: "knowledge-ops"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2008-09-15"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [3, 5, 6, 16, 17]
keywords: [amnesia, organizational-memory, knowledge-half-life,
  knowledge-continuity, turnover, restructuring, tool-migration]
abstract: |
  This document specifies the Organizational Amnesia Prevention Protocol (OAPP),
  a Best Current Practice for preventing systematic loss of institutional memory
  through turnover, restructuring, and tool churn. OAPP defines the Knowledge
  Half-Life (KHL) metric, a 7-level Criticality Taxonomy for knowledge tagging,
  mandatory pre-departure tacit knowledge externalization for Existential and
  Critical knowledge, Knowledge Continuity Plans (KCP) as mandatory restructuring
  gates, and tagged-only tool migration. Organizations implementing OAPP reduce
  knowledge half-life decay by maintaining continuity through disruption vectors.
  While framed as a prevention protocol, OAPP functions analytically as a
  diagnostic instrument for organizational memory health.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0007 — Organizational Amnesia Prevention Protocol (OAPP)

## Abstract

This document specifies the Organizational Amnesia Prevention Protocol (OAPP),
a Best Current Practice for preventing systematic loss of institutional memory
through turnover, restructuring, and tool churn. OAPP defines the Knowledge
Half-Life (KHL) metric, a 7-level Criticality Taxonomy for knowledge tagging,
mandatory pre-departure tacit knowledge externalization for Existential and
Critical knowledge, Knowledge Continuity Plans (KCP) as mandatory restructuring
gates, and tagged-only tool migration. Organizations implementing OAPP reduce
knowledge half-life decay by maintaining continuity through disruption vectors.
While framed as a prevention protocol, OAPP functions analytically as a
diagnostic instrument for organizational memory health.

> **Dual-Layer Notice**: This RFC employs the Organizational Amnesia Prevention
> Protocol (OAPP) as a satirical vehicle for presenting peer-reviewed findings
> on organizational memory dynamics (Walsh & Ungson 1991; Argote 1999; Nonaka &
> Takeuchi 1995; Edmondson 2019). While OAPP employs satirical framing, the
> organizational claims are substantiated by the cited literature. Implementers
> should treat OAPP as an analytical lens, not a deployable governance protocol
> — though some organizations have reportedly "implemented" it by requiring
> knowledge continuity plans before every reorg.

## 1. Introduction

### 1.1 Motivation

Walsh and Ungson (1991) established that organizations possess memory systems
with identifiable retention bins and decay functions. Argote (1999) demonstrated
that organizational learning decays without active reinforcement. Nonaka and
Takeuchi (1995) established the SECI model: knowledge creation requires
continuous externalization, combination, and internalization.

Organizational amnesia — the systematic loss of institutional memory through
turnover, restructuring, and tool churn — is not a bug but a thermodynamic
certainty (Theorem-002: Committee Entropy). The Organizational Amnesia
Prevention Protocol (OAPP) makes this entropy measurable and manageable.

### 1.2 Scope

This document specifies:
- Knowledge Half-Life (KHL) metric with hybrid time/event measurement
- 7-level Criticality Taxonomy for knowledge tagging (Existential → Nice-to-know)
- Mandatory pre-departure tacit knowledge externalization for Existential/Critical
- Knowledge Continuity Plans (KCP) as mandatory restructuring gates
- Tagged-only tool migration with explicit abandonment of untagged
  knowledge
- Tacit knowledge externalization protocols (pairing, shadowing,
  narrative capture)
- Integration with RFC-0003 (Fragmentation), RFC-0005 (Gravity),
  RFC-0006 (SMDP), RFC-0016 (Backup), RFC-0017 (CBP)

### 1.3 Non-Goals

This document does not specify:
- Automated knowledge extraction (AI/ML) — see BCP-XXXX
- Legal/compliance retention (GDPR, SOX) — out of scope
- Knowledge backup/restore mechanics — RFC-0016 (Institutional Memory Backup)
- Individual learning/development — HR scope

### 1.4 Relationship to Other RFCs

| RFC | Relationship |
|-----|--------------|
| RFC-0003 (Fragmentation) | Amnesia accelerates fragmentation; KHL and FI correlated |
| RFC-0005 (Gravity) | Amnesia creates gravity wells; knowledge orbits power |
| RFC-0006 (SMDP) | Amnesia → decisions untethered from strategy; SMI and KHL correlated |
| RFC-0016 (Memory Backup) | OAPP = prevention; RFC-0016 = last-resort restore |
| RFC-0017 (CBP) | CBP edges as amnesia-resistant knowledge sync channels |

## 2. Terminology

| Term | Definition |
|------|------------|
| **Organizational Amnesia** | Systematic loss of institutional memory through turnover, restructuring, and tool churn |
| **Knowledge Half-Life (KHL)** | Time until 50% of knowledge holders for a concept are gone OR event-triggered decay |
| **Criticality Taxonomy** | 7-level hierarchy for knowledge tagging (Existential → Nice-to-know) |
| **Knowledge Continuity Plan (KCP)** | Mandatory document for restructuring: knowledge mapping, transfer plan, verification |
| **Tacit Knowledge Externalization** | Pre-departure conversion of tacit knowledge to explicit artifacts |
| **Tagged-Only Migration** | Tool migration scope limited to tagged knowledge; untagged explicitly abandoned |
| **Knowledge Half-Life (KHL)** | Hybrid metric: time-to-50%-holder-gone + event-triggered decay on departure/reorg/migration |
| **Criticality Level** | 7-level tag: Existential (0) → Critical (1) → High (2) → Important (3) → Useful (4) → Minor (5) → Nice-to-know (6) |

## 3. Protocol Specification

### 3.1 Knowledge Half-Life (KHL) Metric

**Requirement 1**: Organizations MUST measure Knowledge Half-Life (KHL) for all
tagged knowledge using the hybrid metric:

```
KHL = min( T_time, T_event )
```

Where:
- `T_time` = calendar months until 50% of original knowledge holders are gone
- `T_event` = 0 triggered on: departure of holder, restructuring affecting domain, tool migration

**Requirement 2**: KHL MUST be reported quarterly with 95% confidence intervals
via bootstrap resampling (1000 iterations over knowledge holders).

**Requirement 3**: KHL thresholds:

| KHL Range | Classification | Action |
|-----------|----------------|--------|
| KHL > 36 months | Stable | Routine monitoring |
| 18–36 months | At Risk | Quarterly review; targeted reinforcement |
| 6–18 months | Critical Decay | Mandatory reinforcement (pairing, documentation) |
| < 6 months | Collapse Imminent | Emergency capture; RFC-0016 backup triggered |

**Requirement 4**: KHL MUST be computed per Criticality Level (Existential decay
triggers immediate action regardless of aggregate KHL).

### 3.2 Criticality Taxonomy (7 Levels)

**Requirement 5**: All organizational knowledge MUST be tagged with one of seven
Criticality Levels:

| Level | Label | Definition | Retention Target |
|-------|-------|------------|------------------|
| 0 | **Existential** | Loss threatens org survival (regulatory, safety, core IP) | Permanent; multi-holder |
| 1 | **Critical** | Loss causes severe operational/financial/regulatory impact | Multi-holder; documented |
| 2 | **High** | Loss causes significant degradation; recoverable at high cost | Documented + 2 holders |
| 3 | **Important** | Loss causes measurable degradation; recoverable at moderate cost | Documented + 1 holder |
| 4 | **Useful** | Loss causes minor inconvenience; easily relearned | Documented or 1 holder |
| 5 | **Minor** | Loss causes negligible impact; easily recreated | Optional documentation |
| 6 | **Nice-to-know** | No measurable impact if lost; cultural/historical | No retention required |

**Requirement 6**: Tagging MUST be performed by knowledge owner + one peer reviewer
within 30 days of knowledge creation. Disputes resolved by RFC-0010 (Epistemic Injustice) panel.

**Requirement 7**: Criticality tags MUST be reviewed annually. Downgrade requires
evidence of reduced impact; upgrade requires evidence of increased criticality.

### 3.3 Knowledge Half-Life Measurement Protocol

**Requirement 8**: KHL measurement MUST use hybrid methodology:

- **Time Component**: Track holder count decay monthly; T_time = months to 50% holder loss
- **Event Component**: T_event = 0 on any trigger event:
  - Departure of any knowledge holder
  - Restructuring affecting knowledge domain
  - Tool migration affecting knowledge artifacts
  - Reorganization changing reporting lines for holders

**Requirement 9**: KHL reporting MUST include:
- Per-concept KHL with 95% CI
- Per-Criticality-Level aggregate KHL
- Top-10 fastest decaying concepts
- Event-triggered decay events log

### 3.4 Critical Knowledge Tagging Protocol

**Requirement 10**: All knowledge artifacts MUST be tagged at creation:

- **Artifacts**: Documents, code repos, wikis, runbooks, architectures, runbooks
- **Tag Fields**: `criticality_level` (0-6), `knowledge_holders` (list), `domain`, `last_verified`
- **Verification**: Annual review mandatory for Existential/Critical/High

**Requirement 11**: Criticality tagging disputes resolved via RFC-0010 (Epistemic
Injustice) panel within 14 days.

### 3.5 Pre-Departure Tacit Knowledge Externalization

**Requirement 12**: For Existential (Level 0) and Critical (Level 1) knowledge,
departing holders MUST complete Tacit Knowledge Externalization (TKE) before
departure:

| TKE Method | Applicable Levels | Duration | Verification |
|------------|-------------------|----------|--------------|
| **Pairing/Shadowing** | Existential, Critical | Min 5 sessions × 90 min | Observer sign-off |
| **Narrative Capture** | Existential, Critical | 3–5 structured interviews | Transcript + summary |
| **Decision Replay** | Existential | 2–3 sessions | Decision log + rationale |
| **Code/Artifact Walkthrough** | Critical | 2–3 sessions | Annotated artifacts |

**Requirement 13**: TKE MUST be scheduled within 48 hours of departure notice.
Failure to complete TKE blocks departure clearance for Existential knowledge.

**Requirement 14**: TKE artifacts MUST be tagged with `tke_source: departure`,
`original_holder`, `criticality_level`, and linked to original knowledge artifacts.

### 3.6 Knowledge Continuity Plan (KCP) — Restructuring Gate

**Requirement 15**: Any restructuring affecting ≥ 5 people or ≥ 2 teams MUST have
an approved Knowledge Continuity Plan (KCP) before launch.

**KCP Required Sections**:

| Section | Content |
|---------|---------|
| **Knowledge Map** | Affected domains, criticality levels, current holders |
| **Transfer Plan** | Pairing assignments, shadowing schedule, documentation targets |
| **Verification Plan** | Knowledge checks, quizzes, pairing sessions post-reorg |
| **Risk Register** | High-risk knowledge (single holder, no doc), mitigation |
| **Timeline** | Pre-reorg (KCP approval), during (transfer), post (verification at 30/60/90 days) |
| **Rollback Criteria** | KHL thresholds triggering reorg pause |

**Requirement 16**: KCP MUST be approved by independent epistemology auditor
(RFC-0016) before restructuring launch. Reorg without approved KCP is a
protocol violation.

**Requirement 17**: Post-reorg verification at 30/60/90 days MUST measure KHL
for affected domains. KHL regression > 20% triggers mandatory review.

### 3.6 Tacit Knowledge Externalization Protocol (Continuous)

**Requirement 18**: Beyond pre-departure TKE, organizations SHOULD implement
continuous tacit externalization:

| Practice | Frequency | Target Levels | Method |
|----------|-----------|---------------|--------|
| **Pairing/Rotation** | Quarterly | Existential, Critical | Cross-team pairing; knowledge transfer |
| **Decision Replay** | Per major decision | Existential | Structured retrospective: context, options, rationale |
| **Narrative Capture** | Semi-annual | Critical, Important | Structured interviews → searchable narratives |
| **Artifact Walkthrough** | Per major release | Critical | Annotated code/doc walkthroughs |

**Requirement 19**: Externalization artifacts MUST be tagged with `tke_source:
continuous`, `criticality_level`, and linked to knowledge graph.

### 3.7 Tagged-Only Tool Migration

**Requirement 20**: Tool migrations (wiki, ticketing, chat, docs) MUST migrate
only tagged knowledge (Criticality Levels 0–4). Untagged knowledge (Levels 5–6)
is explicitly abandoned.

**Requirement 21**: Migration verification MUST confirm:
- 100% of Existential/Critical artifacts migrated and verified
- ≥ 90% of High/Important artifacts migrated and verified
- Migration log with source→target mapping, verification status, owner sign-off

**Requirement 22**: Untagged knowledge abandoned in migration MUST be logged in
Abandonment Register with explicit owner acknowledgment.

### 3.8 Normative Requirements Summary

| Req | Parameter | MUST | SHOULD | MAY |
|-----|-----------|------|--------|-----|
| 1 | KHL hybrid metric | YES | | |
| 2 | Quarterly KHL + CI | YES | | |
| 3 | KHL thresholds table | YES | | |
| 4 | Per-criticality KHL | YES | | |
| 5 | 7-level tagging | YES | | |
| 6 | Tagging review + disputes | YES | | |
| 7 | Annual tag review | YES | | |
| 8 | Hybrid KHL measurement | YES | | |
| 9 | KHL reporting format | YES | | |
| 10 | Tagging at creation | YES | | |
| 11 | Tag dispute resolution | YES | | |
| 12 | Pre-departure TKE (0,1) | YES | | |
| 13 | TKE scheduling (48h) | YES | | |
| 14 | TKE artifact tagging | YES | | |
| 15 | KCP for reorg (≥5 people/≥2 teams) | YES | | |
| 16 | KCP independent audit | YES | | |
| 17 | Post-reorg KHL verification | YES | | |
| 18 | Continuous TKE practices | | YES | |
| 19 | TKE artifact tagging | YES | | |
| 20 | Tagged-only migration (0–4) | YES | | |
| 21 | Migration verification | YES | | |
| 22 | Abandonment register | YES | | |

## 4. Operational Considerations

### 4.1 Deployment Models

OAPP is a diagnostic, not a governance mandate. Organizations MAY apply as:

1. **Passive Radar**: Continuous KHL + tagging from existing data. No intervention.
2. **Quarterly Audit**: KHL + tagging review drives targeted documentation sprints.
3. **Executive Dashboard**: KHL trends + top-10 decaying concepts reported to C-suite.
4. **CBP Integration**: High KHL triggers CBP intensification (RFC-0017).

### 4.2 Failure Modes

| Failure Mode | Mechanism | Detection | Mitigation |
|--------------|-----------|-----------|------------|
| **Tagging Theater** | Tags applied without verification | Low verification rate | Mandatory peer review; RFC-0010 panel |
| **TKE Theater** | Departing employees "perform" TKE without substance | Low artifact quality | Observer sign-off; artifact quality rubric |
| **KCP Checkbox** | KCP created but not executed | Post-reorg KHL regression | Mandatory 30/60/90 verification |
| **Criticality Inflation** | Everything tagged Existential/Critical | Tag distribution audit | Fixed quota per level; RFC-0010 panel |
| **Tool Migration Gaming** | Tag everything to force migration | Migration log audit | Tag quota enforcement; RFC-0010 panel |

### 4.3 Monitoring and Alerting

**Requirement 23**: Organizations implementing OAPP SHALL alert when:
- Any Existential/Critical concept KHL < 12 months
- Aggregate KHL crosses threshold (18 months)
- Reorg launched without approved KCP
- Migration verification < 90% for Critical+
- TKE completion rate < 80% for departing Existential/Critical holders

## 5. Security & Privacy Considerations

### 5.1 Epistemic Security

KHL data and criticality tags reveal:
- Which units hold existential knowledge (target for poaching)
- Single points of failure (bus factors)
- Knowledge gravity wells (power mapping)

**Requirement 24**: KHL data SHALL be classified at same level as org restructuring
plans. Access limited to: measured units, C-suite, independent epistemology auditor.

### 5.2 Individual Privacy

KHL computation uses digital traces (Git, Slack, Calendar, Tickets).

**Requirement 25**: Aggregation to role level (minimum 3 individuals) before
KHL computation. Individual-level graphs PROHIBITED for KHL reporting.

**Requirement 26**: Survey responses (TKE, criticality tagging) MUST be
anonymized. Minimum response threshold: 3 respondents per role.

### 5.3 CBP Integrity (RFC-0017 §7)

OAPP uses CBP edges in knowledge graphs. If KHL monitoring incentivizes
executives to attend coffee breaks for "centrality boosting," CBP's epistemic
integrity is compromised.

**Requirement 27**: CBP edges used in KHL MUST be anonymized and aggregated.
No executive attendance tracking for KHL purposes.

## 6. OSC Considerations

### 6.1 Registry Updates

This RFC requests:
- RFC-0007 allocated in Best Current Practice, knowledge-ops area (0300–0399)
- Keywords: amnesia, organizational-memory, knowledge-half-life,
  knowledge-continuity, turnover, restructuring, tool-migration
- See-also: RFC-0003, RFC-0005, RFC-0006, RFC-0016, RFC-0017

### 6.2 Code Points

OAPP defines no code points. KHL thresholds, Criticality Levels, and KCP
templates are informational guidelines.

## 7. References

### 7.1 Normative References

[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003,
Organizational Standards Consortium, 1992. https://rfc.osc.org/rfc0003

[RFC-0005] Matos, R. "Knowledge Gravity Measurement Framework." RFC 0005,
Organizational Standards Consortium, 1998. https://rfc.osc.org/rfc0005

[RFC-0006] Matos, R.M. "Strategic Misalignment Detection Protocol." RFC 0006,
Organizational Standards Consortium, 2026. https://rfc.osc.org/rfc0006

[RFC-0010] Matos, R.M. "Epistemic Injustice Remediation Protocol." RFC 0010,
Organizational Standards Consortium, 2026. https://rfc.osc.org/rfc0010

[RFC-0016] Matos, R.M. "Institutional Memory Backup Specification." RFC 0016,
Organizational Standards Consortium, 2026. https://rfc.osc.org/rfc0016

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017,
Organizational Standards Consortium, 2001. https://rfc.osc.org/rfc0017

### 7.2 Informative References

Argote, Linda. 1999. *Organizational Learning: Creating, Retaining and
Transferring Knowledge*. Boston: Kluwer Academic Publishers.

Edmondson, Amy C. 2019. *The Fearless Organization: Creating Psychological Safety
in the Workplace for Learning, Innovation, and Growth*. Hoboken: Wiley.

Nonaka, Ikujiro, and Hirotaka Takeuchi. 1995. *The Knowledge-Creating Company:
How Japanese Companies Create the Dynamics of Innovation*. New York: Oxford
University Press.

Walsh, James P., and Gerardo Rivera Ungson. 1991. "Organizational Memory."
*Academy of Management Review* 16 (1): 57–91.
https://doi.org/10.5465/amr.1991.4278992.

Wenger, Etienne. 1998. *Communities of Practice: Learning, Meaning, and
Identity*. Cambridge: Cambridge University Press.

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2008-09-15 | R. Matos | Initial draft post-financial crisis knowledge loss |
| 0.2 | 2018-09-01 | R. Matos | Digital tool migration amnesia recognition |
| 0.3 | 2020-03-01 | R. Matos | Pandemic: remote work amnesia; remote TKE |
| 1.0 | 2026-07-18 | Rodolfo Matos | OEP canon alignment; 7-level taxonomy; hybrid KHL; mandatory KCP |

## Appendix B: Open Issues

1. **KHL Causal Direction**: Does low KHL cause poor outcomes, or do poor
   outcomes cause knowledge loss? Longitudinal RCT needed. [UNVERIFIED]

2. **Criticality Inflation Control**: Fixed quota per level vs dynamic threshold.
   Quota prevents inflation but may misclassify. [UNVERIFIED]

3. **TKE Quality Metric**: How to measure TKE artifact quality beyond completion?
   Rubric needed: completeness, actionability, searchability. [UNVERIFIED]

4. **Remote/Hybrid TKE**: Pairing/shadowing in distributed teams. Tool-mediated
   TKE quality vs in-person. [UNVERIFIED]

5. **Cross-Cultural KHL**: High-power-distance cultures may have systematically
   different baseline KHL (knowledge concentrated at top). [UNVERIFIED]

6. **KCP for Mergers/Acquisitions**: Special KCP variant for M&A knowledge
   integration. Different timescale, different stakes. [UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Walsh, Ungson, Argote, Nonaka, Takeuchi,
> Edmondson, Nonaka, Takeuchi, etc.) are accurate. The coffee machine, however,
> is real — and it is currently synchronizing more knowledge than this
> repository ever will.