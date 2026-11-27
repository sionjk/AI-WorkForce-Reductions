# AI and global workforce reductions

This notebook analyzes 2,470 records of reported tech layoffs from March 2020 through April 2026 and examines what employers said about AI in the 18 March 2026 records.

**Start here.** Open [COP 4283 Final Project.ipynb](Final%20Project/COP%204283%20Final%20Project.ipynb). Sections 9–11 contain the timeline, industry ranking, and March evidence. Section 13 summarizes the findings.

## Run the notebook

1. Extract the ZIP. Open a terminal in the folder containing this README.
2. With Python 3 installed (tested with 3.14), run the following commands.

   ```sh
   python -m pip install jupyterlab "pandas>=2" scipy "altair>=6,<7" "vl-convert-python>=1.9,<2"
   python -m jupyterlab
   ```

3. In JupyterLab, open `Final Project/COP 4283 Final Project.ipynb` from the file browser. Choose **Kernel → Restart Kernel and Run All Cells**. Expand the control beneath each saved figure to use its filters or read the March sources.

## Files and sources

All data files are in the `Final Project` folder beside the notebook. The analysis runs from these local files.

| File | Purpose |
| --- | --- |
| `layoffs_events.csv` | Source records for the timeline and industry comparisons. |
| `march_2026_evidence.csv` | Group-reviewed classifications, explanations, and source links for March. |
| `us_labor_indicators.csv`, `global_labor_indicators.csv`, `news_sentiment.csv` | Background datasets cleaned in Sections 4–5. |
| `layoffs_clean.csv` | Cleaned event data included for inspection. Section 8 regenerates this file, three other cleaned tables, and three summaries. |

The four source datasets come from Belbino’s Kaggle collection, which draws on Layoffs.fyi, FRED, the World Bank, and NewsAPI. The project group reviewed the March evidence separately. [Kaggle dataset](https://www.kaggle.com/datasets/belbino/global-ai-layoffs-and-job-market-2020-present/data)
