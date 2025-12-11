# lego-analysis

Author: Yuanxi Liu
Date: 12.2025

# LEGO Aftermarket Value Analysis

## Description
This repository contains a data analysis project exploring what drives the long-term aftermarket value of LEGO sets.  
Using cleaned datasets with set attributes (theme, release year, piece count, retirement year) and estimated sealed/used market values, we examine how different factors influence value appreciation over time.  

The project includes:
- ROI (return on investment) calculations  
- Descriptive analysis of release year trends  
- Theme-level performance comparisons  
- Sealed vs. used market value patterns  
- Set size and scarcity effects  
- A predictive model for aftermarket prices  
- Actionable recommendations for LEGO’s product strategy  

This work was completed as part of a data analytics course. All code and visualizations follow a CRISP-DM style workflow.

---

## Questions of Interest
1. **How does LEGO set value appreciate over time?**  
   Do older sets consistently outperform newer ones?

2. **Which themes generate the highest long-term ROI?**  
   Are certain nostalgic or low-run themes more valuable?

3. **How does condition affect value?**  
   How large is the price gap between sealed and used sets?

4. **Does set size influence appreciation?**  
   Do larger sets gain more value, or are small exclusives stronger?

5. **Can we predict aftermarket value from basic attributes?**  
   Using features like theme, release year, and piece count.

---

## Motivation
LEGO sets behave like collectible assets in the secondary market, with some sets appreciating dramatically after retirement.  
Our goal is to understand **why** some sets gain value while others decline, and how LEGO could use data to guide its future product and pricing strategy.

Since the provided dataset reflects general aftermarket values rather than Amazon-specific sales, our analysis focuses on **market-driven collector demand**, scarcity, and theme nostalgia effects.

---

### Mini-Disclaimer
This notebook is part of my capstone project for a data science course. The project is independent and has no connection to the company LEGO. I am very much a beginner in data analysis and have created this notebook as one of my projects in an online course. Please don't take the conclusions I have made too seriously. If you have suggestions for improvement or insight into maybe some errors I've made, please feel free to let me know.

---

## Installation
An Anaconda distribution and the following packages are required:
* Python 3.9.7
* matplotlib    3.4.3
* matplotlib-inline 0.1.2
* nltk  3.6.5
* notebook  6.4.5
* numpy 1.20.3
* pandas    1.3.4
* plotly    5.5.0
* regex 2021.8.3

---

## Sources
Data being used in this notebook has been downloaded from the following sources:

Lego datasets:
* https://brickset.com/

Currency exchange rates:
* www.macrotrends.net

Consumer Price Index (CPI):
* https://fred.stlouisfed.org/series/CPIAUCSL

---

## Project Structure:
The project is made out of the following files:
* lego-analysis.ipynb as the main jupyter notebook
* all datasets are stored in the folder /data as csv files

---

---

## CRISP-DM Process Overview

### **Business Understanding**
LEGO wants to identify product characteristics that drive long-term value in the collector market.  
Key questions include theme strength, scarcity, condition, and size effects.

### **Data Understanding**
We use two datasets:  
- LEGO set information (theme, year, pieces, retirement)  
- Estimated resale values for sealed and used sets  

### **Data Preparation**
- Cleaning missing values  
- Creating ROI features  
- Basic feature engineering (lifespan, age, etc.)

### **Modeling**
A Random Forest model predicts sealed and used aftermarket values.  
Performance:  
- **Sealed:** MAE ≈ \$36, R² ≈ 0.71  
- **Used:** MAE ≈ \$17, R² ≈ 0.73  

### **Evaluation**
The model shows aftermarket value can be meaningfully predicted using simple set attributes.

### **Deployment (Recommendations)**
Findings were used to generate strategic recommendations for LEGO, such as focusing on collector themes and expanding limited-edition sets.

---

## Key Insights
- Older sets show significantly higher ROI (often 200%–400%+).  
- Themes like **Studios, Western, Batman, SpongeBob, Bionicle, Indiana Jones** perform exceptionally well.  
- Themes tied to short-term media trends show poor ROI.  
- Sealed sets dramatically outperform used sets.  
- Set size has **little correlation** with ROI—scarcity matters more.  

---

## Recommendations for LEGO
1. Prioritize collector-focused nostalgic themes.  
2. Produce more small, limited-run exclusive sets.  
3. Reduce overproduction of short-lived media tie-ins.  
4. Integrate predictive modeling into early product planning.  
5. Enhance packaging and collector-edition offerings.

---

## Next Steps
To improve future modeling and insights, LEGO could gather:
- Customer-level purchase data  
- Sales rankings and seasonality  
- Marketing spend and inventory levels  
- Theme lifecycle performance  

These additions would support more precise forecasting and deeper understanding of demand.

---
