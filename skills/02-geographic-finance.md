# Geographic Finance — Domain Skill

## Scope

This skill covers the **spatial dimensions of financial markets**, with a focus on **residential real estate finance**. It bridges real estate economics, financial economics, and economic geography to analyze how financial flows, risk, and institutions interact with place.

## Core Theoretical Frameworks

### House Price Dynamics and Indices
- **Repeat-sales methodology**: Case-Shiller (1987, 1989); Bailey-Muth-Nourse; weighted least squares to account for heteroskedasticity in long intervals.
- **Hedonic indices**: controlling for quality change via characteristics-based regression (Diewert, de Haan & Diewert).
- **Hybrid approaches**: combining repeat-sales and hedonic methods for thin markets.
- **Spatial granularity**: metro-level vs. ZIP-code vs. census-tract indices; smoothing vs. noise trade-off; kriging-based interpolation.
- **Price discovery**: lead-lag between new and existing home prices, between rental and owner-occupied markets.

### Mortgage Markets and Credit Geography
- **Mortgage origination channels**: banks, non-bank lenders, GSEs (Fannie Mae, Freddie Mac, Ginnie Mae), FHA/VA programs.
- **Securitization chain**: loan origination → pooling → tranching → RMBS/CMBS → secondary market. Moral hazard at each node (Keys, Mukherjee, Seru & Vig).
- **Credit rationing and access**: spatial variation in lending standards; LTV, DTI, FICO thresholds; jumbo vs. conforming loan limits.
- **Redlining and lending discrimination**: HMDA data analysis; disparate impact vs. disparate treatment; Community Reinvestment Act (CRA); digital redlining.
- **Spatial credit risk**: geographic concentration of mortgage default; contagion effects; neighborhood foreclosure externalities (Campbell, Giglio & Pathak).


### Housing as a Financial Asset
- **Risk-return profile**: housing vs. equities vs. bonds (Jordà, Knoll, Kuvshinov, Schularick & Taylor, 2019).
- **Leverage and wealth accumulation**: homeownership as leveraged investment; down-payment constraints; wealth inequality amplification.
- **Housing wealth effects**: marginal propensity to consume out of housing wealth (Mian, Rao & Sufi; Aladangady).
- **REITs and institutional investment**: real estate investment trusts; institutional single-family rental (SFR); financialization of housing (Aalbers; Fields).

### Spatial Risk and Pricing
- **Spatial diversification**: geographic portfolio theory applied to real estate (Zietz & Sirmans; Goetzmann & Wachter).
- **Climate and environmental risk pricing**: flood risk capitalization; sea-level rise discounting; wildfire risk; transition risk (Baldauf, Garlappi & Yannelis; Bernstein, Gustafson & Lewis).
- **Insurance markets**: NFIP (National Flood Insurance Program); private flood insurance; spatial moral hazard; adverse selection in hazard zones.
- **Contagion and spatial spillovers**: foreclosure contagion; price discovery spillovers across neighborhoods; spatial momentum.

### Financialization of Housing
- **Aalbers (2016) framework**: subordination of housing to financial logics; housing as vehicle for capital accumulation.
- **Institutional landlords**: private equity in rental markets; build-to-rent; impact on affordability and tenant welfare.
- **Global capital flows**: cross-border real estate investment; safe-haven demand; capital controls and housing prices (Badarinza & Ramadorai; Favilukis & Van Nieuwerburgh).
- **FinTech and PropTech**: algorithmic valuation (AVMs), iBuying, fractional ownership, tokenization.

## Vocabulary Guide

| Term | Meaning |
|---|---|
| LTV (Loan-to-Value) | Ratio of mortgage amount to property appraised value; key underwriting metric |
| DTI (Debt-to-Income) | Ratio of total monthly debt payments to gross monthly income |
| RMBS / CMBS | Residential / Commercial Mortgage-Backed Securities |
| GSE | Government-Sponsored Enterprise (Fannie Mae, Freddie Mac) |
| Conforming loan | Mortgage meeting GSE purchase criteria (size, LTV, documentation) |
| Default risk | Probability of borrower failing to meet mortgage payment obligations |
| Prepayment risk | Risk that borrowers refinance or pay off mortgages early, affecting MBS cash flows |
| Capitalization rate (cap rate) | Net operating income / property value; key metric in commercial and rental valuation |
| AVM | Automated Valuation Model — algorithmic property price estimation |
| Foreclosure externality | Negative spillover of a foreclosed property on neighboring home values |
| HMDA | Home Mortgage Disclosure Act data — loan-level mortgage origination records |
| Spatial arbitrage | Exploiting price differentials across locations, often limited by transaction costs and information asymmetry |
| Financialization | Process by which financial motives, markets, and actors increasingly dominate housing provision |
| Reverse mortgage| A reverse mortgage is a special type of loan that lets older homeowners convert part of their home equity into cash without having to make monthly mortgage payments |

## What to Emphasize in Summaries

1. **Data infrastructure**: What data sources are used? How are house price indices constructed? What are the spatial and temporal granularities?
2. **Financial mechanism**: What is the specific financial channel (credit supply, securitization, insurance, investment flows)?
3. **Spatial dimension**: How does geography mediate the financial mechanism? Is there spatial heterogeneity in effects?
4. **Distributional consequences**: Who bears the risk? How are gains/losses distributed across income, race, gender, and geography?
5. **Regulatory context**: What regulatory framework governs the financial mechanism (CRA, Dodd-Frank, Basel, NFIP)?
6. **Market efficiency**: Does the paper test or assume efficient pricing of spatial characteristics and risks?

## Key Journals

Journal of Finance, Journal of Financial Economics, Review of Financial Studies, Journal of Monetary Economics, Real Estate Economics, Journal of Real Estate Finance and Economics, Journal of Housing Economics, Journal of Financial Intermediation, Journal of Urban Economics, American Economic Review.

## Foundational References

- Case, K.E. & Shiller, R.J. (1989). The efficiency of the market for single-family homes.
- Keys, B.J., Mukherjee, T., Seru, A. & Vig, V. (2010). Did securitization lead to lax screening?
- Mian, A. & Sufi, A. (2009). The consequences of mortgage credit expansion.
- Campbell, J., Giglio, S. & Pathak, P. (2011). Forced sales and house prices.
- Jordà, Ò., Knoll, K., Kuvshinov, D., Schularick, M. & Taylor, A.M. (2019). The rate of return on everything.
- Aalbers, M. (2016). *The Financialization of Housing*.
- Glaeser, E., Gottlieb, J. & Gyourko, J. (2012). Can cheap credit explain the housing boom?
- Bernstein, A., Gustafson, M. & Lewis, R. (2019). Disaster on the horizon.
