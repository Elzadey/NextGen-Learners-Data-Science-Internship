<p align="center">
  <img src="assets/banner.png" alt="NextGen Learners — Code · Learn · Innovate · Succeed" width="100%">
</p>

<h1 align="center">NextGen Learners — Data Science Internship</h1>

<p align="center">
  My weekly deliverables, notebooks, and datasets from the <b>NextGen Learners</b> Data Science Internship.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Cleaning-150458?logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white" alt="Jupyter">
  <img src="https://img.shields.io/badge/Google%20Colab-Ready-F9AB00?logo=googlecolab&logoColor=white" alt="Colab">
  <img src="https://img.shields.io/badge/Status-In%20Progress-1abc9c" alt="Status">
</p>

---

## 📌 About

This repository documents my progress through the **NextGen Learners Data Science Internship**. Each week focuses on a practical, real-world task, and every folder contains the full work: a documented notebook, the data, and a short write-up of the decisions I made and why.

> **Philosophy:** clean code is good, but *explained decisions* are better. Every notebook mixes code with markdown reasoning so anyone can follow the thinking, not just the output.

---

## 🗂️ Weekly Progress

| Week | Topic | Skills | Status |
|:----:|-------|--------|:------:|
| 1 | [Cleaning & Exploring the Applicant Dataset](./NextGenLearners_Week1_Data_Cleaning) | Pandas, data cleaning, wrangling, EDA | ✅ Done |
| 2 | _Coming soon_ | — | ⏳ |
| 3 | _Coming soon_ | — | ⏳ |
| 4 | _Coming soon_ | — | ⏳ |

---

## 🧹 Week 1 — Data Cleaning & Exploration

**Goal:** take a messy `applicants.csv` (missing values, duplicates, inconsistent text, wrong data types) and turn it into a clean, trustworthy dataset using only reproducible Pandas code, with no manual editing in Excel.

### What I did

1. **Explored first** with `shape`, `head()`, `info()`, `isnull().sum()` and `duplicated().sum()` to get a "before" snapshot.
2. **Handled missing values column by column**, with a written justification for each:
   - `Applicant Name`: dropped rows, since a nameless application is unusable.
   - `Email`: handled based on its role as the key follow-up field.
   - `University`: filled with `"Not Specified"` (non-critical).
   - `Status`: filled with `"Under Review"` (unprocessed applications).
3. **Removed duplicates**, both exact rows and near-duplicates detected by `Email`.
4. **Standardized text**: stripped whitespace, unified casing, and mapped messy `Domain Applied` spellings to 5 clean categories.
5. **Fixed data types**: converted `Application Date` to `datetime64` with `pd.to_datetime(errors='coerce')` and normalized `Phone` formatting while keeping it as text.
6. **Wrote a Data Quality Summary** (before vs. after) and exported the cleaned dataset.

### Techniques used

`isnull()` · `dropna()` · `fillna()` · `drop_duplicates()` · `str.strip()` · `str.title()` · `str.lower()` · `str.replace()` · `.map()` · `pd.to_datetime()`

### Deliverables

| File | Description |
|------|-------------|
| `Week1_Data_Cleaning_<Name>.ipynb` | Fully documented notebook with markdown explanations |
| `applicants.csv` | Raw (messy) input data |
| `applicants_cleaned.csv` | Final cleaned dataset |

---

## 🚀 How to Run

**Option 1 — Google Colab (no setup)**

1. Open [colab.research.google.com](https://colab.research.google.com) and choose **File → Upload notebook**.
2. Upload the notebook and `applicants.csv` from the Week 1 folder.
3. Run **Runtime → Run all**.

**Option 2 — Locally**

```bash
# 1. Clone the repository
git clone https://github.com/Elzadey/NextGen-Learners-Data-Science-Internship.git
cd NextGen-Learners-Data-Science-Internship/NextGenLearners_Week1_Data_Cleaning

# 2. Install dependencies
pip install pandas jupyter faker

# 3. Launch Jupyter and run the notebook top-to-bottom
jupyter notebook
```

---

## 📁 Repository Structure

```text
NextGen-Learners-Data-Science-Internship/
├── assets/
│   └── banner.png
├── NextGenLearners_Week1_Data_Cleaning/
│   ├── Week1_Data_Cleaning_<Name>.ipynb
│   ├── applicants.csv
│   └── applicants_cleaned.csv
└── README.md
```

---

## 🛠️ Tech Stack

- **Python** — core language
- **Pandas** — data cleaning and wrangling
- **Faker** — generating realistic mock data
- **Jupyter / Google Colab** — documented, reproducible analysis

---

## 👩‍💻 Author

**Elzadey** — [GitHub](https://github.com/Elzadey)

---

<p align="center">
  <b>CODE · LEARN · INNOVATE · SUCCEED</b><br>
  <i>Empowering Minds, Building Futures</i> — <a href="https://github.com/nextGenLearners">@nextGenLearners</a>
</p>
