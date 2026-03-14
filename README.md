# AI Adoption, Productivity, and Growth: A Cross-Country Macroeconomic Analysis

Cross-country panel analysis (2018–2023) studying how national AI adoption relates to labor productivity, GDP growth, and unemployment using multivariate statistical methods.

---

## Research Questions

1. What are the main factors that explain differences in AI adoption between countries?
2. How does AI adoption relate to labor productivity and GDP growth?
3. Can countries be grouped into distinct clusters based on AI readiness and economic performance?
4. Do AI adoption, GDP growth, and productivity follow a multivariate normal distribution?

---

## Key Findings

- **AI research activity** (publications per capita) shows the strongest correlation with both labor productivity (r = 0.79) and GDP growth (r = 0.84)
- **AI VC investment** shows weaker short-run correlations, likely due to time lags between investment and economic returns
- **PCA** constructs a single AI readiness index from three indicators (research, investment, skills), with PC1 explaining ~54% of variance. Log-transformation was necessary to prevent US dominance from distorting country positions
- **Clustering** reveals three global groups: advanced economies (high AI + high productivity), emerging adopters (mid-level), and specialized high-productivity economies — both K-means and hierarchical clustering agree on the groupings
- **Multivariate normality test** confirms the joint distribution of AI, productivity, and growth is **non-normal** with heavy upper tails, reflecting a global AI divide where a small number of countries far outperform the rest

---

## Data

| File | Source | Description |
|---|---|---|
| `data/ai_pubs_per_capita.csv` | OECD AI Data Portal | AI research publications per capita by country-year |
| `data/ai_pubs_time.csv` | OECD AI Data Portal | Total AI publication volume over time |
| `data/ai_skills.csv` | OECD AI Data Portal | Share of workers with AI-related skills (time-invariant) |
| `data/ai_vc_investment.csv` | OECD AI Data Portal | Private-sector VC investment in AI by country-year |
| `data/labor_productivity.csv` | World Bank WDI | GDP per person employed |
| `data/gdp_growth.csv` | World Bank WDI | Annual real GDP growth rate |
| `data/unemployment.csv` | World Bank WDI | Unemployment rate |

**Merged panel: ~695 rows × 9 columns** (70 countries, 2018–2023)

---

## Methods

| Method | Purpose |
|---|---|
| Correlation analysis | Pairwise relationships between AI indicators and macroeconomic outcomes |
| PCA | Combine AI research, investment, and skills into a single AI readiness index |
| K-means clustering | Group countries by AI readiness and economic profile (k=3, elbow method) |
| Hierarchical clustering | Country-level dendrogram for structural grouping validation |
| MVN testing | Mahalanobis distance Q-Q plots to test distributional assumptions |

---

## Project Structure

```
ai-macroeconomic-analysis/
├── analysis/
│   └── ai_macroeconomic_analysis.ipynb
├── data/
│   ├── ai_pubs_per_capita.csv
│   ├── ai_pubs_time.csv
│   ├── ai_skills.csv
│   ├── ai_vc_investment.csv
│   ├── labor_productivity.csv
│   ├── gdp_growth.csv
│   └── unemployment.csv
├── report/
│   └── DATA319_Final_Project_Report.pdf
└── README.md
```

---

## Requirements

```
numpy pandas matplotlib seaborn scikit-learn scipy pycountry
```

```bash
pip install numpy pandas matplotlib seaborn scikit-learn scipy pycountry
```

---

## Context

Individual final project for DATA 319 (Multivariate Statistical Methods) at Washington State University, Fall 2025. Aligned with global policy discussions on AI and sustainable development (SDG 8: Decent Work and Economic Growth).

**References:**
- OECD AI Data Portal: https://oecd.ai/en/data
- World Bank World Development Indicators: https://databank.worldbank.org/source/world-development-indicators
- OECD (2024). The Impact of Artificial Intelligence on Productivity, Distribution and Growth
- OECD (2025). Macroeconomic Productivity Gains from AI in G7 Economies
- IMF Working Paper (2025). AI Adoption and Economic Growth

---

## Author

**Seohyeon Yoon** · B.S. Data Analytics (Economics Minor), Washington State University
[LinkedIn](https://www.linkedin.com/in/seohyeon-yoon-dataanalytics)
