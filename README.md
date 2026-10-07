# Walmart data analysis

A workspace for exploring the M5 Walmart sales dataset. The project questions are in [docs/questions.md](docs/questions.md).

For local database setup, see [docs/postgresql_setup.md](docs/postgresql_setup.md).

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

The dataset is stored locally in `data/raw/m5-forecasting-accuracy/`:

| File | Contents |
| --- | --- |
| `calendar.csv` | Dates, week identifiers, events, and SNAP flags |
| `sell_prices.csv` | Weekly item prices by store |
| `sales_train_validation.csv` | Daily unit sales through the validation period |
| `sales_train_evaluation.csv` | Daily unit sales through the evaluation period |
| `sample_submission.csv` | Forecast submission format |

Raw data and generated outputs are excluded from Git. Put notebooks in `notebooks/`, reusable code in `src/`, and generated tables or figures in `outputs/`.

To check the files from Python:

```python
from pathlib import Path
import pandas as pd

data_dir = Path("data/raw/m5-forecasting-accuracy")
calendar = pd.read_csv(data_dir / "calendar.csv")
sales_sample = pd.read_csv(data_dir / "sales_train_evaluation.csv", nrows=100)
print(calendar.shape, sales_sample.shape)
```

The sales tables have more than 1,900 columns, so start with a small sample before loading a full table into memory.

## Next steps

1. Work through the questions in [docs/questions.md](docs/questions.md) at your own pace.
2. Record the original dataset source and any assumptions here.
3. Create an exploration notebook in `notebooks/`.
