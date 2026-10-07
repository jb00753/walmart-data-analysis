# Walmart data analysis

A workspace for exploring Walmart sales data. The dataset and analysis question are still to be confirmed.

## Set up on Windows (PowerShell)

If Anaconda is installed with pandas, NumPy, Matplotlib, Seaborn, and JupyterLab, open an Anaconda Prompt in this folder and run:

```powershell
python -m jupyterlab
```

For a separate environment when package downloads are available:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

If PowerShell blocks activation, use `.\.venv\Scripts\python.exe` in place of `python` without activating the environment.

Place source files in `data/raw/`. Raw data and generated outputs are excluded from Git. Put notebooks in `notebooks/`, reusable code in `src/`, and generated tables or figures in `outputs/`.

## Next steps

1. Confirm and add the intended dataset.
2. Record the data source, fields, and analysis question here.
3. Create an initial exploration notebook once the dataset is known.
