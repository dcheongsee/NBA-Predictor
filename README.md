# 🏀 NBA Game Outcome Predictor

Predicts whether the **home team** wins an NBA game from a minimal set of box‑score stats.

**Tech stack:** Python · Pandas · Scikit‑learn · Google Colab



## At a glance

<small>
<table style="border-collapse:collapse;border:0;border-top:0;">
  <tr style="border-top:0;">
    <th align="left" style="border:0;border-top:0;background:#fff;">
      Data
    </th>
    <td style="border:0;border-top:0;background:#fff;">
      26 000+ games (2004 – 2020) from public box-score archives
    </td>
  </tr>
  <tr>
    <th align="left" style="border:0;background:#fff;">
      Pre-processing
    </th>
    <td style="border:0;background:#fff;">
      Full-row NaN purge · automatic binary <strong>Win</strong> label generation
    </td>
  </tr>
  <tr>
    <th align="left" style="border:0;background:#fff;">
      Features
    </th>
    <td style="border:0;background:#fff;">
      FG % (home & away) · rebounds (home) · assists (home)
    </td>
  </tr>
  <tr>
    <th align="left" style="border:0;background:#fff;">
      Model
    </th>
    <td style="border:0;background:#fff;">
      Random Forest, 100 trees, <code>max_depth=None</code>
    </td>
  </tr>
  <tr>
    <th align="left" style="border:0;background:#fff;">
      Validation
    </th>
    <td style="border:0;background:#fff;">
      Stratified 20 % hold-out · <strong>79 % accuracy</strong>
    </td>
  </tr>
  <tr>
    <th align="left" style="border:0;background:#fff;">
      Diagnostics
    </th>
    <td style="border:0;background:#fff;">
      Confusion-matrix heat map to verify class balance
    </td>
  </tr>
  <tr>
    <th align="left" style="border:0;background:#fff;">
      Extras
    </th>
    <td style="border:0;background:#fff;">
      Match-up Simulator – plug your stats ⇒ instant W/L call
    </td>
  </tr>
</table>
</small>




## Quick start (Colab)

Click the badge or run:

```bash
!git clone https://github.com/dcheongsee/NBA‑Predictor.git
```

Open `NBA_Predictor.ipynb` in Colab and execute **Run All** – the notebook rebuilds the entire pipeline end‑to‑end in under two minutes on free tier hardware.

## Local run

```bash
python -m venv .venv && source .venv/bin/activate
pip install pandas scikit-learn matplotlib notebook
jupyter notebook NBA_Predictor.ipynb
```

## Repository layout

```
.
├── NBA_Predictor.ipynb   # Reproducible workflow
|                         # CLI + Match‑up simulator
├── nba_games.csv         # cached CSV
└── README.md
```

## Results

* Accuracy   **79 %**
* F1‑score   0.78

See `NBA_Predictor.ipynb` for full metrics.

## Why it matters

A compact but end‑to‑end example of sports analytics: raw CSV ingestion through cleaning, feature engineering, modelling and live inference. Reproducible in a single notebook.

## License

MIT-licensed. Keep the copyright header, otherwise do whatever you like
