# Case Study: Predictive Asset Health for Gas Generation

## Context

A fleet of gas-fired power generation assets relied on time-based and reactive maintenance strategies. Component failures were expensive (forced outage costs of $1M+/day at peak), but the organization lacked a systematic way to predict when components would fail or to prioritize capital allocation across hundreds of critical components.

## My Role

Senior Product Manager: responsible for defining the product vision for a predictive asset health capability, aligning engineering and operations stakeholders, and driving delivery of the initial Weibull failure modeling platform.

## Problem Framing

**Operational reality:**
- Maintenance decisions were based on OEM recommendations (time-based) or reactive response (run-to-failure)
- No fleet-wide visibility into component degradation rates or remaining useful life
- Capital planning was disconnected from actual asset condition: investments were allocated by schedule, not by risk
- Critical OEM documentation and failure history were scattered across disconnected systems

**Product opportunity:** Build a predictive asset health capability that uses statistical failure modeling to forecast component end-of-life, enabling condition-based maintenance scheduling and risk-weighted capital allocation.

## Product Strategy

I structured the product around three capabilities:

1. **Failure prediction**: Weibull distribution models fitted to component failure history, producing probability-of-failure curves over time
2. **Asset risk quantification**: Combining failure probability with consequence (repair cost, outage impact, safety risk) to produce a single risk score per component
3. **OEM intelligence repository**: Centralized, searchable repository of OEM documentation to support execution-level maintenance decisions

## Key Decisions

### Weibull over ML-first approach
- **Decision:** Start with well-understood statistical models (Weibull distributions) rather than jumping to complex ML
- **Rationale:** Weibull models are interpretable, require less training data, and are trusted by reliability engineers. They provide a credible foundation that ML can enhance later (anomaly detection layered on top of baseline Weibull predictions).

### Total Value integration
- **Decision:** Connect failure predictions directly to financial impact models (Fossil Total Value)
- **Rationale:** Telling an operations team "this component has a 30% probability of failure in 12 months" is useful. Telling them "this component has a 30% probability of a $2.4M event in 12 months" drives action.

### Fleet-wide vs. site-specific
- **Decision:** Build models that generalize across the fleet, with site-specific calibration
- **Rationale:** Individual sites don't have enough failure data to train reliable models. Fleet-wide models with site-specific operating condition adjustments provide both statistical power and local relevance.

## Results

- Expanded predictive coverage to 70%+ of critical component types
- Enabled data-driven O&M capital allocation tied to actual risk rather than schedule
- Improved Total Value decision-making by integrating failure probability with financial models
- Established a repeatable methodology that reliability engineers trust and use independently

## Lessons Learned

1. **Start with the model users trust**: Reliability engineers already knew Weibull. Starting there built credibility. Trying to introduce a black-box ML model first would have faced organizational resistance.

2. **Connect predictions to dollars**: A probability curve alone doesn't drive decisions. Connecting it to financial impact (cost of failure, value of prevention) makes the output actionable for capital planners.

3. **Data quality is the real bottleneck**: The modeling itself is straightforward. Getting consistent, clean failure history across a multi-decade fleet is the actual hard problem. I spent more time on data product design (provenance, validation, standardization) than on model selection.
