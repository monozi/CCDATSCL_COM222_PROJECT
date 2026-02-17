# 🏋️ Quantifying Strength and Body Composition Changes
### from a 10-Week Structured Resistance Training Program
#### *A Self-Experiment Study (N-of-1 SCED)*

<div align="center">

![Saitama Workout](https://media.tenor.com/vnZXVC8fuA8AAAAi/aba-saitama-saitama-aba.gif)

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-1A7A4A?style=for-the-badge)
![Duration](https://img.shields.io/badge/Duration-10_Weeks-E8A838?style=for-the-badge)
![Design](https://img.shields.io/badge/Design-N--of--1_SCED-1B2A4A?style=for-the-badge)

</div>

---

**👤 Author:** John Angelo A. Basilio  
**🏫 Institution:** National University — College of Computing and Information Technologies, Manila, Philippines  
**📚 Course:** Data Science (CCDATSCL_COM222)  
**📅 Period:** November 24, 2025 – February 2, 2026

---

## 📌 Overview

This repository contains all data, code, and documentation for a 10-week self-experiment study examining the effects of structured progressive resistance training and caloric surplus on body composition, strength, and training volume. The researcher served as both investigator and participant, applying a rigorous Single-Case Experimental Design (SCED) methodology with comprehensive daily tracking.

| | |
|---|---|
| ⚖️ **Baseline** | 66.0 kg |
| 🎯 **Target** | 80 kg |
| 🏁 **Endpoint** | 75.5 kg |
| 📊 **Total Observations** | 296 (across 3 data sources) |

---

## 🔥 Key Findings

<div align="center">

![Results](https://media.giphy.com/media/3o7aTskHEUdgCQAXde/giphy.gif)

</div>

| 📈 Outcome | Baseline | Endpoint | Change | p-value | Cohen's d |
|---|---|---|---|---|---|
| ⚖️ Body Weight | 66.0 kg | 75.5 kg | +9.5 kg | <0.001 | 2.55 |
| 💪 Muscle Mass | 29.2 kg | 33.9 kg | +4.7 kg | <0.001 | 2.56 |
| 🏋️ Volume Load | 19,780 kg/wk | 59,040 kg/wk | +198% | 0.008 | 1.17 |
| 🔄 Phase 2 vs Phase 1 | 26,543 kg | 50,268 kg | +89.4% | 0.0015 | 3.27 |

- ✅ All **3 hypotheses rejected** (p < 0.01, large effect sizes)
- ✅ Muscle gains exceeded BIA error by **1.84×** the ±6.86% SEM threshold
- ✅ Body fat remained stable (22.0% → 22.1%) — **successful clean bulk** 🎉
- ✅ Strong correlations: Volume→Muscle (r=0.755 ⭐), Protein→Muscle (r=0.786 ⭐)

---

## 📁 Repository Structure

```
📦 self-experiment-study
├── 📂 data/
│   ├── 📄 body_composition.csv             # Weekly anthropometric measurements (Week 0–10)
│   ├── 📄 workout_log.csv                  # Per-session training data (sets, reps, weight, e1RM)
│   ├── 📄 food_intake.csv                  # Daily nutritional intake (calories, protein, water)
│   └── 📄 final_comprehensive_dataset.csv  # Merged & cleaned dataset
│
├── 📂 notebooks/
│   └── 📓 self_experiment_study.ipynb      # Full analysis notebook (EDA + hypothesis testing)
│
├── 📂 paper/
│   └── 📝 Basilio_Self-Experiment_Study.pdf  # IEEE-formatted research paper
│
├── 📂 figures/                             # All generated figures (Figs 1–7)
│
└── 📄 README.md
```

---

## 🧪 Hypotheses

| # | 🔴 Null Hypothesis (H₀) | Test Used | Decision |
|---|---|---|---|
| H1 | No change in body mass or volume load beyond baseline | One-Sample T-Test | ✅ **REJECT H₀** |
| H2 | No significant change in muscle mass (within BIA error) | SEM Benchmark (±6.86%) | ✅ **REJECT H₀** |
| H3 | No difference in volume between UL split and PPL split | Independent Samples T-Test | ✅ **REJECT H₀** |

---

## 📊 Statistical Methods

<div align="center">

![Data Analysis](https://media.giphy.com/media/xT9IgzoKnwFNmISR8I/giphy.gif)

</div>

| 🔬 Method | Purpose |
|---|---|
| 📋 Descriptive Statistics | Mean, SD, min/max, quartiles for all variables |
| 🔔 Shapiro-Wilk Test | Normality validation before parametric tests |
| 🧮 One-Sample T-Test | Baseline-to-post-intervention comparison (H1) |
| 📏 SEM Benchmark | Observed change vs ±6.86% BIA error threshold (H2) |
| ⚖️ Independent Samples T-Test | Phase 1 (UL) vs Phase 2 (PPL) volume (H3) |
| 🔗 Pearson Correlation (r) | Volume/protein vs muscle mass changes |
| 📐 Cohen's d | Effect size for all t-tests |

All analyses performed in Python using `pandas`, `scipy`, `matplotlib`, and `seaborn`.

---

## 📦 Data Sources

| 🗂️ Source | Frequency | Tool | Variables |
|---|---|---|---|
| `body_composition.csv` | Weekly (Monday, fasted) | BIA Scale + Measuring Tape | Weight, muscle mass, body fat %, circumferences |
| `workout_log.csv` | Per session | HEVY App | Exercise, sets, reps, weight, volume load, e1RM |
| `food_intake.csv` | Daily | MyFitnessPal + Digital Food Scale | Calories, protein, water, creatine |

---

## 🏋️ Training Protocol

| Phase | Weeks | Split | Frequency | 📊 Avg Volume/Week |
|---|---|---|---|---|
| 🔵 Phase 1 | 1–6 | Upper/Lower (UL) | 4×/week | 26,543 kg |
| 🟢 Phase 2 | 7–9 | Push/Pull/Legs + UL (PPL/UL) | 5×/week | 50,268 kg |

> ⚠️ Week 10 data was collected but partially compromised by gastrointestinal illness. Volume analysis uses Weeks 1–9.

---

## 📖 Variable Definitions

| Variable | Definition |
|---|---|
| `volume_load` | Sets × Reps × Weight (kg) per exercise |
| `e1RM` | Estimated 1-rep max: `weight × (1 + reps/30)` |
| `muscle_mass` | BIA-estimated skeletal muscle tissue (kg) |
| `avg_protein` | Weekly average of daily protein intake (g) |
| `avg_calories` | Weekly average of daily caloric intake (kcal) |
| `week` | Sequential week index (0 = baseline, 1–10 = intervention) |

---

## 🚀 How to Run

### Requirements
```bash
pip install pandas numpy scipy matplotlib seaborn scikit-learn jupyter
```

### Run the Notebook
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
jupyter notebook notebooks/self_experiment_study.ipynb
```

> 💡 The notebook loads data from GitHub raw URLs — no local file setup required.

---

## 📈 Results Summary

### 💪 Body Composition (Figure 4)
Body weight increased linearly (R²=0.91, +0.95 kg/week). Muscle mass showed the highest predictability (R²=0.95, +0.47 kg/week) — exceeding typical population averages of 0.5–1.0 kg/month. Body fat showed no temporal trend (R²=0.08), confirming a successful clean bulk. 🎯

### 🔬 Measurement Validity (Figure 6)
The observed muscle mass change of +12.62% exceeded the ±6.86% BIA SEM threshold by a factor of **1.84** — validating consumer-grade BIA for individual tracking when measurements are standardized. ✅

### 🔄 Split Modification Effect (Figure 7)
Transitioning from a 4-day to 5-day training split produced an **89% increase** in weekly volume (d=3.27) — suggesting split structure is a high-leverage programming variable independent of general fitness level. 📊

---

## ⚠️ Limitations

- 👤 Single-subject design limits generalizability
- 🔄 Mid-study split modification introduces causal ambiguity for post-Week 7 changes
- 📏 BIA has ±3–4% SEM vs gold-standard DXA or MRI
- 🥗 Nutritional logging subject to human estimation error
- 📉 n=9 intervention weeks limits statistical power for correlation analyses

---

## 📝 Citation

```
Basilio, J. A. A. (2026). Quantifying Strength and Body Composition Changes from a 
10-Week Structured Resistance Training Program: A Self-Experiment Study. 
National University, Manila, Philippines.
```

---

## 📜 License

This project is for academic purposes. Data reflects personal physiological measurements of the author.

---

<div align="center">

*Made with 💪, 📊, and a lot of data tracking*

![Thank You](https://media.giphy.com/media/13HgwGsXF0aiGY/giphy.gif)

</div>
