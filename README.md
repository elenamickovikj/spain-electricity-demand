# Daily electricity demand in Spain: seasonality, smoothing and decomposition

Time-series analysis of daily electricity demand in Spain (2019–2025, Red Eléctrica de España)
and its relationship with temperature (Open-Meteo). Course project, FINKI – Time Series.

**Methods:** interactive Plotly visualisation; smoothing (SMA, WMA, SES, Holt-Winters, LOWESS);
decomposition (classical, STL, MSTL); experiment tracking with MLflow.

**Main findings:**
- two seasons of similar strength: weekly (0.76) and yearly with winter and summer peaks (0.76); weak long-term trend (0.34)
- the weekly season is multiplicative (Holt-Winters AIC 16255.5 vs 16348.3)
- the largest residuals match real events: the 2020 lockdown, holidays, Storm Filomena, the April 2025 blackout

**Structure:** `notebooks/preprocessing.ipynb` (data download and cleaning), `notebooks/Lab1.ipynb` (analysis),
`reports/hw1/` (PDF report and MLflow screenshot).

**Run:** `pip install -r requirements.txt`, start `mlflow server --backend-store-uri sqlite:///mlflow.db`, then run the notebooks.