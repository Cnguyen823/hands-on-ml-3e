# Hands-On Machine Learning (3rd Edition)

My study notebooks and experiments for *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow (3rd Ed.)* by Aurélien Géron.

---

## 📂 Repository Structure
```
hands-on-ml-3e/
├── chapter01/          # notebooks per chapter
├── chapter02/
...
├── chapter19/
├── datasets/
│   ├── raw/            # raw datasets (gitignored)
│   └── processed/      # small sample datasets safe to commit
├── experiments/        # side projects and experiments
├── scripts/            # helpers, preprocessing, etc.
├── requirements.txt
├── .gitignore
└── README.md
```

---

## ⚙️ Environment Setup

### Using Conda
```bash
conda create -n hands_on_ml python=3.10 -y
conda activate hands_on_ml
pip install -r requirements.txt
```

### Using venv
Mac/Linux:
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
Windows:
```powershell
python -m venv venv
.env\Scriptsctivate
pip install -r requirements.txt
```

---

## 🗂 .gitignore
This repo ignores:
- Python cache files (`__pycache__`, `.pyc`)
- Virtual environments (`venv/`)
- Jupyter notebook checkpoints (`.ipynb_checkpoints/`)
- Raw datasets and model weights (`datasets/raw/`, `models/`)
- OS clutter (`.DS_Store`)
- Large ML model files (`*.h5`, `*.ckpt`, `*.pt`, `*.npz`)

---

## 🔧 Notebook Hygiene with nbstripout
To keep commits clean, install `nbstripout` to automatically strip outputs from notebooks:

```bash
pip install nbstripout
nbstripout --install
```

- Removes outputs before committing.
- Keeps repo small, clean, and reproducible.
- Collaborators can run the same commands.

---

## 🤖 Automated Notebook Execution (GitHub Actions)

This repository uses a GitHub Actions workflow to automatically run all Jupyter notebooks on every push or pull request.  

### Purpose
- Ensures notebooks run without errors.
- Verifies dependencies in `requirements.txt`.
- Helps maintain reproducibility and clean commits.

### Workflow Details
- Triggered on **push** to `main` and on **pull requests**.
- Runs on **Ubuntu 22.04** with **Python 3.10**.
- Installs dependencies and executes all notebooks in-place.
- Fails the workflow if any notebook has errors, giving immediate feedback.

### Benefits
- Detect errors before collaborators or CI/CD pipelines encounter them.
- Keeps notebooks reproducible without committing outputs (thanks to `nbstripout`).
- Lightweight and automated check for all chapters and experiments.

---

## 📊 Progress Tracker
- [ ] Chapter 1 — The ML Landscape
- [ ] Chapter 2 — End-to-End ML Project
- [ ] Chapter 3 — Classification
- [ ] Chapter 4 — Training Models
- [ ] Chapter 5 — Support Vector Machines
- [ ] Chapter 6 — Decision Trees
- [ ] Chapter 7 — Ensemble Learning
- [ ] Chapter 8 — Dimensionality Reduction
- [ ] Chapter 9 — Unsupervised Learning
- [ ] Chapter 10 — Neural Networks with Keras & TensorFlow
- [ ] Chapter 11
- [ ] Chapter 12
- [ ] Chapter 13
- [ ] Chapter 14
- [ ] Chapter 15
- [ ] Chapter 16
- [ ] Chapter 17
- [ ] Chapter 18
- [ ] Chapter 19

---

## 📌 Recommended Workflow
1. Activate your `hands_on_ml` environment.
2. Open notebooks in **Jupyter Lab** or **VS Code**.
3. Run notebooks locally.
4. Commit code + markdown only — outputs stripped automatically.
5. Push to GitHub.
6. Repeat per chapter or experiment.

---

## 📚 Additional Notes
- Keep experiments separate in `experiments/`.
- Use `datasets/processed/` for small sample files you want to commit.
- Optional: GitHub Actions can automatically run notebooks on push.

