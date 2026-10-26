# EU Energy Transition & Emissions Analysis (OpenClassrooms Admission Project)

**Author:** Aitor Kevin Eteo Mba  
**Context:** OpenClassrooms Data Analyst Formation — Admission Project  
**Focus:** Univariate & Bivariate Exploratory Data Analysis (EDA)

---

## 📌 Project Overview

This project was developed as the admission capstone for the OpenClassrooms Data Analyst program. The goal was to demonstrate end-to-end data processing—from ingestion and cleaning to statistical modeling and visualization—using real-world European energy metrics.

### Research Question
> *To what extent does the share of renewable electricity generation explain variations in per-capita greenhouse gas emissions across the 27 EU member states?*

---

## 📊 Methodology & Statistical Concepts

The analysis follows the foundational probability and statistics framework covered in the OpenClassrooms coursework:

### 1. Data Collection & Preprocessing
- **Source:** Our World in Data (OWID) Complete Energy Dataset.
- **Scope:** Filtered to the 27 European Union member states for the year 2022.
- **Normalization:** Rescaled national greenhouse gas emissions from megatonnes ($\text{Mt}$) to metric tonnes per capita using national population metrics.

### 2. Univariate Analysis (`renewables_share_elec`)
- **Central Tendency & Spread:** Sample mean ($\bar{x}$), median ($Me$), standard deviation ($s$), and Interquartile Range ($\text{IQR}$).
- **Distribution Shape:** Skewness ($\gamma_1$) and excess kurtosis ($\gamma_2$) evaluated via histograms and boxplots.
- **Concentration:** Empirical Lorenz curve and Gini coefficient ($G$) calculated using the trapezoidal rule to measure adoption disparities across member states.

### 3. Bivariate Analysis (`renewables_share_elec` $\rightarrow$ `co2_per_capita`)
- **Linear Association:** Empirical covariance and Pearson correlation coefficient ($r$) with significance testing ($p$-value).
- **Modeling:** Ordinary Least Squares (OLS) simple linear regression ($\hat{y} = ax + b$).
- **Goodness of Fit:** Variance decomposition ($SCT = SCM + SCE$) and coefficient of determination ($R^2$).

### 4. Visualizations
- Interactive European choropleth map built with Plotly Express.
- Matplotlib & Seaborn distribution plots (histograms, boxplots with mean indicators, regression trendlines).

---

## 🛠️ Stack

- **Language:** Python
- **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly.express`, `scipy.stats`
- **Environment:** Google Colab / Jupyter Notebook

---

## ⚠️ Limitations & Takeaways

While the regression indicates a clear inverse association between renewable power adoption and per-capita emissions, bivariate regression naturally cannot account for confounding sectoral variables (industrial baseload, transport electrification, residential heating fuels, or low-carbon nuclear power). 

Future iterations will explore multivariate panel regression across a multi-year window (2013–2023) to capture dynamic national trends.
