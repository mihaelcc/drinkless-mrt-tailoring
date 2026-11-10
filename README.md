# Notifications Persuade the Already Persuaded — code and results

Reproducibility package for the paper *"Notifications Persuade the Already Persuaded: Decay, Explainable Tailoring and Equity of Engagement Prompts in a Behaviour Change App"* (submitted to PERSUASIVE 2027).

The analysis is a secondary analysis of the open data of the **Drink Less micro-randomized trial** (MRT). No new data were collected.

- Original trial: Bell, L., et al. (2023). How notifications affect engagement with a behavior change app: Results from a micro-randomized trial. *JMIR mHealth and uHealth*, 11, e38342. https://doi.org/10.2196/38342
- Data: Garnett, C., Bell, L., Perski, O., Potts, H., Qian, T. (2022). *MRT: Optimising the notification policy to improve engagement*. Open Science Framework. https://osf.io/w3szp

The data are **not** redistributed here; the notebook downloads them from OSF.

## Contents

| Path | Description |
|---|---|
| `drinkless_mrt_analysis.ipynb` | Full analysis, from data download to every table and figure in the paper |
| `results/` | Outputs of the run reported in the paper (figures, CSV tables, `results_all.json`, `RESULTS_SUMMARY.md`) |
| `requirements.txt` | Python package versions used for the reported run |

## How to run

**Google Colab (recommended).** Open the notebook in Colab and choose *Runtime → Run all*. The run takes about 6–10 minutes on a free CPU runtime. If the automatic OSF download fails, the notebook asks for `w3szp-osfstorage-archive.zip` (OSF → Files → *Download as zip*).

**Locally.** Python ≥ 3.10 and R (`Rscript`, used only to convert the `.rds` files to CSV):

```bash
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute drinkless_mrt_analysis.ipynb
```

All outputs are written to `drinkless_results/` and zipped as `drinkless_results.zip`.

## What the notebook does

| Section | Analysis | Paper |
|---|---|---|
| 1–2 | Data preparation (weekday reconstructed from Dataset B) and descriptives | Sect. 3, Fig. 1 |
| 3 | Causal excursion effects (WCLS, risk difference, cluster-robust SEs) and moderators | Table 1 |
| 4 | Effect by week on the absolute (RD) and relative (RR) scales, cluster bootstrap | Fig. 3 |
| 5 | Moderation by engagement state | Fig. 4 |
| 6 | DR-learner with leave-users-out cross-fitting, five tailoring models, budget-matched gain G(b), calibration | Table 2, Figs. 5–6 |
| 6b | Paired bootstrap of model differences (area under G(b), M3 minus each model) | Sect. 5.3 |
| 7 | Robustness across four random user partitions | Fig. 7 |
| 8 | Explainable rules (M3, M4) and SHAP for M1 | Figs. 8–9 |
| 9 | Allocation of notifications by engagement tertile under M3 at a 40% budget | Fig. 10 |

Random seeds are fixed (7, 11, 23, 101 for the user partitions; 3 and 2027 for bootstrap draws). Small numerical differences may appear with other package versions.

## Licence

Code: MIT (see `LICENSE`). Data remain subject to the terms of the original OSF project; please cite Garnett et al. (2022) and Bell et al. (2023) when using them.
