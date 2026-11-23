# Stock and ETF Directional Forecasting

Research archive comparing **DLinear, LSTM and TCN** for directional forecasting of US stocks and ETFs. The daily study uses AAPL, MSFT, JPM, JNJ and WMT; the intraday study uses EEM.

## Paper

[Full manuscript (PDF)](paper/manuscript.pdf) · [Editable manuscript](paper/manuscript.docx)

*Directional Forecasting of Stocks and ETFs with Temporal Deep Learning Models*, Yi Kang and Yancong Deng.

## Contents

| Folder | Contents |
| --- | --- |
| `daily/` | Five-stock robustness notebook and the five daily OHLCV source files |
| `intraday/` | Five-minute and ten-minute experiments, raw EEM observations and the cleaned five-minute table |
| `results/` | Archived study summaries; `original/` preserves the original paper tables |
| `paper/` | Full manuscript |

## Running the experiments

Use Python 3.11 and install `requirements.txt`. Open each notebook with its own directory as the working directory:

- `daily/robust_test.ipynb`: 60-day histories, five-day forward return-sign targets, chronological train/validation/test splits and three neural models.
- `intraday/5min-0405.ipynb`: the supplied cleaned EEM five-minute series and multiclass threshold experiments.
- `intraday/10min-0426-advisor.ipynb`: raw EEM loading, data auditing and five-/ten-minute extensions. The archive defaults to EEM only. Additional ETF experiments require their separate raw files before adding symbols to `SELECTED_ADDITIONAL_ETFS`.

The notebooks include complete training loops. Running them takes substantially longer than loading the archived result tables.

## Reproducibility

The selected daily and EEM inputs are included. The daily feature pipeline was executed for all five stocks, and forward passes of all three model classes were checked. Full training was **not rerun** during archive preparation.

Exact recovery of the original manuscript metrics is **not established**: the historical study and later notebook revisions differ, and neural training depends on seeds, software versions and hardware. Archived original tables are retained rather than replaced by results from a different experiment. Additional market-wide datasets and large intermediate arrays are excluded.

Code comments and documentation are in English. Original column names, runtime messages and the manuscript are preserved. Market observations retain their original provider context; this archive does not grant a separate data redistribution license.
