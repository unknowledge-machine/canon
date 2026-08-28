---
rfc: "0012"
title: "Slide Deck Compression Algorithm"
stream: "Experimental"
status: "DRAFT"
category: "Informational"
area: "informal-networks"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-18"
updated: "2026-07-18"
obsoletes: []
obsoleted_by: []
see_also: [11, 13]
keywords: [slides, compression, information-loss, bullet-points, death-by-powerpoint]
abstract: |
  This document specifies the Slide Deck Compression Algorithm
  (SDCA), a formal model for quantifying and compressing the
  information content of organizational slide decks. SDCA
  introduces the Information Density Metric (IDM), the Bullet
  Point Compression Ratio (BPCR), the Animation Overhead
  Factor (AOF), and the Death-by-Powerpoint Threshold (DPT).
  Information content in slide decks is inversely proportional
  to the number of slides.
dual_layer: true
satire_notice: "satire"
---

# RFC-0012 -- Slide Deck Compression Algorithm

## Abstract

This document specifies the Slide Deck Compression Algorithm
(SDCA), a formal model for quantifying and compressing the
information content of organizational slide decks. SDCA
introduces the Information Density Metric (IDM), the Bullet
Point Compression Ratio (BPCR), the Animation Overhead
Factor (AOF), and the Death-by-Powerpoint Threshold (DPT).
Information content is inversely proportional to slide count.

> **Satire Notice**: This document is published in the
> **Experimental** stream. While technically coherent, its
> primary purpose is satirical illumination of slide deck
> pathologies. The OSC does not recommend deploying SDCA
> without peer review, a projector, and a working clicker.

## 1. Introduction

Every slide deck follows a predictable trajectory: initial
purpose, bullet point inflation, animation creep, and
collapse into a 42-slide deck that says what a paragraph
could have said. SDCA formalizes this trajectory to measure,
predict, and compress slide deck information loss.

The core insight: information content is inversely
proportional to slide count. At some critical threshold,
the deck enters Death-by-Powerpoint territory.

## 2. Terminology

| Term | Definition |
|------|------------|
| **Slide** | A unit of media conveying at most one idea. |
| **Bullet Point** | Text prefixed by a glyph, suggesting importance. |
| **Animation** | A transition adding motion without information. |
| **IDM** | Information content per slide in bits. |
| **DPT** | Slide count beyond which comprehension collapses. |
| **Deck** | A sequence of slides, typically longer than needed. |
## 3. Protocol Specification

### 3.1 Information Density Metric (IDM)
```
IDM = (W_meaningful * log2(S)) / N_slides
```
`W_meaningful` = meaningful word count.
`S` = vocabulary size. `N_slides` = total slides.
IDM decreases as slide count increases: `IDM(N) = I / N`.

| Deck Type | IDM (bits/slide) | Quality |
|-----------|-------------------|---------|
| Executive Summary | 45.0 | Excellent |
| Technical Spec | 30.0 | Good |
| Sales Pitch | 15.0 | Mediocre |
| Status Update | 8.0 | Poor |
| "Strategic Vision" | 3.0 | Pathological |

### 3.2 Bullet Point Compression Ratio (BPCR)

```
BPCR = N_meaningful / N_total
```

| BPCR Range | Classification |
|------------|---------------|
| 0.8 - 1.0 | Dense |
| 0.5 - 0.8 | Normal |
| 0.2 - 0.5 | Bloated |
| 0.0 - 0.2 | Critical |

Decay: `BPCR(N) = 0.9 / log2(N + 1)`.
At N=10: ~0.27. At N=50: ~0.13.

### 3.3 Animation Overhead Factor (AOF)

```
AOF = 1 / (1 + 0.3 * N_animations)
```

| Animations | AOF | Comprehension Loss |
|-----------|-----|-------------------|
| 0 | 1.00 | 0% |
| 5 | 0.40 | 60% |
| 10 | 0.25 | 75% |
| 20 | 0.14 | 86% |

### 3.4 Death-by-Powerpoint Threshold (DPT)

```
DPT = (C_audience * T_attention) / IDM_target
```

| Audience | DPT |
|----------|-----|
| Engineers | 15 slides |
| Managers | 8 slides |
| Executives | 5 slides |
| Board | 3 slides |

DPT for executives confirms the "Rule of 5" widely known
but never followed.

### 3.5 SDCA Packet Structure

```
SDCA_SYN:
  deck_id: string
  slide_count: int
  total_bullets: int
  animated_transitions: int

SDCA_DATA:
  deck_id: string
  current_slide: int
  idm: float
  bpcr: float
  aof: float

SDCA_FIN:
  deck_id: string
  slides_delivered: int
  slides_actually_read: int
  idm_final: float
  dpt_exceeded: boolean
```

### 3.6 Compression Algorithm

```
COMPRESS(deck):
  1. Compute IDM for full deck
  2. If IDM > IDM_target: return
  3. Sort slides by IDM contribution (ascending)
  4. While IDM < IDM_target AND slides remain:
     a. Remove lowest-IDM slide
     b. Redistribute meaningful bullets
     c. Recompute IDM
  5. Remove all animations (AOF = 1.0)
  6. Verify DPT not exceeded
```

| Deck Type | Compression Ratio |
|-----------|-------------------|
| Sales Pitch | 3.2x |
| Status Update | 5.0x |
| "Vision" Deck | 8.0x |
| Technical Spec | 1.5x |

## 4. Failure Modes

### 4.1 Deck With One Slide
IDM approaches infinity. Audience suspicious. Probability
of "where are the rest?" approaches 1.0.

### 4.2 No Animations
AOF = 1.0 (optimal). Presenter feels deck is "boring."

### 4.3 Every Bullet Animated
AOF < 0.1. Audience enters trance. DPT collapses to 3.

### 4.4 Post-Conclusion Slide
Hidden slide after apparent end. Trust degrades.
## 5. Security Considerations

### 5.1 Deck Injection
Unauthorized addition drops IDM. Mitigation: slide-level
access control.

### 5.2 Font Escalation
Larger fonts compensate for low IDM, creating an arms
race between font size and slide count.

### 5.3 Clip Art Denial of Service
Excessive clip art eliminates content real estate.

## 6. Performance Evaluation

| Metric | No-SDCA | With SDCA |
|--------|---------|-----------|
| Avg IDM (bits/slide) | 5.2 | 22.0 |
| Avg BPCR | 0.25 | 0.72 |
| Avg AOF | 0.35 | 0.95 |
| DPT Exceeded | 68% | 12% |
| Audience Survival | 45% | 89% |

Optimal deck size: `N_optimal = I_total / 20.0`.
For I_total = 100 bits: 5 slides.

## 7. Extensions

| RFC | Title | Status |
|-----|-------|--------|
| 0011 | Meeting Entropy Acceleration Protocol | DRAFT |
| 0013 | Email-to-Slide Conversion Hazard | PLANNED |

## 8. References

### 8.1 Normative References

[RFC-0011] Matos, R.M. "Meeting Entropy Acceleration Protocol."
RFC 0011, OSC, 2026.

[RFC-0013] Matos, R.M. "Email-to-Slide Conversion Hazard."
RFC 0013, OSC, 2026.

### 8.2 Informative References

Tufte, Edward R. 2003. *The Cognitive Style of PowerPoint*.

Parker, Ian. 2001. "Absolute PowerPoint." *The New Yorker*.

---

> **Colophon**: The Organizational Standards Consortium (OSC)
> does not exist. It is a fictional standards body created for
> the Organizational Epistemology Project (OEP). RFCs published
> under the OSC imprint are satirical artifacts that encode
> genuine organizational science. The slide deck, however, is
> real -- and it could have been a single bullet point.
