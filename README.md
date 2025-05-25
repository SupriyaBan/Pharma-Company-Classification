# Indian Pharmaceutical Sector Analysis

This project presents a comprehensive financial and clustering analysis of 40 publicly listed pharmaceutical companies in India, offering insights into the sector's structure, performance, and segmentation.

## Project Objective
To analyze the financial health, efficiency, and performance patterns across the Indian pharmaceutical landscape by leveraging financial ratios, exploratory data analysis (EDA), and clustering techniques.

## Company Selection Criteria
Based on market capitalization

Includes small-cap, mid-cap, and large-cap firms

Ensures a balanced representation of the Indian pharmaceutical industry, from major players like Sun Pharma to niche companies like Jubilant Pharmova

## Financial Ratios Considered
Ratio	Formula	Description
Current Ratio	Current Assets / Current Liabilities	Liquidity measure
Debt-to-Equity	Total Debt / Total Equity	Capital structure
Inventory Turnover	COGS / Inventory	Inventory efficiency
Return on Equity (ROE)	Net Income / Total Equity	Profitability
Operating Margin	Operating Income / Revenue	Operational profitability
P/E Ratio	Share Price / EPS	Valuation
Book Value per Share	Total Equity / Shares Outstanding	Valuation metric
Asset Turnover	Revenue / Total Assets	Asset efficiency
Debt Ratio	Total Debt / Total Assets	Financial leverage
Net Profit Margin	Net Income / Revenue	Overall profitability

## Exploratory Data Analysis (EDA)
### Distribution & Outliers
Outliers found in: Current Ratio, Book Value per Share, P/E Ratio

Mild negatives in ROE and Net Profit Margin, indicating underperformers

Operating Margin and Debt Ratios showed moderate skewness

### Correlation Insights
Strong Positive Correlation:

ROE & Net Profit Margin (0.92)

Debt Ratio & D/E (0.98)

Inventory Turnover & Asset Turnover (0.64)

Strong Negative Correlation:

Current Ratio & Debt Ratios (~-0.55)

Net Profit Margin & D/E (-0.31)

Cluster Categories from Correlations:
Profitability: ROE, NPM, Operating Margin

Leverage: Debt Ratio, D/E

Liquidity: Current Ratio

Efficiency: Inventory Turnover, Asset Turnover

## K-Means Clustering
Methodology
Algorithm: K-Means

Metrics used: Elbow Method, Silhouette Score, Calinski-Harabasz Index

Optimal Clusters: 3

### Cluster Breakdown
Feature	Cluster 0 ("Aggressives")	Cluster 1 ("A-Players")	Cluster 2 ("Underperformers")
Current Ratio	1.37	3.66	1.48
Debt-to-Equity	0.73	0.087	0.32
ROE	2.1%	3.8%	-8.7%
Operating Margin	14.6%	17.3%	3.6%
Net Profit Margin	6.9%	16.0%	-32.8%
P/E Ratio	43.4	41.3	-152.1
Book Value/Share	174.0	327.4	273.4
Asset Turnover	0.154	0.191	0.141
Debt Ratio	0.32	0.057	0.157

### Cluster Interpretation
Cluster 0 - "Aggressives": High leverage, moderate profitability — possibly value investments with risk.

Cluster 1 - "A-Players": Top-performing, financially stable, efficient — ideal growth stocks.

Cluster 2 - "Underperformers": Financially distressed with losses and low efficiency.

## Feature Ranking
Techniques Used:
ANOVA F-Test (for statistical relevance)

Random Forest (for non-linear importance)

Key Insights:
Most influential: Debt-related and profitability metrics (ROE, NPM, D/E)

Least influential: Inventory Turnover, Asset Turnover, Operating Margin

## Agglomerative Hierarchical Clustering
🛠 Method:
Agglomerative clustering with Ward’s linkage

Dendrogram used to visualize cluster hierarchy

3 major clusters identified

Cluster Summary:
Feature	Cluster 1 ("Balanced")	Cluster 2 ("Top-performers")	Cluster 3 ("Asset-rich & Efficient")
ROE	3%	5%	2%
Net Profit Margin	10%	20%	7%
Debt-to-Equity	0.36	0.04	0.22
Book Value/Share	235.8	264.3	367.2

### Cluster Interpretation
Balanced: Profitable, efficient, but moderate debt use.

Top-performers: Low debt, high returns — investor favorites.

Asset-rich & Efficient: High asset utilization, mature capital-intensive firms.

## Outlier Detection: Isolation Forest
Algorithm Used:
Isolation Forest for anomaly detection

Identified Outliers:
Glenmark

AstraZeneca India

Unichem Labs

Wockhardt

These firms had:

Negative ROE or Net Profit Margin

Extreme P/E Ratios

Varying cluster assignments, confirming financial anomalies

