---
rfc: "0013"
title: "Jargon Inflation Index"
stream: "Informational"
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
see_also: [12, 14]
keywords: [jargon, inflation, measurement, buzzwords, synergy, leverage, paradigm-shift]
abstract: |
  This RFC defines the Jargon Inflation Index (JII), a satirical yet
  structurally rigorous framework for quantifying the inverse relationship
  between jargon density and organizational clarity. The JII provides four
  composite metrics that, when measured over time, reveal the precise moment
  at which communication collapses into incoherence.
satire_notice: "satire"
dual_layer: true
---

# RFC-0013: Jargon Inflation Index

> *"If you can't explain it plainly, you haven't inflated it enough."*
> — Apocryphal middle-manager, 2019

## 1. Introduction

Organizations communicate. This is a known fact. The *manner* in which they
communicate, however, follows a predictable degradation curve. As pressure
increases, clarity decreases and jargon increases — a phenomenon first
observed informally and now codified here with mathematical precision it
does not deserve.

The Jargon Inflation Index (JII) formalizes this observation into four
measurable quantities. These metrics are intended for use by anyone who has
sat through a meeting and realized they understood fewer words than when
they walked in.

### 1.1. Scope

This specification covers:

- The Jargon Density Score (JDS)
- The Buzzword Repetition Rate (BRR)
- The Clarity Inverse Correlation (CIC)
- The Synergy Saturation Point (SSP)
- Failure modes in jargon-heavy environments

### 1.2. Motivation

No existing RFC addresses the systemic inflation of organizational language.
RFC-0012 addresses epistemological debt. RFC-0014 addresses informal
network decay. The JII bridges them: debt accumulates *through* inflated
language, and networks decay *because of* it.

## 2. Terminology

| Term | Definition |
|------|-----------|
| Jargon Token | Any word or phrase that would confuse a competent outsider |
| Synergy Word | A jargon token with no concrete referent |
| Buzzword | A jargon token repeated beyond its informational value |
| Clarity Score | Subjective comprehension rating (0-10) from a naive reader |
| Reference Corpus | A body of text assumed to be clear (e.g., a README) |
| Saturation Event | The moment jargon density crosses the comprehension threshold |
| Organizational Glossary | A document nobody reads that defines jargon nobody uses |

## 3. Protocol Specification

### 3.1. Jargon Density Score (JDS)

The JDS measures jargon tokens per 1000 tokens of text.

```
JDS = (jargon_token_count / total_token_count) * 1000
```

Classification thresholds:

```
JDS <  10  : Clear          (suspicious)
JDS 10-30  : Normal         (organizational baseline)
JDS 30-60  : Dense          (meeting territory)
JDS > 60   : Incomprehensible (reached the singularity)
```

### 3.2. Buzzword Repetition Rate (BRR)

The BRR measures how often the same buzzwords recur, indicating a
vocabulary under duress.

```
BRR = unique_buzzword_count / total_jargon_token_count
```

A BRR near 1.0 means the speaker knows many jargon terms (dangerous but
diverse). A BRR near 0.0 means they repeat the same few words
(precisely the scenario this index was designed to capture).

Classification thresholds:

```
BRR > 0.7  : Diverse jargon   (wide vocabulary, shallow depth)
BRR 0.3-0.7: Moderate reuse   (the standard corporate palette)
BRR < 0.3  : Extreme reuse    (the "synergy-ecosystem" cycle)
```

### 3.3. Clarity Inverse Correlation (CIC)

The CIC quantifies the relationship between jargon density and
comprehension. It requires human evaluation on the Reference Corpus.

```
CIC = correlation(JDS, 1/clarity_score)
```

Interpretation:

```
CIC >  0.8  : Strong inverse (more jargon = less clarity, as expected)
CIC 0.4-0.8 : Moderate       (some phrases are meaningful)
CIC <  0.4  : Anomaly        (jargon that is somehow clear — investigate)
```

### 3.4. Synergy Saturation Point (SSP)

The SSP identifies the jargon density at which a naive reader fails to
extract the core message of a document. It is measured, not computed.

```
SSP = min(JDS) where clarity_score < 3.0
```

When SSP is reached, the document has achieved what the author likely
intended: total opacity. In practice, SSP tends to cluster around
JDS = 45 for standard business prose, and JDS = 75 for management
consulting decks.

## 4. Failure Modes

| Failure Mode | Description | Mitigation |
|-------------|-------------|-----------|
| Glossary Inflation | Defining jargon with more jargon | Enforce plain-language glossaries |
| Metric Gaming | Optimizing JDS without reducing jargon | Rotate evaluation panels |
| BRR Collapse | Reducing all communication to three buzzwords | Require structural variety |
| SSP Denial | Refusing to acknowledge saturation | Anonymous reader feedback |
| CIC Null | Failing to test with naive readers | Mandate external review |

## 5. Security Considerations

Jargon inflation can be weaponized. Deliberately opaque communication
creates information asymmetry between insiders and outsiders. This enables:

- Gatekeeping via vocabulary control
- Obfuscation of poor decision-making
- Exclusion of non-native speakers

The JII is a defense against these patterns. Measuring them is the first
step toward dismantling them.

## 6. Performance Evaluation

In controlled tests across five organizations:

```
Org     | Avg JDS | Avg BRR | Avg CIC | SSP
--------|---------|---------|---------|----
Corp A  |   38    |  0.34   |  0.87   | 42
Corp B  |   61    |  0.22   |  0.91   | 48
Startup |   12    |  0.65   |  0.43   | N/A
NGO     |   27    |  0.41   |  0.72   | 51
Govt    |   55    |  0.28   |  0.89   | 44
```

Startup CIC is low because their jargon is technical and therefore
somewhat clear to their target audience. Government SSP is high because
their readers are accustomed to opacity.

## 7. Extensions

| Extension | Description | Status |
|-----------|-------------|--------|
| JII-Streaming | Real-time JDS monitoring in video calls | Proposed |
| JII-Lexicon | Auto-updating jargon dictionary per domain | Draft |
| JII-Feedback | Inline jargon density alerts in editors | Experimental |
| JII-Historical | Longitudinal jargon inflation tracking | Proposed |
| JII-CrossLang | JII adaptation for non-English languages | Future |

## 8. References

- [RFC-0012] Epistemological Debt: Accumulation and Recognition
- [RFC-0014] Informal Network Decay Patterns
- [RFC-0001] Organizational Epistemology Project Charter
- Orwell, G. "Politics and the English Language" (1946)
- The Dilbert Principles, Scott Adams (1996)

## 9. Colophon

This RFC was written in plain language on purpose. The irony of writing a
jargon RFC in clear prose is noted and intentional. If you found any
synergy words in this document, please open an issue.

---

*RFC-0013 | OEP | Status: DRAFT | 2026-07-18*
