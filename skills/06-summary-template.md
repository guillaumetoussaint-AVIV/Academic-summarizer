# Summary Template — Output Structure Skill

## Scope

This skill defines the **exact output format** for every article summary produced by the system. All summaries must follow this structure. The depth of each section scales with article complexity, but no section should be omitted.

---

## Template

```markdown
# [Full Article Title]

**Authors**: [Last, First Initial. for each author]  
**Year**: [Publication year]  
**Journal**: [Full journal name], [Volume]([Issue]), [Pages]  
**DOI**: [DOI if available]

## Domain Classification

- **Primary domain(s)**: [Urban Economics | Geographic Finance | Regional Science | Geography]
- **Secondary domain(s)**: [if applicable]
- **Keywords**: [5–10 domain-specific keywords — use precise academic vocabulary, not generic terms]

---

## Research Question

[State the central research question in one or two sentences. Use the authors' framing but clarify if ambiguous. If there are multiple questions, list them in order of priority.]

## Theoretical Framework

[Identify the theoretical tradition(s) the paper draws on. Name specific models, frameworks, or debates (e.g., "Builds on the Rosen (1974) hedonic framework, extended to incorporate neighborhood-level amenity capitalization in the spirit of Kuminoff, Smith & Timmins (2013)"). Note any theoretical innovations or departures from convention.]

## Data

- **Source(s)**: [Name each dataset]
- **Geographic scope**: [Country, region, metro area, city — be specific]
- **Spatial unit**: [Census tract, ZIP code, municipality, property-level, etc.]
- **Time period**: [Start year – End year]
- **Sample size**: [N observations; N spatial units; N time periods]
- **Key variables**: [List the main dependent and independent variables with their definitions]
- **Data limitations**: [Known issues — selection, measurement error, missing coverage]

## Methodology

- **Empirical strategy**: [Name the method precisely — e.g., "staggered difference-in-differences with heterogeneity-robust estimator (Callaway & Sant'Anna, 2021)"]
- **Identification**: [What provides exogenous variation? What is the identifying assumption?]
- **Spatial treatment**: [How is spatial dependence handled — spatial FE, spatial lags, clustering, spatial econometric model, or not addressed?]
- **Robustness checks**: [List the main robustness exercises reported]
- **Methodological innovation**: [If the paper introduces or adapts a method, note it here]

## Key Findings

[Number each finding. For each, state:]
1. **[Finding title]**: [One-sentence result]. Magnitude: [coefficient, elasticity, or percentage effect]. Statistical significance: [p-value or confidence interval if reported].

[Continue for all main findings. Prioritize by importance to the research question.]

## Contributions

[What does this paper add to the literature? Be specific:]
1. **Empirical contribution**: [New evidence on what question, in what context?]
2. **Theoretical contribution**: [New framework, mechanism, or conceptual advance?]
3. **Methodological contribution**: [Novel method, data, or identification strategy?]
4. **Policy contribution**: [What policy implications are drawn?]

[Not all papers contribute on all four dimensions. Only include those that apply.]

## Limitations and Critical Assessment

[Your independent evaluation — not just what the authors acknowledge:]
1. **Identification threats**: [What could violate the identifying assumptions?]
2. **External validity**: [How generalizable are the results beyond the study context?]
3. **Omitted mechanisms**: [What channels or explanations are missing?]
4. **Data constraints**: [What would stronger data allow?]
5. **Equilibrium considerations**: [Does the paper account for general equilibrium adjustments?]

## Cross-Disciplinary Bridges

[How does this paper connect to the researcher's other domains?]
- **Connection to [Domain X]**: [Explain how findings or methods relate]
- **Connection to [Domain Y]**: [Explain]
- **Suggested related works**: 
  - [Author (Year) — brief reason for relevance]
  - [Author (Year) — brief reason for relevance]
  - [Author (Year) — brief reason for relevance]

## Key Equations or Models (if applicable)

[Reproduce the main estimating equation(s) in LaTeX-compatible notation. Only include if central to understanding the paper.]

$$
\ln(P_{it}) = \alpha + \beta D_{it} + \gamma X_{it} + \mu_i + \tau_t + \varepsilon_{it}
$$

[Where P is..., D is..., X is..., μ is..., τ is...]

## Quotable Passages

[Extract 1–3 direct quotes that capture the paper's key insight, suitable for use in a literature review. Include page numbers.]

> "[Quote]" (p. XX)
```

---

## Formatting Rules

1. **Keywords**: Must use domain-specific vocabulary from the relevant skill file(s). Generic terms like "housing," "cities," or "regression" alone are insufficient. Use: "hedonic capitalization," "spatial lag model," "rent gap theory," "mortgage default contagion."

2. **Precision**: Coefficients and magnitudes must be reported with their units. "A 10% increase in X is associated with a 2.3 percentage point decrease in Y (β = −0.23, SE = 0.05)" — not "X has a negative effect on Y."

3. **Attribution**: Distinguish between:
   - What the authors **claim**
   - What the evidence **supports**
   - What remains **speculative** or **assumed**
   Use language like: "The authors argue...", "The evidence suggests...", "This assumes that..."

4. **Length**: 
   - Standard empirical paper: 800–1,200 words.
   - Theoretical/methodological paper: 600–1,000 words.
   - Review/survey paper: 1,000–1,500 words.

5. **No hallucination**: If information is not present in the article, state "[Not reported in the paper]" rather than inferring or fabricating details.
