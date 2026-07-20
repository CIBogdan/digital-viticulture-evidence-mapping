# Digital Viticulture Evidence Mapping

A reproducible Python workflow for PRISMA-guided screening, weighted
thematic classification and cross-domain evidence mapping in digital
and precision viticulture.

The workflow was developed for the systematic review:

**Integrated Digital Ecosystems for Precision Viticulture: A Systematic
Review of Multisource Sensing, AI-Based Modelling and Decision-Support
Systems**

## Overview

The notebook implements a semi-automated evidence-mapping procedure for
identifying and prioritizing publications relevant to digital and
precision viticulture.

Titles and abstracts are screened and scored using weighted vocabularies
representing four complementary technological domains:

1. Artificial Intelligence and Machine Learning
2. Sensor and Spectral Technologies
3. Digital and Precision Viticulture
4. Digital Technologies and Decision Support

For each domain, the 40 highest-scoring records meeting the minimum
relevance threshold are retained. Cross-domain overlap is quantified
using unique Web of Science identifiers, and duplicate assignments are
resolved according to the strongest thematic score.

## Workflow

```mermaid
flowchart LR
    A["Web of Science records"] --> B["PRISMA-guided screening"]
    B --> C["Include records"]
    C --> D["Weighted classification"]
    D --> E["Top 40 per domain"]
    E --> F["160 category assignments"]
    F --> G["Cross-domain overlap"]
    G --> H["WoS-based deduplication"]
    H --> I["Evidence base for full-text evaluation"]
```