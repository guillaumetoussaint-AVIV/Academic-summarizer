# Academic Article Summarizer — Residential Real Estate Research

A set of AI agent skills for producing detailed, structured summaries of scientific articles in the interdisciplinary field of residential real estate.

## Purpose

These skills act as a **knowledge base and instruction set** for a generative AI model (Claude, GPT, etc.) to produce high-quality academic summaries. Each skill file contains domain-specific vocabulary, theoretical frameworks, key references, and evaluation criteria that guide the model toward precise, field-appropriate output.

## Target Domains

| Domain | Skill File | Focus |
|---|---|---|
| Orchestrator | `00-orchestrator.md` | Routes articles to relevant domains, sets quality standards |
| Urban Economics | `01-urban-economics.md` | Hedonic pricing, sorting, housing supply, amenity capitalization |
| Geographic Finance | `02-geographic-finance.md` | Mortgage markets, house price indices, spatial risk, financialization |
| Regional Science | `03-regional-science.md` | Spatial econometrics, agglomeration, migration, regional equilibrium |
| Geography | `04-geography.md` | Neighborhood effects, gentrification, segregation, GIS, critical geography |
| Methodology | `05-methodology.md` | Causal inference, spatial econometrics, ML, qualitative methods |
| Summary Template | `06-summary-template.md` | Standardized output format for all summaries |

## How to Use

### Option 1 — System Prompt (recommended)

Concatenate the skill files and include them in your system prompt or custom instructions:

```
You are a research assistant. Follow the instructions in the attached skill files to summarize academic articles.

[Paste contents of all .md files]
```

### Option 2 — Claude Projects / GPT Custom Instructions

1. Create a new project in Claude (Projects) or a Custom GPT.
2. Upload all `.md` files from the `skills/` folder as knowledge base documents.
3. Set the project instructions to: *"When I share an academic article, summarize it following the Orchestrator workflow and Summary Template."*

### Option 3 — Selective Loading

For a focused session on a specific domain, load only:
- `00-orchestrator.md` (always)
- The relevant domain skill (e.g., `01-urban-economics.md`)
- `05-methodology.md` (always)
- `06-summary-template.md` (always)

## Usage Example

**Prompt:**
> Summarize the following article: [paste article text or PDF]

The model will:
1. Classify the article into one or more domains
2. Identify the methodology
3. Produce a structured summary using the template
4. Add cross-disciplinary connections

## Customization

- **Add new domains**: Create a new skill file following the same structure (frameworks, vocabulary, evaluation criteria, journals, foundational references).
- **Adjust output format**: Edit `06-summary-template.md` to modify the summary structure.
- **Add journals or references**: Append to the relevant domain skill's reference section.

## File Structure

```
academic-summarizer-skills/
├── README.md
└── skills/
    ├── 00-orchestrator.md
    ├── 01-urban-economics.md
    ├── 02-geographic-finance.md
    ├── 03-regional-science.md
    ├── 04-geography.md
    ├── 05-methodology.md
    └── 06-summary-template.md
```

## License

Free to use for academic research purposes.
