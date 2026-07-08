# Python Environment Setup Notes

## 1. Creating a Conda Environment
conda create -p venv python==3.10 -y
- `-p venv` → creates environment in current folder (path-based, not global)
- `python==3.10` → installs Python 3.10 in this environment
- `-y` → auto-confirms all prompts

## 2. Virtual Environment
An isolated environment where project-specific libraries are installed, 
separate from the system Python and other projects. Prevents version conflicts 
between different projects.

## 3. requirements.txt
A text file listing all libraries + versions needed for a project.
Example:
numpy==1.24.0
pandas==2.0.1
Install all at once using:
pip install -r requirements.txt

## 4. CMD vs PowerShell
- CMD works smoothly with conda/venv activation.
- PowerShell often blocks scripts due to execution policy, causing activation errors.
- Recommended: use CMD for conda/venv work.

## 5. ipykernel
Connects the virtual environment to Jupyter Notebook so it appears as a 
selectable kernel.
pip install ipykernel
python -m ipykernel install --user --name=venv

## 6. Types of Virtual Environments
- venv (Python built-in)
- conda (best for data science/ML)
- virtualenv (older, third-party)
- pipenv
- poetry

## 7. python --version
Checks which Python version is currently active — used to confirm the 
correct environment is activated.