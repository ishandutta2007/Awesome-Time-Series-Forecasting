# Awesome-Time-Series-Forecasting

## Top Time Series Forecasting Tools Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Foundation Models, Automated ML & Multivariate Forecasting*  

**Last updated: March 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Time Series Forecasting**. These tools predict future values of sequentially indexed data — sales, demand, traffic, inventory, and sensor readings — using statistical methods, automated machine learning, and increasingly, foundation models that forecast zero-shot without task-specific training.



**Examples** include DataRobot, H2O.ai, Pecan AI, AWS Forecast, Azure Automated ML, Databricks, BigML, dotData, Akkio, and RapidMiner (the category leaders).



**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, foundation-model forecasting, and transparent time-series pipelines — ideal for data scientists prioritizing reproducibility, developers building forecasting services, and organizations avoiding per-model enterprise pricing.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[DataRobot](https://www.datarobot.com/)**  

  Enterprise AutoML platform with strong time-series forecasting capabilities. Automatically detects stationarity and seasonality and implements backtesting to achieve high accuracy . Uses open-source algorithms including scikit-learn, H2O, TensorFlow, and XGBoost . Pricing starts at **$65,000/year for 5 users, 10 model workers, and 5 deployed models** . Often perceived as expensive for smaller teams, with seat-based limits around 5 users per license . No built-in ETL — users must prepare data elsewhere .



- **[H2O.ai Driverless AI](https://h2o.ai/platform/dai-timeseries/)**  

  AutoML platform with comprehensive time-series capabilities. Handles automatic time groups, robust validation without data leakage, time-series-specific feature engineering, and integration with existing feature engines . Features include date features (day of week, day of month), auto-regressive features (optimal lag, lag-feature interaction), exponentially weighted moving averages, target transformations, and differentiation . **Fast TTA** (Test Time Augmentation) applies regularization during prediction for production stability — disable for regulatory compliance requiring deterministic outputs .



- **[Pecan AI](https://www.pecan.ai/)**  

  Predictive AI agent built for business outcomes, delivering predictions directly to CRM without requiring a data science team . Handles churn prediction, LTV modeling, lead scoring, demand forecasting, upsell/cross-sell, winback, fraud prevention, and campaign ROAS prediction . Reports average results including **12% churn reduction**, **15% marketing ROAS improvement**, **25% inventory cost reduction**, and **90% of predictions delivered without data science support** . Plans: **Starter** (2 prediction batches/month, 500M rows), **Team** (10 batches, 2B rows), and **Business** (custom, 5B rows) .



- **[Amazon Forecast](https://aws.amazon.com/forecast/)**  

  Fully managed service using statistical and ML algorithms for high-accuracy forecasting, based on the same technology used at Amazon.com . Automates algorithm selection via AutoML, handles missing values with multiple imputation methods, and integrates built-in datasets . Use cases span retail demand planning, supply chain, resource planning, and operational planning . **No longer available to new customers** — existing customers continue as normal . Pricing is usage-based with no minimum; free tier includes 10,000 forecasts/month, 10GB storage, and 10 hours training for the first two months .



- **[Azure Automated ML](https://azure.microsoft.com/en-us/products/machine-learning/)**  

  Automated machine learning within Azure Machine Learning for time-series forecasting. Supports "pivoted" time-series formulation where past values become additional dimensions for regressors, with separate train and validation set specification . Models are serialized as Python pickle files, with documented procedures for local deployment .



- **[Databricks AutoML Forecasting](https://docs.databricks.com/)**  

  AutoML forecasting via the Databricks Model Training UI or Python API (`databricks.automl.forecast()`) . Requires training data with a time-series column saved as a Unity Catalog table. Supports multi-series forecasting with time-series identifier columns, custom data splits, weight columns, holiday regions, and timeout configuration . Runs on fully-managed compute, registers models to Unity Catalog, and generates batch inference notebooks automatically .



- **[BigML Time Series](https://bigml.com/)**  

  Optimized implementation of **exponential smoothing methods** (ETS) for time-series forecasting . Assigns exponentially increasing weights to more recent instances, modeling trend and seasonal patterns . Handles missing values via spline interpolation by default . Supports **univariate and multivariate** time series, with model parameters including alpha, beta, gamma, phi, and period exposed via API . Outputs include point forecasts, 95% confidence bounds, and ETS model classification (e.g., M,Ad,N) .



- **[dotData](https://dotdata.com/)**  

  Automated feature discovery platform for time-series forecasting. A national healthcare company using Facebook Prophet increased **forecast accuracy by 20%** in 3 days with dotData — discovering **67,000 multi-dimensional features** and testing **700 ML models** by a single data scientist . **dotData Insight 3.0** (September 2026) integrates AutoML prediction capabilities with feature discovery, adding offline installation support, Microsoft Entra ID SSO, and pivot analysis visualization .



- **[Akkio](https://www.akkio.com/)**  

  No-code AI platform for forecasting revenue, costs, commodity prices, and market trajectory . Builds models in as little as **10 seconds** (optional 1-5 minute training for potentially higher accuracy) with no charge for model training time . Deploys via API, Salesforce, Zapier, or web app. Includes confidence bounds visualization and accuracy metrics . Targets non-technical teams and agencies.



- **[RapidMiner](https://rapidminer.com/)**  

  Data science platform with a **Time Series extension** (AGPL licensed) adding operators for transformations, filtering, decomposition, feature extraction, forecasting, windowing, validation, and more . Supports multivariate time series with multiple attributes processed simultaneously, and index attributes of datetime or numeric type .



## Open-Source GitHub Projects



- **[TimesFM](https://github.com/google-research/timesfm)**  

  **Google Research's time-series foundation model** — the leading open-weight forecasting model. **TimesFM-3** (330M parameters) is pre-trained on **1 trillion+ time points** and is natively multivariate . Supports multiple targets (jointly forecasting related series), past covariates (historically known features), and past-future covariates (known future events like promotions or holidays) . Uses **Contiguous Patch Masking** for single-pass forecasting without autoregressive iteration, predicting **9 quantiles** (10th-90th percentile) for each target . Zero-shot forecasting without task-specific fine-tuning. Available on Hugging Face.



- **[sktime](https://github.com/sktime/sktime)**  

  **Unified framework for time-series machine learning** with a scikit-learn-compatible API. Provides forecasting, classification, regression, clustering, and annotation for time series. Includes a large ecosystem of algorithm adapters (statsmodels, Prophet, ARIMA, exponential smoothing) and transformation tools. BSD-3-Clause licensed.



- **[StatsForecast](https://github.com/Nixtla/statsforecast)**  

  **Lightning-fast statistical forecasting library** from Nixtla. Implements ARIMA, ETS, CES, Theta, and other classical models with **native parallelism** via numba. Handles multiple seasonalities and high-frequency data. Designed for performance on large-scale forecasting tasks. Apache 2.0 licensed.



- **[NeuralForecast](https://github.com/Nixtla/neuralforecast)**  

  **Deep learning forecasting library** from Nixtla. Implements NBEATS, NHITS, TFT, PatchTST, TimesNet, and other neural architectures with a unified API. Supports exogenous variables, static features, and probabilistic forecasting. Apache 2.0 licensed.



- **[Prophet](https://github.com/facebook/prophet)**  

  **Meta's additive regression model** for forecasting with daily observations. Handles missing data, shifts in trend, and multiple seasonality (daily, weekly, yearly) with interpretable parameters. Includes holiday effects and changepoint detection. MIT licensed. Widely used but has known limitations for multi-dimensional forecasting .



- **[Darts](https://github.com/unit8co/darts)**  

  **User-friendly forecasting and anomaly detection library** for Python. Provides a consistent API for classical (ARIMA, ETS) and deep learning (RNN, TCN, Transformer) models, with built-in backtesting, ensemble methods, and probabilistic forecasting. Apache 2.0 licensed.



- **[GluonTS](https://github.com/awslabs/gluonts)**  

  **Probabilistic time-series modeling toolkit** from AWS. Provides deep learning models (DeepAR, Transformer, WaveNet) and classical models with a unified probabilistic API. Powers Amazon Forecast under the hood. Apache 2.0 licensed.



- **[PyTorch Forecasting](https://github.com/jdb78/pytorch-forecasting)**  

  **Deep learning for time-series forecasting in PyTorch.** Implements Temporal Fusion Transformer (TFT), NBEATS, DeepAR, and other architectures with a high-level API built on PyTorch Lightning. Handles covariates, static features, and multi-horizon forecasting.



- **[tsfresh](https://github.com/blue-yonder/tsfresh)**  

  **Automatic extraction of 750+ time-series features** for regression and classification. Includes feature selection based on statistical significance. MIT licensed. Useful for feature engineering pipelines feeding into tree-based forecasters.



- **[ETNA](https://github.com/tinkoff-ai/etna)**  

  **Time-series analysis library** from Tinkoff with a focus on practical forecasting. Provides EDA tools, classical and neural models, backtesting, and pipeline composition. Apache 2.0 licensed.



### Additional Strong Open-Source Options



- **Kats** — Meta's lightweight, generalizable framework for time-series analysis including forecasting, detection, and feature extraction.

- **Orbit** — Uber's Python library for Bayesian time-series forecasting with probabilistic modeling and inference.

- **pmdarima** — Python wrapper for R's auto.arima, providing automated ARIMA model selection.

- **PyOD** — Python Outlier Detection toolkit useful for anomaly detection in time-series data.

- **Merlion** — Salesforce's time-series anomaly detection library with autoML capabilities.

- **Greykite** — LinkedIn's flexible forecasting library with interpretable models.



**Frameworks for building custom systems**: Combine **TimesFM** for zero-shot multivariate forecasting, **StatsForecast** or **NeuralForecast** for specialized classical and deep learning models, **sktime** or **Darts** for unified experimentation, and **tsfresh** for automated feature engineering to build a complete open-source forecasting stack.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Time-series forecasting tools involve statistical modeling and uncertainty quantification. **Forecasts are probabilistic estimates, not guarantees** — confidence bounds should be communicated to stakeholders, and predictions should be validated against actual outcomes for monitoring drift. Foundation models provide strong zero-shot baselines but may underperform domain-specific fine-tuned models on niche tasks.

- Self-hosted open-source solutions require proper data pipeline integration, model monitoring, and retraining strategies for production use.



---



**Made for data scientists, ML engineers, demand planners, and developers building time-series forecasting platforms.**  

Let's make time-series forecasting more open, accurate, and reproducible.
