# 🐱 Cookie Cats: A/B Test Analysis

**Does delaying the gate from level 30 to level 40 hurt player retention?**

## 📌 Project Overview

Cookie Cats is a popular mobile puzzle game. Players encounter *gates* — forced pauses that encourage them to wait or make an in-app purchase. The product team wanted to know: **what happens to player retention if the first gate is moved from level 30 to level 40?**

This project presents a full A/B test analysis of ~90,000 players, from sample size planning to a data-driven product recommendation.

## 🎯 Research Questions

1. **Sample size planning** — how many users do we need to detect a meaningful effect?
2. **Exploratory analysis** — what does 7-day retention look like across both groups?
3. **Statistical testing (Z-test)** — is the observed difference statistically significant?
4. **Validation (χ²-test)** — does an independent method confirm the result?

## 📊 Key Results

| Metric | gate_30 (control) | gate_40 (treatment) |
|---|---|---|
| 7-day retention | **19.02%** | 18.20% |
| 1-day retention | **44.52%** | 44.23% |
| Z-test p-value | | 0.0016 |
| χ²-test p-value | | 0.0016 |

**Conclusion:** Moving the gate to level 40 statistically significantly reduces 7-day retention (p = 0.0016 < 0.05). The 95% confidence intervals for both groups do not overlap, confirming the result is stable. **Recommendation: keep the gate at level 30.**

## 🗂 Repository Structure

```
├── cookie_cats_ab_test_analysis.ipynb   # Main analysis notebook
├── cookie_cats.csv                      # Dataset (source: Kaggle)
└── README.md
```

## 🛠 Tech Stack

- **Python 3.10**
- **pandas** — data manipulation
- **scipy / statsmodels** — statistical tests (Z-test, χ²-test, power analysis)
- **seaborn / matplotlib** — visualisation

## 📂 Dataset

Source: [Mobile Games A/B Testing — Cookie Cats (Kaggle)](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats)

Columns: `userid`, `version`, `sum_gamerounds`, `retention_1`, `retention_7`

## 🚀 How to Run

```bash
git clone https://github.com/YOUR_USERNAME/cookie-cats-ab-test.git
cd cookie-cats-ab-test
pip install pandas scipy statsmodels seaborn matplotlib
jupyter notebook cookie_cats_ab_test_analysis.ipynb
```

Or open directly in Google Colab:  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/cookie-cats-ab-test/blob/main/cookie_cats_ab_test_analysis.ipynb)

---
*Feel free to reach out with questions or feedback!*
