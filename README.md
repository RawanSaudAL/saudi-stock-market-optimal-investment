# Saudi Stock Market Optimal Investment  
Risk-Adjusted Sector Analysis Framework | Tadawul (2020–2026)

## Project Overview

This project was developed to answer a practical and widely relevant question within the Saudi Stock Exchange (Tadawul):

Which sector represents the strongest and most strategically efficient opportunity for capital allocation when balancing growth, risk, and liquidity?

The dashboard is designed not only as an analytical exercise, but as a structured decision-support tool. Its purpose is to translate complex market behavior into clear, measurable indicators that help investors including those without deep financial expertise understand where strength is concentrated within the Saudi market and how different sectors compare in terms of performance quality.

Rather than focusing on speculation or short-term price movements, the framework evaluates sectors through disciplined quantitative metrics that reflect performance sustainability, risk exposure, and execution feasibility. The objective is to provide a rational foundation for investment direction within the Saudi equity market.

---

## Data Source

The analysis is based on a historical dataset sourced from Kaggle, originally retrieved via the Yahoo Finance API (yfinance). It includes daily market data for 16 major Saudi-listed companies across key sectors including Banking, Energy, Telecommunications, Healthcare, Utilities, and others.

The dataset covers the period from January 1, 2020 to January 15, 2026, with 21,816 time-series observations. It contains closing prices, trading volumes, ticker identifiers, and sector classifications. Sector enrichment enabled structured aggregation and consistent cross-sector comparison.

The timeframe captures multiple economic cycles and market fluctuations, allowing sector strength and resilience to be evaluated across varying conditions.

---

## Methodology and Analytical Process

The project followed a structured analytical workflow beginning with data preparation in Python and concluding with interactive dashboard implementation in Tableau.

Data preprocessing was conducted using pandas and numpy to ensure reliability and computational accuracy. Missing values were inspected and handled appropriately, duplicate records were removed based on Date and Ticker combinations, datetime formatting was standardized, and numeric columns such as Close price and Volume were validated.

Daily returns were engineered using the standard financial formula:
<img width="700" height="168" alt="image" src="https://github.com/user-attachments/assets/7e338fca-71fc-45ce-8bc5-b418b8e0161b" />

Exploratory Data Analysis was conducted before KPI construction to validate statistical assumptions and understand the behavior of returns across sectors. This included inspection of return distributions, volatility dispersion, and descriptive statistics such as mean return, standard deviation, minimum, and maximum values. This ensured that risk-adjusted calculations were built on empirically observed patterns.

The analytical framework was structured around five guiding investment questions:

1. Which sector delivered the strongest cumulative growth?
2. Which sector exhibited the lowest volatility?
3. Which sector generated the highest return relative to risk?
4. Where is liquidity most concentrated?
5. Which sector demonstrates the most efficient overall capital profile when combining these dimensions?

Growth was measured using cumulative aggregation of daily returns for comparative purposes. Volatility was calculated using the standard deviation of daily returns as a statistical measure of risk. Risk-adjusted efficiency was defined as average daily return divided by volatility, allowing internal sector comparison. Liquidity was measured through total traded volume to reflect market depth and practical investability.

To synthesize these components into a single decision metric, a composite score was constructed using:

<img width="1274" height="158" alt="image" src="https://github.com/user-attachments/assets/4390d1f4-652d-4527-8211-325741a0bd36" />



Logarithmic scaling was applied to normalize skewed liquidity distributions while preserving meaningful differences in trading depth. This composite score enables dynamic sector ranking based on balanced efficiency rather than isolated performance extremes.

The dashboard was implemented in Tableau using advanced table calculations including dynamic ranking (RANK), statistical aggregation (STDEV), and automatic best-sector identification (WINDOW_MAX). Interactive filters allow users to adjust timeframes and sector selections, ensuring transparency and analytical flexibility.

The layout was first structured in Figma to ensure clarity, hierarchy, and usability for both technical and non-technical audiences.

---

## Dashboard and Design

The interactive dashboard presents:

- Sector growth trends over time  
- Risk versus return positioning  
- Liquidity concentration across sectors  
- Dynamic composite ranking  

These components collectively provide a structured view of sector strength within the Saudi market.

<img width="1264" height="982" alt="image" src="https://github.com/user-attachments/assets/f748ffb1-0279-4aa2-9626-15b4a9550736" />


The design prototype developed in Figma ensured that information hierarchy and KPI visibility support intuitive interpretation.

<img width="1568" height="936" alt="image" src="https://github.com/user-attachments/assets/17c1554d-abfe-4e74-a547-629308fe1d42" />




---

## Key Insights

The analysis demonstrates that sector leadership varies depending on the evaluation dimension. Some sectors exhibit strong cumulative growth but higher volatility, while others provide stability with moderate returns.

When integrating growth, volatility, and liquidity into the composite efficiency model, the IT Applications & Services sector achieved the highest overall score during the analyzed period. It demonstrated sustained growth, controlled volatility relative to other high-performing sectors, and strong trading liquidity sufficient for scalable capital deployment.

The broader insight is that identifying the strongest sector requires evaluating performance quality rather than absolute numbers. A balanced risk-adjusted framework provides a more defensible and rational basis for investment direction within the Saudi market.

---

## Live Access

Interactive Tableau Dashboard:  
[Insert Tableau Public Link Here]

Original Dataset Source:  
https://www.kaggle.com/datasets/abdulmalekx/saudi-stocks-prediction-data-tadawul-2020-2026

Figma Design Prototype:  

https://www.figma.com/design/H5bkUK2twcapapJAqe0FtP/Untitled?node-id=0-1&t=hl32pgvtof4JjhIB-1

---

## Assumptions and Limitations

## Assumptions & Limitations

This analysis is based on historical market data and focuses on relative sector comparison rather than forward-looking prediction. Cumulative daily returns were used for comparative evaluation, and the risk-adjusted metric does not incorporate a risk-free rate, as the objective was internal efficiency assessment within the same market context.

The dataset includes 16 major Saudi-listed companies. In certain sectors, representation was limited to a single company, meaning sector performance reflects the behavior of that representative firm rather than the full breadth of the industry. Expanding coverage across additional companies per sector would improve robustness and reduce representation bias.

The framework intentionally concentrates on observable market behavior  price-based returns, statistical volatility, and liquidity depth — and does not incorporate financial statement fundamentals such as earnings growth, leverage ratios, or valuation multiples. The scope was defined to evaluate market-driven performance efficiency.

From a design perspective, advanced visual treatments prototyped in Figma, such as detailed gradients and custom shapes, could not be fully replicated in Tableau due to platform constraints. Analytical clarity and interpretability were prioritized over aesthetic complexity to maintain usability.

The dashboard was intentionally designed to remain accessible to non-technical users and individuals with limited market experience. Future iterations may incorporate deeper analytical layers, broader sector coverage, and additional financial indicators to enhance depth while preserving interpretability.

---
## Conclusion

This project demonstrates a structured approach to transforming raw market data into a decision-support framework grounded in statistical reasoning and practical investment logic. By integrating growth, volatility, and liquidity into a unified analytical model, the dashboard provides a clear and balanced perspective on sector strength within the Saudi equity market.

Beyond visualization, the core value of this work lies in disciplined KPI engineering, data validation, and the translation of quantitative analysis into interpretable insights. The framework prioritizes clarity without compromising analytical depth, making it accessible to both technical and non-technical stakeholders.

Ultimately, this analysis reflects a data-driven methodology aligned with real-world capital allocation thinking — where investment decisions are guided by measurable efficiency rather than isolated performance metrics.
