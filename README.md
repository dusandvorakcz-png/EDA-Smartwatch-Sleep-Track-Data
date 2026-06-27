# Exploratory Data Analysis: Smartwatch Sleep Tracking

An exploratory data analysis (EDA) of a synthetic smartwatch sleep dataset,
investigating what is associated with longer deep sleep.

## Project Question
**What factors are associated with longer deep sleep (in minutes)?**

I created a target variable, `deep_sleep_minutes`, from total sleep duration and
the deep-sleep percentage, then tested it against demographic, lifestyle, and
physiological variables.

## Key Findings
- Deep sleep is bell-shaped with a slight right skew; the median night has about
  79 minutes, and ~39% of nights fall between 60 and 90 minutes.
- **No relationship with age** (r = 0.01) — notable, since real-world deep sleep
  declines with age, suggesting this synthetic data did not encode that pattern.
- **No lifestyle factor is associated with deep sleep** — caffeine, alcohol,
  stress, screen time, and exercise all correlate near zero.
- The only meaningful link is with overall **sleep score** (r = 0.27).
- The strongest relationship in the dataset is sleep score vs sleep efficiency
  (r = 0.60), and the data did encode one realistic medical link: weight vs
  apnea risk (r = 0.8).

**Conclusion:** In this synthetic dataset, deep sleep tracks overall sleep
quality but is not driven by any measurable behaviour or demographic. All
relationships are correlational, not causal.

## Tools
Python, pandas, NumPy, Matplotlib, Seaborn (in Google Colab). Data loaded via
the Kaggle API (`kagglehub`).

## Dataset
- 20,000 synthetic sleep sessions from 2,000 users (2018–2025), 45 columns.
- Fully synthetic and privacy-safe; no real user data.
- Source: [Smartwatch Sleep Tracking Dataset on Kaggle](https://www.kaggle.com/datasets/mirzayasirabdullah07/smartwatch-sleep-tracking-dataset-20182025)

## Running the notebook
This notebook loads the data through the Kaggle API. To run it yourself, add your
own Kaggle token in Colab (Secrets → `KAGGLE_API_TOKEN`), or download the CSV
directly from the Kaggle link above.

## Credit
Dataset by Abdullah, Y. (2025), *Smartwatch Sleep Tracking Dataset (Synthetic,
2018–2025)*, released under CC BY 4.0.
