# NBA Tanking: A Game Theory & Data Analysis

**[Live interactive explainer →](https://dschell3.github.io/NBATankingAnalysis/tanking_explained.html)**

This project models the strategic incentive to lose games ("tanking") in the NBA draft system using game theory, Monte Carlo simulation, and real lottery data. It also evaluates a structural reform — a "hockey model" borrowed from the PWHL — that inverts the incentive entirely.

## What It Does

The analysis builds from a single-team utility model up to a league-wide simulation, asking: *why does tanking persist, and what kind of rule change would actually stop it?*

The answer isn't about adjusting lottery odds. It's about whether losing games moves your draft position at all.

**Key findings:**
- The NBA's 2019 reform compressed lottery odds but didn't change the structure: (Tank, Tank) remains a Nash equilibrium in nearly all superstar draft years
- Under the hockey model, post-elimination wins — not regular-season losses — determine draft position, making (Tank, Tank) unsatisfiable under any positive utility weights
- Monte Carlo simulation across 1,000 runs confirms: Pre-2019 NBA converges to ~99% tanking, Post-2019 to ~42%, and the hockey model to ~0%
- Retroactive analysis of 2023–2025 data shows the hockey model would have moved picks by an average of 2.3 positions, consistently favoring teams that competed after elimination

## Structure

| File | Description |
|------|-------------|
| [`tanking_explained.html`](tanking_explained.html) | Interactive explainer for a general audience |
| [`nba_tanking_analysis.ipynb`](nba_tanking_analysis.ipynb) | Full technical notebook |

The notebook covers six sections: single-team utility model, two-player prisoner's dilemma, superstar year franchise value extension (with sensitivity analysis), Monte Carlo league dynamics, retroactive hockey model analysis on real NBA data, and a summary of findings.

## Data Sources

- **Draft lottery odds:** NBA official records (pre-2019 and post-2019 formats)
- **Season records and schedule data:** StatMuse schedule pages (2023–2025), fetched via web extraction; mathematical elimination dates determined manually
- **Draft pick surplus value calibration:** Heuristic calibrations consistent with published NBA draft surplus value literature — values are author approximations
- **Revenue calibration:** Forbes annual NBA team valuations (2023–2024); NBA CBA revenue sharing structure (2023 CBA, ~50% BRI pooled); gate revenue estimated from average attendance × median ticket price — all figures are author estimates consistent with public reporting

## Stack

Python (NumPy, Pandas, Matplotlib), Jupyter, JavaScript / HTML / SVG

---

*Darren Schell — [github.com/dschell3](https://github.com/dschell3)*
