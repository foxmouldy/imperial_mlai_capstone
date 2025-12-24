# Model Card: Adaptive Black-Box Optimisation Pipeline (`bb_oxo_dd`) 

## Overview  
- **Type:** Hybrid optimisation framework (Bayesian Optimisation, Optuna/TPE, AutoML, simple NN surrogate)  
- **Version:** v1.0  
- **Description:** `bb_oxo_dd` is a sequential decision-making system that selects inputs to optimise unknown black-box functions under limited query budgets.

## Intended Use  
**Suitable for:** black-box optimisation, hyperparameter tuning, experimental design, noisy or expensive objectives.  
**Not suitable for:** supervised prediction, safety-critical deployment, or fully batch optimisation with complete data.

## Optimisation Strategy  
Over ten rounds, the strategy evolved from **broad exploration** (Bayesian optimisation) to **focused exploitation** (Optuna/TPE), with AutoML and a simple neural-network surrogate 
introduced later to capture higher-dimensional structure. Decisions explicitly balance exploration, exploitation, and robustness to noise.

## Performance  
Evaluated on **eight benchmark functions** of increasing dimensionality.  
- **Metric:** best observed objective value under a fixed query budget  
- **Observation:** strong performance at low–moderate dimensions; diminishing returns and increased variance at higher dimensions.

## Assumptions and Limitations  
**Assumptions:** smooth, queryable objectives with non-adversarial noise.  
**Limitations:** sensitivity to initial sampling, degraded performance in high dimensions, no guarantee of global optimality.

## Ethical Considerations  
Transparent documentation of optimisation choices and assumptions supports reproducibility and discourages inappropriate real-world use. 
The system is intended as a decision aid, not a replacement for expert judgement.

## Reflection  
`bb_oxo_dd`’s strength lies in adaptive decision-making under uncertainty; its weakness emerges in sparse, high-dimensional regimes. 
The current level of documentation is sufficient for clarity and responsible reuse; additional detail would increase complexity without improving interpretability.
