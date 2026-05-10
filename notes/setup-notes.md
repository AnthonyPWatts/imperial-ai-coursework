# Imperial AI Course – Environment Setup Notes

## Machine

Primary study laptop for Imperial AI course.

### Hardware
- Intel i7 laptop
- 24GB RAM
- Windows 11
- VS Code-based workflow

### Remote Capability
- RustDesk available
- Desktop workstation available for heavier workloads if needed

---

# Workspace Structure

Root folder:

```text
C:\_Source\ImperialAI
```

Subfolders:

```text
notes/
labs/
scratch/
math-refresh/
experiments/
capstone/
```

---

# Python Environment

## Current Status

Using local virtual environment:

```text
.venv
```

Currently based on:

```text
Python 3.13.13 (Anaconda-distributed)
```

This is acceptable for now because:
- notebook execution works
- numpy/pandas/sklearn import successfully
- local venv isolation is functioning

Potential future improvement:
- replace with clean CPython 3.12 install if compatibility issues appear later

---

# Core Packages Installed

Installed packages include:

- numpy
- pandas
- matplotlib
- scikit-learn
- scipy
- jupyter
- notebook
- ipykernel
- seaborn
- plotly
- requests
- openpyxl

---

# VS Code Extensions

Installed extensions:

- Python
- Pylance
- Jupyter
- GitLens
- Markdown All in One

Optional future additions:
- GitHub Copilot
- Continue.dev

---

# Notebook Kernel

Kernel currently in use:

```text
.venv (Python 3.13.13)
```

Verified working with:
- numpy imports
- pandas imports
- sklearn imports
- notebook execution

---

# Commands That Worked

## Create venv

```powershell
python -m venv .venv
```

## Activate venv

```powershell
.venv\Scripts\activate
```

## Install core packages

```powershell
pip install numpy pandas matplotlib scikit-learn scipy jupyter ipykernel notebook
```

## Install additional packages

```powershell
pip install seaborn plotly requests openpyxl
```

## Register notebook kernel

```powershell
python -m ipykernel install --user --name imperial-ai --display-name "Imperial AI"
```

---

# Issues Encountered

## Python version confusion

Initial confusion caused by:
- VS Code selecting Anaconda-backed interpreter
- local venv inheriting Anaconda Python 3.13

Resolution:
- accepted current working state
- prioritised progress over environment perfectionism

---

# Validation Performed

Environment test notebook successfully executed:

```python
import numpy as np
import pandas as pd
import sklearn
```

Confirmed:
- notebook execution works
- package imports work
- VS Code kernel selection works

---

# Future Improvements

Possible later tasks:

- Install clean CPython 3.12
- Rebuild venv from official Python
- Add GitHub repo
- Configure Copilot
- Add Ruff/Black formatting
- Explore PyTorch/TensorFlow
- Add remote Jupyter workflows from desktop GPU machine

---

# Important Reminder

Do not descend into infinite tooling optimisation.

Priority is:
1. learning
2. experimentation
3. maths fluency
4. implementation practice

Environment perfection is secondary.