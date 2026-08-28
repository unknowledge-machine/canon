---
rfc: "0027"
title: "Cognitive Bias Quantification Protocol (CBQP)"
stream: "Humor"
status: "DRAFT"
category: "Informational"
area: "epistemology"
authors:
  - name: "Rodolfo Matos"
    org: "Organizational Standards Consortium (OSC)"
    email: "rm@osc.org"
created: "2026-07-19"
updated: "2026-07-19"
obsoletes: []
obsoleted_by: []
see_also: [1, 4, 5, 10, 17, 23, 24, 25, 26]
keywords: [cognitive-bias, dunning-kruger, false-consensus,
  telepathy-demand, bias-quotient, epistemic-distortion]
abstract: |
  This document specifies the Cognitive Bias Quantification Protocol (CBQP),
  a framework for measuring the systematic epistemic distortions introduced
  by cognitive biases in organizational decision-making. CBQP introduces the
  Cognitive Bias Quotient (CBQ) — a standardized metric alongside IQ and EQ —
  and decomposes it into the Dunning-Kruger Coefficient (DKC), False Consensus
  Index (FCI), Telepathy Demand Index (TDI), and Bias-Competence Inverse
  Correlation (BCIC). Organizations with CBQ > 0.7 experience accelerated
  epistemic fragmentation (RFC-0003), knowledge gravity distortion (RFC-0005),
  and succession entropy (RFC-0025). While framed as a measurement protocol,
  CBQP functions analytically as a diagnostic instrument for organizational
  epistemic health.
dual_layer: true
satire_notice: "satire"
---

# RFC-0027 — Cognitive Bias Quantification Protocol (CBQP)

## Abstract

This document specifies the Cognitive Bias Quantification Protocol (CBQP),
a framework for measuring the systematic epistemic distortions introduced
by cognitive biases in organizational decision-making. CBQP introduces the
Cognitive Bias Quotient (CBQ) — a standardized metric alongside IQ and EQ —
and decomposes it into the Dunning-Kruger Coefficient (DKC), False Consensus
Index (FCI), Telepathy Demand Index (TDI), and Bias-Competence Inverse
Correlation (BCIC). Organizations with CBQ > 0.7 experience accelerated
epistemic fragmentation (RFC-0003), knowledge gravity distortion (RFC-0005),
and succession entropy (RFC-0025). While framed as a measurement protocol,
CBQP functions analytically as a diagnostic instrument for organizational
epistemic health.

> **Satire Notice**: This document is published in the **Humor** stream.
> While technically coherent, its primary purpose is satirical illumination
> of organizational dynamics. The OSC does not recommend deploying CBQP
> in production without IRB approval and a very large mirror.

## 1. Introduction

Organizations assume that decision-makers are rational agents who process
information objectively. Cognitive psychology has demonstrated that this
assumption is systematically false. Kahneman and Tversky (1979) established
that humans use heuristics that produce predictable errors. Kruger and
Dunning (1999) demonstrated that incompetence prevents recognition of
incompetence. Ross et al. (1977) showed that people overestimate the
extent to which others share their beliefs.

The Cognitive Bias Quantification Protocol (CBQP) makes these distortions
measurable. By quantifying the epistemic cost of cognitive biases, CBQP
transforms a psychological observation into a tractable organizational
metric: the Cognitive Bias Quotient (CBQ).

## 2. Terminology

| Term | Definition |
|------|------------|
| **Cognitive Bias Quotient (CBQ)** | Standardized metric [0,1] quantifying aggregate epistemic distortion from cognitive biases |
| **Dunning-Kruger Coefficient (DKC)** | Gap between self-assessed competence and peer-assessed competence |
| **False Consensus Index (FCI)** | Overestimation of agreement between self and others |
| **Telepathy Demand Index (TDI)** | Subordinate effort required to infer unstated intent |
| **Bias-Competence Inverse Correlation (BCIC)** | Negative correlation between bias magnitude and actual competence |
| **Bias Amplification Factor (BAF)** | Multiplier on epistemic distortion under stress/uncertainty |
| **Illusion of Explanatory Depth (IOED)** | Overconfidence in understanding complex systems |

## 3. Protocol Specification

### 3.1 Cognitive Bias Quotient (CBQ)

**Requirement 1**: Organizations MUST compute CBQ quarterly as:

```
CBQ = ω₁·DKC + ω₂·FCI + ω₃·TDI + ω₄·BCIC
```

Where weights default to: ω₁=0.3, ω₂=0.25, ω₃=0.25, ω₄=0.2 (sum=1).

**Requirement 2**: CBQ interpretation thresholds:

| CBQ Range | Classification | Action |
|-----------|----------------|--------|
| CBQ ≤ 0.2 | **Clear** | Minimal bias distortion; routine monitoring |
| 0.2 < CBQ ≤ 0.4 | **Hazy** | Emerging bias; targeted debiasing |
| 0.4 < CBQ ≤ 0.6 | **Foggy** | Significant distortion; mandatory intervention |
| 0.6 < CBQ ≤ 0.8 | **Opaque** | Systemic bias; leadership restructuring |
| CBQ > 0.8 | **Black Hole** | Epistemic collapse; external intervention |

### 3.2 Dunning-Kruger Coefficient (DKC)

**Requirement 3**: DKC MUST be computed as the normalized gap between
self-assessed and peer-assessed competence:

```
DKC = max(0, (Self_Assessment - Peer_Assessment) / Scale_Max)
```

Where:
- **Self_Assessment**: Quarterly self-rating on domain competence (1–10)
- **Peer_Assessment**: Median peer rating on same domain (1–10)
- **Scale_Max**: Maximum scale value (10)

**Requirement 3.1**: DKC interpretation:

| DKC Range | Classification |
|-----------|----------------|
| DKC = 0 | Accurate self-assessment |
| 0 < DKC ≤ 0.2 | Mild overconfidence |
| 0.2 < DKC ≤ 0.4 | Moderate Dunning-Kruger |
| 0.4 < DKC ≤ 0.6 | Severe Dunning-Kruger |
| DKC > 0.6 | Peak Mount Stupid |

**Requirement 3.2**: DKC MUST be computed per domain (technical, strategic,
interpersonal, financial). Aggregate DKC = mean across domains.

### 3.3 False Consensus Index (FCI)

**Requirement 4**: FCI MUST measure the gap between estimated and actual
agreement:

```
FCI = |Estimated_Agreement - Actual_Agreement|
```

Where:
- **Estimated_Agreement**: Self-reported "What % of colleagues agree with me?" (0–1)
- **Actual_Agreement**: Measured via anonymous survey on same decisions

**Requirement 4.1**: FCI interpretation:

| FCI Range | Classification |
|-----------|----------------|
| FCI ≤ 0.1 | Realistic |
| 0.1 < FCI ≤ 0.3 | Optimistic |
| 0.3 < FCI ≤ 0.5 | False Consensus |
| FCI > 0.5 | Solipsistic |

### 3.4 Telepathy Demand Index (TDI)

**Requirement 5**: TDI MUST quantify the cognitive load on subordinates
required to infer unstated managerial intent:

```
TDI = (Unstated_Expectations × Ambiguity × Urgency) / Explicit_Guidance
```

Where:
- **Unstated_Expectations**: Count of deliverables not in written requirements
- **Ambiguity**: 1–5 scale from "crystal clear" to "read the room"
- **Urgency**: 1–5 scale from "when you can" to "needed yesterday"
- **Explicit_Guidance**: 1–5 scale from "detailed spec" to "figure it out"

**Requirement 5.1**: TDI interpretation:

| TDI Range | Classification | Subordinate Experience |
|-----------|----------------|------------------------|
| TDI ≤ 2 | **Low** | Clear expectations |
| 2 < TDI ≤ 5 | **Moderate** | Occasional mind-reading |
| 5 < TDI ≤ 10 | **High** | Daily telepathy required |
| 10 < TDI ≤ 20 | **Critical** | Full-time telepath |
| TDI > 20 | **Impossible** | Burnout inevitable |

**Requirement 5.2**: TDI MUST be measured per manager-subordinate pair
and aggregated (median) per manager.

### 3.5 Bias-Competence Inverse Correlation (BCIC)

**Requirement 6**: BCIC MUST measure the negative correlation between
bias magnitude and actual competence:

```
BCIC = -Corr(Bias_Score, Competence_Score)
```

Where:
- **Bias_Score**: Composite of DKC, FCI, TDI for the individual
- **Competence_Score**: Peer-assessed + outcome-based competence metric

**Requirement 6.1**: BCIC interpretation:

| BCIC Range | Classification |
|------------|----------------|
| BCIC < 0.1 | No correlation (biases distributed randomly) |
| 0.1 ≤ BCIC < 0.3 | Weak inverse correlation |
| 0.3 ≤ BCIC < 0.5 | Moderate inverse correlation |
| BCIC ≥ 0.5 | Strong inverse correlation (incompetent = most biased) |

**Requirement 6.2**: BCIC MUST be computed at team level and reported
quarterly. BCIC > 0.5 triggers mandatory leadership review.

### 3.6 Bias Amplification Factor (BAF)

**Requirement 7**: BAF MUST measure how stress/uncertainty amplifies
base biases:

```
BAF = 1 + Σ(Stress_Factor_i × Weight_i)
```

Where Stress_Factors include:
- Organizational change (0–0.5)
- Resource scarcity (0–0.3)
- Deadline pressure (0–0.4)
- Ambiguity (0–0.3)
- Visibility/Accountability (0–0.2)

Maximum BAF = 2.7 (all factors maxed).

### 3.7 Composite: Effective Cognitive Bias Quotient (ECBQ)

**Requirement 8**: Organizations MUST report ECBQ under stress:

```
ECBQ = CBQ × BAF
```

ECBQ interpretation uses CBQ thresholds but reflects stress conditions.

## 4. Protocol Mechanics

### 4.1 Measurement Cadence

| Metric | Frequency | Method |
|--------|-----------|--------|
| DKC | Quarterly | Self + peer survey |
| FCI | Quarterly | Decision survey |
| TDI | Monthly | Subordinate pulse survey |
| BCIC | Quarterly | Correlation analysis |
| BAF | Event-driven | Stress event logging |

### 4.2 Survey Instruments

**Requirement 9**: Organizations MUST use validated instruments:

| Bias | Instrument | Source |
|------|------------|--------|
| DKC | Self vs Peer Competence Gap | Adapted from Kruger & Dunning (1999) |
| FCI | Estimated vs Actual Agreement | Adapted from Ross et al. (1977) |
| TDI | Subordinate Telepathy Load | Novel — OEP original |
| BCIC | Bias-Competence Correlation | OEP original |

### 4.3 CBP Integration

**Requirement 10**: Coffee-Break Protocol (RFC-0017) sessions MUST be
explicitly excluded from bias measurement. CBP is the **debiasing
channel** — informal weak-tie synchronization intrinsically reduces DKC, FCI,
and TDI through exposure to diverse perspectives.

## 5. Failure Modes

### 5.1 Bias Blind Spot
Individuals recognize biases in others but not themselves.
**Detection**: DKC_self < DKC_peer for same individual.
**Mitigation**: Third-party assessment; RFC-0010 panel.

### 5.2 Debiasing Theater
Organizations "implement" debiasing training without structural change.
**Detection**: CBQ stable post-training; BAF unchanged.
**Mitigation**: Structural incentives (RFC-0009, RFC-0023).

### 5.3 Telepathy Normalization
High TDI becomes cultural norm ("that's how it works here").
**Detection**: Median TDI > 5 for > 2 quarters.
**Mitigation**: Explicit guidance mandate; RFC-0023 Promotion Gate.

### 5.4 Bias Gamification
Individuals optimize survey responses to lower CBQ.
**Detection**: DKC + FCI + TDI components diverge; BAF spikes.
**Mitigation**: Weight behavioral traces (α=0.6) over self-report.

## 6. Integration with OEP Canon

### 6.1 Cross-RFC Effects

| RFC | CBQP Interaction |
|-----|------------------|
| RFC-0001 (HOP) | DKC inflates ECI; TDI increases Directive Latency |
| RFC-0003 (EFMP) | FCI inflates False Consensus → higher FI |
| RFC-0005 (KGMF) | DKC creates false gravity wells |
| RFC-0007 (OAPP) | TDI accelerates Knowledge Half-Life decay |
| RFC-0009 (KHIS) | DKC mimics hoarding behavior |
| RFC-0010 (EIRP) | DKC correlates with epistemic injustice perpetration |
| RFC-0017 (CBP) | CBP reduces all CBQP components (debiasing) |
| RFC-0023 (PGP) | DKC blocks Promotion Gate |
| RFC-0024 (TIP) | TDI measures Trench Intelligence demand |
| RFC-0025 (SEP) | DKC accelerates Succession Entropy |

### 6.2 Theorem Connections

- **Theorem-001 (CMT)**: CBP weak ties are primary debiasing mechanism
- **Theorem-002 (CET)**: Committee entropy increases with median DKC
- **Theorem-003 (KGT)**: DKC distorts Knowledge Gravity measurement
- **Theorem-004 (EFB)**: FCI directly increases Fragmentation Index
- **Theorem-005 (TKIT)**: TDI formalizes the inexpressibility of intent

## 7. Security & Privacy

### 7.1 Epistemic Security
CBQ reveals:
- Which leaders are most epistemically distorted
- Which teams suffer highest telepathy demand
- Where bias-induced decisions create risk

**Requirement 11**: CBQ data classified at same level as performance reviews.
Access: measured individual, direct manager, independent auditor.

### 7.2 Individual Privacy
**Requirement 12**: Aggregation to role level (min 5) before reporting.
Individual CBQ PROHIBITED in dashboards.

### 7.3 CBP Integrity
**Requirement 13**: CBP attendance/participation MUST NOT feed CBQP.
CBP is the antidote, not the measurement.

## 8. Performance Evaluation

| Metric | No-CBQP | With CBQP |
|--------|---------|-----------|
| Avg CBQ | 0.68 | 0.35 |
| Median TDI | 12.4 | 3.2 |
| Decision Rework Rate | 34% | 12% |
| Subordinate Burnout | 41% | 18% |
| Promotion Reversal Rate | 23% | 5% |

## 9. Extensions

| RFC | Title | Status |
|-----|-------|--------|
| 0028 | Bias Debiasing Protocol (BDP) | Planned |
| 0029 | Organizational Rationality Certification | Planned |
| 0030 | AI Bias Amplification Protocol | Planned |

## 10. References

### 10.1 Normative References

[RFC-0001] Matos, R. "Hierarchical Omniscience Protocol (HOP)." RFC 0001.
[RFC-0003] Matos, R. "Epistemic Fragmentation Monitoring Protocol." RFC 0003.
[RFC-0005] Matos, R. "Knowledge Gravity Measurement Framework." RFC 0005.
[RFC-0007] Matos, R.M. "Organizational Amnesia Prevention Protocol." RFC 0007.
[RFC-0009] Matos, R.M. "Knowledge Hoarding Incentive Structure." RFC 0009.
[RFC-0010] Matos, R.M. "Epistemic Injustice Remediation Protocol." RFC 0010.
[RFC-0017] Matos, R. "Coffee-Break Protocol (CBP)." RFC 0017.
[RFC-0023] Matos, R. "Promotion Gate Protocol (PGP)." RFC 0023.
[RFC-0024] Matos, R. "Trench Intelligence Protocol (TIP)." RFC 0024.
[RFC-0025] Matos, R. "Succession Entropy Protocol (SEP)." RFC 0025.
[RFC-0026] Matos, R. "Wernham Hogg Protocol (WHP)." RFC 0026.

### 10.2 Informative References

Kahneman, D., and Tversky, A. 1979. "Prospect Theory: An Analysis of Decision
under Risk." *Econometrica* 47 (2): 263–291.

Kruger, J., and Dunning, D. 1999. "Unskilled and Unaware of It: How Difficulties
in Recognizing One's Own Incompetence Lead to Inflated Self-Assessments."
*Journal of Personality and Social Psychology* 77 (6): 1121–1134.

Ross, L., Greene, D., and House, P. 1977. "The 'False Consensus Effect': An
Egocentric Bias in Social Perception and Attribution Processes." *Journal of
Experimental Social Psychology* 13 (3): 279–301.

Tversky, A., and Kahneman, D. 1974. "Judgment under Uncertainty: Heuristics
and Biases." *Science* 185 (4157): 1124–1131.

---

## Appendix A: Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-07-19 | R. Matos | Initial draft |

## Appendix B: Open Issues

1. **CBQ Calibration**: Cross-cultural validation of thresholds needed.
   [UNVERIFIED]
2. **TDI Measurement**: Subordinate pulse surveys may induce survey fatigue.
   [UNVERIFIED]
3. **BCIC Causality**: Does bias reduce competence, or does low competence
   enable bias? Longitudinal study needed. [UNVERIFIED]
4. **Remote TDI**: Slack/Teams ambiguity increases TDI; platform-specific
   calibration needed. [UNVERIFIED]
5. **AI Bias**: LLMs in decision support may amplify or reduce human biases.
   [UNVERIFIED]

---

> **Colophon**: The Organizational Standards Consortium (OSC) does not exist.
> It is a fictional standards body created for the Organizational Epistemology
> Project (OEP). RFCs published under the OSC imprint are satirical artifacts
> that encode genuine organizational science. All citations of real scholars
> (Kahneman, Tversky, Kruger, Dunning, Ross, etc.) are accurate. The bias,
> however, is real — and you are currently underestimating your own CBQ.