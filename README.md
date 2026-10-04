# SCSE3040 — Machine Learning Operations Lab
**Surya Varshney · S24CSEU0573 · Bennett University · B.Tech CSE 5th Semester · 2026-27**

---

## 📦 About This Repository

This repository contains my lab submissions for **SCSE3040 Machine Learning Operations** at Bennett University.

The practicals follow a single running project — a **food delivery-time predictor** — built from scratch through the semester:

```
notebook → package → tracked experiments → API → container → cluster → logs → pipeline → monitoring
```

---

## 🗂️ Practicals

| # | Practical | Topic | Status |
|---|---|---|---|
| P01 | [Workbench](P01-workbench/) | Setting up Jupyter, numpy, pandas | ✅ Done |
| P02 | [First Model](P02-first-model/) | Linear regression baseline | ✅ Done |
| P03 | [Model Choice](P03-model-choice/) | Honest evaluation, cross-validation | ✅ Done |
| P04 | [Package](P04-package/) | Refactoring notebook → Python package | ✅ Done |
| P05 | [Config & Tests](P05-config-tests/) | YAML config, pytest automated tests | ✅ Done |
| P06 | [MLflow](P06-mlflow/) | Experiment tracking, model registry | ✅ Done |
| P07 | [Serving](P07-serving/) | FastAPI model serving | 🔄 In Progress |

---

## 🚀 Setup

### 1. Clone the repo
```bash
git clone https://github.com/Suryalrn/MLOPS.git
cd MLOPS
```

### 2. Create and activate the virtual environment
```bash
# Windows (PowerShell)
python -m venv venv
.\venv\Scripts\Activate.ps1

# macOS / Linux
python -m venv venv
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements-lock.txt
```

### 4. Run a practical
```bash
cd P05-config-tests
jupyter lab P05.ipynb
```

---

## 🧪 Running Tests (P05)

```bash
cd P05-config-tests/work
python -m pytest -v
```

Expected output:
```
collected 9 items

test_orders.py ....     [ 44%]
test_speed.py ..        [ 66%]
test_model.py ...       [100%]

9 passed in 1.23s
```

---

## 📊 MLflow Tracking (P06)

Start the MLflow UI:
```bash
cd P06-mlflow
python -m mlflow ui --backend-store-uri sqlite:///work/mlflow.db --port 5000
```

Then open **http://127.0.0.1:5000** in your browser.

---

## 📁 Project Structure

```
SCSE3040-Lab-main/
├── data/
│   └── delivery_times.csv      # 600-row dataset (shared across all practicals)
├── P01-workbench/
├── P02-first-model/
├── P03-model-choice/
├── P04-package/
├── P05-config-tests/
│   ├── P05.ipynb
│   ├── P05_submission.html
│   └── work/
│       ├── config.yaml         # YAML settings file
│       ├── orders.py           # Helper module
│       ├── conftest.py         # Shared pytest fixtures
│       ├── test_orders.py      # Unit tests for orders.py
│       ├── test_speed.py       # My own tests (T2)
│       └── test_model.py       # Behaviour tests for the model
├── P06-mlflow/
│   ├── P06.ipynb
│   └── work/
│       └── mlflow.db           # (gitignored — generated locally)
├── requirements-lock.txt       # Pinned dependencies
├── requirements-tools.txt      # Dev tools
├── SETUP.md
└── README.md
```

---

## 🤖 AI Use Disclosure

I used **Antigravity IDE (Google DeepMind)** to help with code completion and explaining pytest fixture patterns during the P05 lab session.

---

## 👨‍🏫 Course Details

| | |
|---|---|
| **Course** | SCSE3040 Machine Learning Operations |
| **University** | Bennett University |
| **Instructor** | Dr. Gaurav Tripathi |
| **Email** | gaurav.tripathi@bennett.edu.in |
| **Session** | 2026-27 |
