# Methodology — Domain Skill

## Scope

This skill provides the **methodological vocabulary and evaluation criteria** for assessing the empirical strategies used in residential real estate research across all four domains. It ensures that summaries correctly describe statistical methods, identification strategies, and data sources, and that methodological strengths and weaknesses are properly noted.

## Causal Inference Toolkit

### Difference-in-Differences (DID)
- **Logic**: Compare treatment and control groups before and after an intervention; the "parallel trends" assumption.
- **Variants**: staggered adoption DID (Callaway & Sant'Anna, 2021; Sun & Abraham, 2021; de Chaisemartin & D'Haultfoeuille); event study plots; heterogeneity-robust estimators.
- **Housing applications**: policy changes (rent control introduction, zoning reform, tax credit programs), place-based treatments (transit line opening, Superfund cleanup, Opportunity Zone designation).
- **Red flags**: no pre-trends test, composition changes in treated/control areas, anticipation effects, contamination of control group.

### Instrumental Variables (IV)
- **Logic**: use an exogenous variable (instrument) correlated with the endogenous regressor but uncorrelated with the error term.
- **Common instruments in housing**: Saiz (2010) topographic/regulatory constraints for supply; Bartik (1991) shift-share for labor demand; historical variables (railroad placement, immigrant enclaves, redlining maps).
- **Diagnostics**: first-stage F-statistic (Staiger & Stock rule of thumb: F > 10; modern: effective F from Olea & Pflueger), over-identification tests, exclusion restriction plausibility arguments.
- **Red flags**: weak instruments, questionable exclusion restriction, LATE interpretation vs. ATE.

### Regression Discontinuity Design (RDD)
- **Logic**: exploit a threshold/cutoff that creates quasi-random assignment.
- **Housing applications**: school attendance zone boundaries, municipal tax jurisdiction boundaries, flood zone boundaries (FEMA), historic district boundaries, income cutoffs for subsidies.
- **Variants**: sharp vs. fuzzy RDD; spatial RDD (Dell, 2010; Keele & Titiunik, 2015) — discontinuity at a geographic boundary.
- **Diagnostics**: McCrary density test, bandwidth sensitivity, covariate balance at the cutoff, donut-hole tests.

### Synthetic Control Method (SCM)
- **Logic**: construct a weighted combination of untreated units to serve as counterfactual for a treated unit.
- **Housing applications**: city-level policy evaluations (rent control, inclusionary zoning), regional shocks.
- **Extensions**: augmented SCM (Ben-Michael, Feller & Rothstein); SCM with multiple treated units; permutation-based inference.

### Panel Data Methods
- **Fixed effects**: entity (property, household, neighborhood, city) and time fixed effects to absorb unobserved heterogeneity.
- **Within-estimator**: exploits variation over time within units; eliminates time-invariant confounders.
- **Correlated random effects**: Mundlak/Chamberlain device.
- **Dynamic panels**: Arellano-Bond GMM for short-T, large-N panels with lagged dependent variable.

### Hedonic and Structural Estimation
- **Hedonic first stage**: log-linear, semi-log, Box-Cox transformations; spatial fixed effects (tract, block group); temporal controls.
- **Second stage / structural recovery**: BLP-style demand estimation; Epple-Sieg sorting models; two-step estimation with generated regressors.
- **Machine learning hedonics**: LASSO, random forest, gradient boosting for flexible functional form; out-of-sample prediction vs. coefficient interpretation trade-off.

## Spatial Econometrics

### Core Models
- **SAR (Spatial Autoregressive / Spatial Lag)**: y = ρWy + Xβ + ε. Endogenous spatial lag; feedback effects.
- **SEM (Spatial Error Model)**: y = Xβ + u, u = λWu + ε. Spatial dependence in disturbances; no substantive spatial spillover.
- **SDM (Spatial Durbin Model)**: y = ρWy + Xβ + WXθ + ε. Includes spatial lags of both dependent and independent variables. LeSage & Pace (2009) argue this should be the default.
- **SLX (Spatial Lag of X)**: y = Xβ + WXθ + ε. Local spillovers without feedback.
- **GWR (Geographically Weighted Regression)**: locally estimated coefficients; captures spatial non-stationarity; Fotheringham, Brunsdon & Charlton (2002).
- **MGWR (Multiscale GWR)**: allows bandwidth to vary by covariate; Fotheringham, Yang & Kang (2017).

### Spatial Weights
- **Contiguity**: queen, rook (for polygon data).
- **Distance-based**: inverse distance, distance band, k-nearest neighbors.
- **Economic/social weights**: based on trade flows, migration, similarity in industrial structure.
- **Sensitivity**: results should be tested across multiple weight specifications.

### Diagnostics
- **Moran's I test** on OLS residuals: is spatial dependence present?
- **Lagrange Multiplier tests**: LM-lag vs. LM-error; robust versions to discriminate between SAR and SEM.
- **Direct, indirect, and total effects**: proper interpretation of SAR/SDM coefficients requires computing marginal effects (LeSage & Pace, 2009).
- **LISA**

## Machine Learning and Computational Methods

- **Prediction tasks**: AVM (automated valuation models), price forecasting, default prediction.
- **Feature importance**: SHAP values, permutation importance for understanding which characteristics drive predictions.
- **Causal ML**: causal forests (Athey & Imbens), double/debiased machine learning (Chernozhukov et al.), LASSO for high-dimensional controls.
- **Spatial ML**: spatial cross-validation (blocking by geography to avoid data leakage); spatial feature engineering.
- **Text and image data**: NLP on listing descriptions; computer vision on property photos or satellite imagery; multimodal models.

## Qualitative and Mixed Methods

- **Case studies**: single or comparative case design; process tracing; within-case analysis.
- **Interviews**: semi-structured, in-depth; purposive or snowball sampling; saturation.
- **Ethnography**: participant observation; thick description; extended engagement with place.
- **Discourse analysis**: how housing and neighborhoods are framed in policy documents, media, real estate marketing.
- **Mixed methods designs**: sequential explanatory (quant → qual), sequential exploratory (qual → quant), concurrent triangulation.
- **Evaluation criteria**: trustworthiness (credibility, transferability, dependability, confirmability) rather than validity/reliability.

## Data Sources Commonly Used

| Data Source | Coverage | Key Variables |
|---|---|---|
| **Census / ACS** (US) or equivalent national census | National, decennial / annual | Demographics, income, housing characteristics, tenure |
| **HMDA** | US, annual | Mortgage originations, denial rates, lender, borrower race/income |
| **MLS / Transaction registers** | Local/metro, continuous | Sale prices, listing prices, days on market, property characteristics |
| **Cadastral / tax assessor** | Local, annual | Assessed values, lot size, building characteristics, ownership |
| **CoreLogic / Zillow / Redfin** | US, proprietary | Transaction prices, AVMs, rental listings, market indices |
| **FHFA / Case-Shiller** | US metro, quarterly/monthly | Repeat-sales house price indices |
| **OpenStreetMap / Google Maps** | Global, continuous | POIs, road networks, amenity mapping |
| **Satellite imagery** | Global, variable resolution | Land cover, building footprints, urban expansion, vegetation |
| **Mobile phone / GPS** | Variable, proprietary | Mobility patterns, activity spaces, commuting, experienced segregation |

## What to Emphasize in Summaries

1. **Name the method precisely**: "the authors use a spatial Durbin model with queen contiguity weights" — not "they run a regression."
2. **Evaluate identification**: Is the causal claim credible? What are the key threats?
3. **Note the estimand**: ATE, ATT, LATE, or local marginal effect? Is the paper clear about what it identifies?
4. **Data quality**: Sample size, spatial coverage, temporal span, potential selection into the sample, measurement error.
5. **Replicability**: Are data and code available? Is the method described in sufficient detail to replicate?
6. **Spatial considerations**: Is spatial dependence in the data addressed or ignored? If ignored, is this a problem?
