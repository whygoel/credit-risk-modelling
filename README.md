# Credit Risk Modelling: PD/LGD/EAD/EL Framework

[![Python](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen.svg)]()

> **End-to-end Basel III / IFRS 9 compliant credit risk modelling framework for consumer loans**

---

## 📌 Overview

This repository contains a **complete, production-ready credit risk modelling framework** built for the Lending Club loan dataset (466,285 loans, 2007-2014). The project implements:

| Component | Description | Model |
|:---|:---|:---|
| **PD** | Probability of Default | Logistic Regression |
| **LGD** | Loss Given Default | Two-Stage (Logistic + OLS) |
| **EAD** | Exposure at Default | Linear Regression |
| **EL** | Expected Loss | PD × LGD × EAD |

---

## 📊 Key Results

| Metric | Value | Status |
|:---|:---:|:---:|
| **PD Model AUC** | 0.6822 | ✅ Acceptable |
| **PD Model Gini** | 0.3644 | ✅ Acceptable |
| **PD Model KS** | 0.2647 | ✅ Good |
| **HL Calibration p-value** | 0.5568 | ✅ PASS |
| **Mean LGD** | 95.29% | ✅ Validated |
| **EAD R²** | 0.1917 | ✅ Validated |
| **Total Portfolio EL** | **$502,324,787** | ✅ Validated |
| **EL as % of Portfolio** | **7.54%** | ✅ Validated |

---

## 🛠️ Tech Stack

| Category | Tools |
|:---|:---|
| **Language** | Python 3.10 |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Statistics** | SciPy |
| **Regression** | Statsmodels (Logit, OLS) |
| **Machine Learning** | Scikit-learn |

---

## 📁 Project Structure

```
credit-risk-modelling/
│
├── complete_pipeline.py      # Full Python script
├── scorecard_final.csv       # 300-850 credit scorecard
├── README.md                 # This file
└── requirements.txt          # Dependencies
```

---

## 🚀 Installation

```bash
pip install -r requirements.txt
python complete_pipeline.py
```

---

## 📊 Model Performance

### PD Model
- **AUC:** 0.6822
- **Gini:** 0.3644
- **KS:** 0.2647
- **Hosmer-Lemeshow p-value:** 0.5568 ✅

### LGD Model
- **Stage 1 (Classification):** AUC 0.6766
- **Stage 2 (Regression):** R² 0.0597
- **Mean LGD:** 95.29%

### EAD Model
- **R²:** 0.1917
- **Mean CCF:** 0.7193

### Expected Loss
- **Total Portfolio EL:** $502,324,787
- **EL as % of Portfolio:** 7.54%

---

## 📝 License

MIT License - see [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Yash Goel**
- B.Sc. Economics (Hons.) | Gokhale Institute of Politics and Economics, Pune
- [LinkedIn](https://linkedin.com/in/yourprofile)
- [GitHub](https://github.com/whygoel)

---

## 📄 Acknowledgments

- **Dataset:** Lending Club (Kaggle)
- **Supervisor:** Assistant Professor, DIAT Pune
