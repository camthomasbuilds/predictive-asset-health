# Predictive Asset Health for Gas Generation

## The Business Problem

A fleet of gas-fired power generation assets relied on time-based and reactive maintenance. Component failures cost $1M+/day at peak. Capital was allocated by OEM schedule, not by actual asset condition. The organization had no systematic way to predict when components would fail or to prioritize investment across hundreds of critical components.

**The strategic question:** How do you connect engineering predictions to capital allocation decisions?

## My Role

Senior Product Manager. Owned product vision, stakeholder alignment across engineering and operations, and delivery of the Weibull failure modeling platform.

## The Key Decisions

### 1. Weibull over deep learning

The instinct was to reach for complex ML. I chose Weibull statistical models instead. Weibull is interpretable, works with sparse failure data, and is already trusted by reliability engineers. The bottleneck wasn't model sophistication. It was stakeholder adoption. Starting with a trusted methodology built the credibility needed to layer on more advanced approaches later.

### 2. Connect predictions to dollars

A probability curve doesn't drive decisions. "This component has a 30% probability of failure in 12 months" is interesting. "This component has a 30% probability of a $2.4M event in 12 months" drives action. I integrated failure predictions directly with the financial impact framework (Total Value), converting engineering outputs into capital allocation inputs.

### 3. Fleet-wide models with site-specific calibration

Individual sites don't have enough failure data to train reliable models. I chose fleet-wide models with site-specific operating condition adjustments, providing both statistical power and local relevance.

### 4. Change management from reactive to condition-based

This product required changing how an entire maintenance organization thinks about risk. For decades, teams operated on OEM schedules and reactive response. Shifting to condition-based, data-driven capital allocation meant redefining how reliability engineers assess equipment, how capital planners justify investments, and how O&M teams prioritize work. I embedded change management into the product strategy: started with the Weibull models engineers already trusted, connected outputs to the financial frameworks planners already used, and designed the system so reliability teams could operate it independently rather than depending on a data science team.

## Results

| Metric | Outcome |
|--------|---------|
| **Coverage** | 70%+ of critical component types |
| **Capital allocation** | Data-driven O&M investment tied to actual risk, not schedule |
| **Financial integration** | Failure probability connected to Total Value framework |
| **Adoption** | Methodology trusted and used independently by reliability engineers |
| **Program value** | $20M+ |

## What This Demonstrates

- **Technical tradeoff judgment** (choosing the right tool over the sophisticated tool)
- **Change management** (shifting an organization from calendar-based to condition-based maintenance)
- **Financial framing** (connecting engineering predictions to capital decisions)
- **Stakeholder-first product design** (building on trusted methodologies to drive adoption)
- **Data product thinking** (provenance, validation, and standardization as first-class concerns)
