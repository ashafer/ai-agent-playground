# Lab Notebook

Add a dated entry every time you make a change to this repo. Newest entries at the top.

## Example — 2026-01-01 — A. Researcher
- Ran `analysis/summarize.py` for the first time; confirmed the repo and my tool are connected.
- No changes made yet — just checking the pipeline works end to end.

## 2026-09-16 — ashafer
- `analysis/summarize.py` crashed with `KeyError: 'cohort'` at line 14. The script read `row["cohort"]`, but `data/reaction_times.csv` uses the column name `group`, not `cohort`.
- Fixed by changing `row["cohort"]` to `row["group"]` in `load_groups()`.
- Re-ran the script; it now completes successfully:
  - control: n=10, mean=504.7 ms
  - treatment: n=10, mean=430.8 ms

<!-- Add your own entry above this line -->
