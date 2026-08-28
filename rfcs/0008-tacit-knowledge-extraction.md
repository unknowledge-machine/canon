---
rfc: "0008"
title: "Tacit Knowledge Extraction Protocol (DEPRECATED)"
stream: "Experimental"
status: "OBSOLETE"
category: "Informational"
area: "epistemology"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "1995-06-15"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: [7, 16]
see_also: [7, 16, 17]
keywords: [tacit-knowledge, extraction, departure, externalization, deprecated]
abstract: |
  This document specifies the Tacit Knowledge Extraction Protocol (TKEP), an
  early attempt to capture departing employees' tacit knowledge through
  structured interviews and artifact capture. TKEP is now OBSOLETE, superseded
  by RFC-0007 (Organizational Amnesia Prevention Protocol) and RFC-0016
  (Institutional Memory Backup Specification). TKEP failed because it treated
  tacit knowledge as an extractable artifact at a single point in time
  (departure), violating the fundamental nature of tacit knowledge as
  personal, context-dependent, and socially embedded (Polanyi 1966; Nonaka &
  Takeuchi 1995). This document is retained as a cautionary tale.
dual_layer: true
satire_notice: "dual-layer"
---

# RFC-0008 — Tacit Knowledge Extraction Protocol (TKEP) — OBSOLETE

## Abstract

This document specifies the Tacit Knowledge Extraction Protocol (TKEP), an
early OSC attempt to capture departing employees' tacit knowledge through
structured exit interviews and artifact capture. TKEP is now **OBSOLETE**,
superseded by RFC-0007 (Organizational Amnesia Prevention Protocol) and
RFC-0016 (Institutional Memory Backup Specification).

TKEP failed because it treated tacit knowledge as an extractable artifact at a
single point in time (departure), violating the fundamental nature of tacit
knowledge as personal, context-dependent, and socially embedded (Polanyi 1966;
Nonaka & Takeuchi 1995). This document is retained as a cautionary tale.

> **Dual-Layer Notice**: This RFC documents a failed protocol. The satirical
> framing highlights the absurdity of believing tacit knowledge can be
> "extracted" like a tooth; the serious layer documents why the approach
> fundamentally misunderstands the nature of tacit knowledge.

---

## 1. Introduction

### 1.1 Historical Context

In 1995, following Nonaka and Takeuchi's *The Knowledge-Creating Company*,
the OSC chartered a working group to "solve the departure problem" — the
observed loss of critical knowledge when experienced employees left. The
resulting TKEP (RFC-0008) specified structured exit interviews, artifact
collection, and a "knowledge will" document.

### 1.2 Why TKEP Failed

TKEP was based on a category error: it treated **tacit knowledge** as if it
were **explicit knowledge** waiting to be transcribed. The protocol assumed:

1. **Extractability**: Tacit knowledge can be articulated on demand
2. **Timeliness**: Departure is an appropriate extraction moment
3. **Cooperation**: Departing employees will faithfully reveal deep knowledge
4. **Completeness**: Captured artifacts represent the knowledge

All four assumptions are false (Polanyi 1966; Nonaka & Takeuchi 1995;
Edmondson 2019).

### 1.3 Supersession

TKEP is **OBSOLETE**, obsoleted by:
- **RFC-0007** (OAPP): Continuous tacit externalization via pairing, shadowing, narrative capture
- **RFC-0016** (IMB): Immutable backup of critical knowledge artifacts

This document is retained as a cautionary tale.

---

## 2. Terminology (Historical)

| Term | Definition |
|------|------------|
| **Knowledge Will** | TKEP artifact: departing employee's documented knowledge bequest |
| **Extraction Interview** | Structured departure interview using TKEP questionnaire |
| **Knowledge Artifact** | Document, diagram, code snippet, or recording produced by TKEP |
| **Extraction Completeness** | TKEP metric: % of identified knowledge domains covered |
| **Tacit Residue** | Knowledge not captured by TKEP (always > 0) |

---

## 3. Protocol Specification (Historical)

### 3.1 Extraction Process (Failed)

```ascii
Departure Notice
      |
      v
TKEP Initiation (HR triggers)
      |
      v
Knowledge Domain Mapping (HR + Manager)
      |
      v
Extraction Interviews (3-5 sessions)
      |
      v
Artifact Collection (docs, code, diagrams)
      |
      v
Knowledge Will Signing
      |
      v
Archive Deposit
```

### 3.2 Extraction Interview Template (Failed)

| Phase | Activity | Duration | Failure Mode |
|-------|----------|----------|--------------|
| 1 | Domain mapping | 60 min | Employee lists what they *think* they know |
| 2 | Critical incidents | 90 min | Employee recounts "war stories" (survivorship bias) |
| 3 | Decision replay | 90 min | Employee explains past decisions (hindsight bias) |
| 4 | Implicit rules | 60 min | Employee articulates unwritten rules (cannot) |
| 5 | Successor briefing | 60 min | Handoff to successor (low fidelity) |

### 3.3 Knowledge Will Artifact (Failed)

```markdown
# Knowledge Will of [Employee]

## Domains
- [ ] Domain A: ...
- [ ] Domain B: ...

## Critical Artifacts
- Document: ...
- Code: ...
- Diagram: ...

## Unwritten Rules
1. ...
2. ...

## Advice to Successor
...

Signed: _________________ Date: ________
```

---

## 4. Failure Mode Analysis (Post-Mortem)

### 4.1 Fundamental Category Error

| TKEP Assumption | Reality (Polanyi/Nonaka/Edmondson) |
|-----------------|-------------------------------------|
| Tacit knowledge is extractable | Tacit knowledge is personal, context-dependent, inexpressible (Polanyi 1966) |
| Departure is extraction moment | Knowledge walks out daily; departure is the visible event |
| Employee will cooperate | Zero incentive; psychological safety absent (Edmondson 2019) |
| Artifacts = knowledge | Artifacts are traces; knowledge is the practice (Nonaka SECI) |

### 4.2 Measured Failure Modes

| Metric | Target | Actual | Gap |
|--------|--------|--------|-----|
| Domain coverage | 90% | 23% | Tacit domains invisible |
| Artifact fidelity | 80% | 12% | Artifacts are traces, not knowledge |
| Successor readiness | 90% | 34% | Successor learns by doing, not reading |
| Knowledge retention at 6mo | 80% | 18% | Tacit residue decays immediately |

### 4.3 Structural Failure Modes

| Failure Mode | Mechanism | Evidence |
|--------------|-----------|----------|
| **Survivorship Bias** | Employee recounts successes, not failures | "War stories" dominate interviews |
| **Hindsight Bias** | Decision replay rationalizes past choices | Post-hoc rationalization |
| **Articulation Failure** | "I know it but can't explain it" | Tacit residue > 80% |
| **Incentive Misalignment** | No reward for depth; risk of liability | Minimal compliance |
| **Successor Overload** | Dumped artifacts without context | Successor learns by doing anyway |

---

## 5. Why Continuous Externalization (RFC-0007) Works Where TKEP Failed

| Dimension | TKEP (RFC-0008) | OAPP (RFC-0007) |
|-----------|-----------------|-----------------|
| **Timing** | Point-in-time (departure) | Continuous (pairing, shadowing) |
| **Social Context** | Solo interview | Social practice (pairing, shadowing) |
| **Psychological Safety** | None (departure = exit) | Built-in (ongoing relationships) |
| **Verification** | None (artifact = truth) | Continuous (pairing validates daily) |
| **Incentive** | None | Built-in (mutual learning) |
| **Tacit Handling** | Extraction attempt | Externalization via practice |

---

## 6. Lessons for Future Protocols

1. **Tacit knowledge is not an artifact** — it cannot be extracted,
   only externalized through practice
2. **Timing matters** — continuous > point-in-time
3. **Social context is essential** — pairing, shadowing, community
   of practice
5. **Prevention > extraction** — RFC-0007 prevents amnesia; RFC-0016
   backs up; RFC-0008 tried to extract (failed)

---

## 6. References

### 6.1 Normative References

[RFC-0007] Matos, R.M. "Organizational Amnesia Prevention Protocol
(OAPP)." RFC 0007, OSC, 2008. https://rfc.osc.org/rfc0007

[RFC-0016] Matos, R.M. "Institutional Memory Backup Specification
(IMB)." RFC 0016, OSC, 2026. https://rfc.osc.org/rfc0016

[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017,
OSC, 2001. https://rfc.osc.org/rfc0017

### 6.2 Informative References

Nonaka, Ikujiro, and Hirotaka Takeuchi. 1995. *The Knowledge-Creating
Company: How Japanese Companies Create the Dynamics of Innovation*.
New York: Oxford University Press.

Polanyi, Michael. 1966. *The Tacit Dimension*. Chicago: University
of Chicago Press.

Edmondson, Amy C. 2019. *The Fearless Organization: Creating
Psychological Safety in the Workplace for Learning, Innovation,
and Growth*. Hoboken: Wiley.

Argote, Linda. 1999. *Organizational Learning: Creating, Retaining
and Transferring Knowledge*. Boston: Kluwer Academic Publishers.

Edmondson, Amy C. 1999. "Psychological Safety and Learning Behavior
in Work Teams." *Administrative Science Quarterly* 44 (2):
350–383.

---

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 1995-06-15 | R. Matos | Initial draft (TKEP v1) |
| 0.2 | 2008-09-15 | R. Matos | Post-financial crisis: recognition of failure |
| 0.3 | 2020-03-01 | R. Matos | Pandemic: remote departure extraction impossible |
| 1.0 | 2026-07-18 | Rodolfo Matos | OBSOLETE; canon alignment; references to RFC-0007/0016 |

## Appendix B: Open Issues (Permanent)

1. **Can ANY protocol extract tacit knowledge at departure?** [UNVERIFIED]
2. **Is "tacit knowledge" even a coherent category?** Polanyi
says yes; critics say no. [UNVERIFIED]
3. **Could AI-assisted extraction work?** [UNVERIFIED]
4. **What about "knowledge wills" as cultural artifacts (not functional)?** [UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs, OEPs, Theorems, and Papers published under the OSC
> imprint are satirical artifacts that encode genuine organizational science.
> All citations of real scholars (Polanyi, Nonaka, Takeuchi, Edmondson, etc.)
> are accurate. The coffee machine, however, is real — and it is currently
> synchronizing more knowledge than this protocol ever extracted.