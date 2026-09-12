# Countries of the World Data Pipeline & Analysis

An automated data pipeline and exploratory data analysis project that extracts global demographic metrics via web scraping, processes the data using Python, and builds interactive visualizations.

---

## Project Overview
* **Goal:** Extract, clean, and analyze global demographic and geographic data to uncover key population trends, density metrics, and geographic distributions.
* **Key Focus Areas:** Automated web extraction of country metrics, demographic feature engineering (population density), and interactive data visualization of global populations.

---

## Workflow & Steps

### 1. Data Extraction & Scraping Pipeline
* **Source Targeting:** Connects to the ScrapeThisSite Simple Sandbox target to retrieve raw demographic web elements.
* **Parsing Logic:** Utilizes Python's `requests` and `BeautifulSoup` libraries to iterate through country container blocks (`div.country`), parsing text nodes for names, capitals, population, and area metrics.
* **Data Export:** Serializes the parsed data into a clean Pandas DataFrame before persisting the output to `../RawData/countries_of_the_world.csv`.

### 2. Data Cleaning & Feature Engineering
* **Data Cleansing:** Inspects and resolves missing administrative data, standardizing missing text strings for regions lacking formal capitals.
* **Feature Engineering:** Computes derived metrics including population density ($\text{population} / \text{area}$) and regional aggregations.

### 3. Exploratory Data Analysis & Visualizations
* **Interactive Dashboarding:** Employs `plotly.express` to generate interactive bar charts showcasing top populated countries, density rankings, and spatial distribution scatter plots.

---

<a id="viz"></a>

![Viz1](viz/Countries_of_the_World_viz.png)

<div align="center">

### Smallest Nations, Population Densities & Major Populations
*Analysis of the top smallest countries by area via scatter plots, population density rankings across high-density regions, and demographic breakdowns for nations with populations exceeding 100 million.*
</div>
