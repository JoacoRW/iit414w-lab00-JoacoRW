# README.md - The Runbook

## (a) Header
- Full name: Joaquin Tomas Rodriguez Woca.
- GitHub username: JoacoRW
- Course code: IIT414W
- Date: 2026-03-06

## (b) System Info
- Operating system: Microsoft Windows 11 Home Single Language (Version 10.0.26200)
- Python version: 3.13.12
- pip version: 26.0.1

## (c) Setup Instructions
Run these commands exactly in PowerShell.

1. Open PowerShell and move to your repo folder:
```powershell
cd "C:\Users\joaqu\OneDrive\Documentos\GitHub\iit414w-lab00-JoacoRW"
```

2. Create a virtual environment:
```powershell
py -3.13 -m venv .venv
```

3. Activate the environment:
```powershell
.\.venv\Scripts\Activate.ps1
```

4. Upgrade pip inside the virtual environment:
```powershell
python -m pip install --upgrade pip
```

5. Install dependencies from `requirements.txt`:
```powershell
pip install -r requirements.txt
```

6. (Optional check) Verify versions:
```powershell
python --version
pip --version
```

## (d) How To Run

run:
```powershell
jupyter lab
```
Then open the notebook and run cells from top to bottom.

## (e) Problems Encountered
1. Problem: I initially used commands outside the project environment, which risked installing packages globally instead of the class venv.
   Fix: I explicitly created and activated `.venv` and confirmed `python --version` and `pip --version` before installing.

2. Problem: FastF1 cache path was not guaranteed to exist on a fresh setup.
   Fix: The notebook creates the cache directory with `os.makedirs(..., exist_ok=True)` before enabling cache.

## (f) Expected Outputs
A successful run should look like this:
- Reproducibility header prints Python, NumPy, and seed values.
- Dependency guard reports installed packages (or installs missing ones).
- Environment verification prints a package/version table and Git info.
- FastF1 session loads and displays lap tables/plots.
- The run completes without `ModuleNotFoundError` or `NotImplementedError` in completed cells.
