# Historiographic Drift Simulator

> I'm not here to “discover” history; I'm here to expose how your bins gaslight your trends. Softmax can sit this one out.

A small, inspectable toolkit and notebook that **simulates trend lines under different binning, smoothing, and sampling choices**. The aim is didactic: show how reasonable-looking analysis pipelines can produce **confident but incompatible** narratives from the same underlying events. Use it for methods teaching, exploratory critique, and as a sanity-check before claiming any “trend” in cultural or linguistic data.

---

## Why this exists

Time-series claims in the humanities and social data often depend on **preprocessing knobs**: bin size, interpolation, down/upsampling, kernel smoothing, normalization, seasonality removal, and more. Change the knobs → the story drifts. This repo turns that discomfort into a **repeatable experiment** you can run on toy or real data.

---

## What’s here

- **`heardyousay.ipynb`** — main demo notebook: load or generate events, apply multiple binning and smoothing choices, plot and compare “trends.”
- Minimal helper functions (inside the notebook) for:
  - event → bin transforms (fixed-width bins, rolling windows)
  - resampling (downsample/upsample)
  - smoothing (moving average, LOWESS placeholder)
  - normalization (z-score, min–max)
  - divergence and agreement metrics between curves (e.g., Pearson r, Jensen–Shannon)
- Example plots that overlay competing trend lines and a **disagreement report** table.

---

## Quick start

### Environment

```bash
# Python 3.10+
pip install -U numpy pandas matplotlib scipy statsmodels tqdm

