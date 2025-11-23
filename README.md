The Widening Gap: Why Rising Female Secondary Education Fails To Translate into Labor Force Inclusion (1990–2019)

**Repository overview**
This repository contains the code, visualizations, and final report for an exploratory visual analysis of the relationship between female secondary school enrollment and female labor force participation across countries (1990–2019). The analysis uses World Bank World Development Indicators and focuses on iterative visualization (small multiples, time-series, and slope graphs) to reveal regional differences and the emergence of a widening gap between education and labor participation.

**Final report (PDF)**
The complete write-up, figures, and reflections are included in the PDF:
`/mnt/data/data viz.pdf`. 

**Contents**

* `README.md` — this file.
* `data/` — (instructions below) where extracted CSVs or merged datasets should go.
* `notebooks/` — Jupyter/Colab notebooks used for data cleaning and plotting.
* `figures/` — final PNG/SVG figures referenced in the report.
* `report/` — the PDF report and any supplementary documentation.


## Key files & figures

* `report/data viz a4 redo.pdf` — full paper and figures. 
* `notebooks/analysis.ipynb` — notebook that downloads World Bank indicators, cleans, creates the three main visualizations (panel bubble plots for 1990/2005/2019, global weighted trend lines, regional LFP comparison), and exports figures.
* `figures/figure1_panel_scatter.png` — Small multiples: Education vs. Labor Participation (1990, 2005, 2019).
* `figures/figure2_global_trends.png` — Global population-weighted trend lines (1990–2019).
* `figures/figure3_regional_lfp.png` — Regional comparison of female labor force participation (1990–2019).
* `figures/figure4_slope_graph.png` — Final slope graph: regional changes in LFP (1990 → 2019).

*(If any of the above files are missing, run the notebook to regenerate them.)*


## Data sources

Primary data are from the World Bank World Development Indicators (WDI). Indicators used:

* **Female labor force participation rate (% of female population ages 15+)** — `SL.TLF.CACT.FE.ZS`
* **Female secondary school enrollment (% net)** — `SE.SEC.NENR.FE`
* **Population, total** — `SP.POP.TOTL` (used for population-weighted aggregation and bubble sizes)
* **GDP per capita (current US$)** — `NY.GDP.PCAP.CD` (contextual)


## Reproduce the analysis (Colab / local instructions)

1. Clone this repository to your local machine or open it in Google Colab.
2. Install dependencies (if running locally):

```bash
pip install pandas matplotlib seaborn requests
```

3. Open `notebooks/analysis.ipynb` (or run the single script `notebooks/run_analysis.py`) and run cells in order. The notebook will:

   * Download the four World Bank indicators (1990–2019)
   * Clean and merge datasets (melt/pivot, align years, map regions)
   * Compute population-weighted global & regional averages
   * Produce and save the figures under `figures/`
4. Review the final report PDF for narrative, captions, and reflections:
   `/mnt/data/data viz a4 redo.pdf`. 

## Notes on design & methodology

* The analysis follows an **iterative visualization** workflow: cross-sectional exploration → temporal (global averages) → regional contextualization → final slope graph.
* Visual encodings emphasize **position** for quantitative comparison and **faceting (small multiples)** to reduce overplotting and cognitive load.
* All plots are reproducible and use population-weighted aggregation to reflect country size in global/regional trends.


## How to cite / attribution

If you reuse the figures or analysis, please cite the report in this repository (the PDF) or contact the author for permission.


## License

This project is provided for academic purposes. If you want to use the code or visual assets for publication or commercial use, please contact the author to discuss licensing.
