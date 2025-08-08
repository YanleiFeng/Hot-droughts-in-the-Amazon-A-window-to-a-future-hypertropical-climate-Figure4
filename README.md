
# Reproducing Figure 4 (Panels a–c)

This repository contains the analysis code and workflows to generate **Figure 4a**, **4b**, and **4c** from the paper titled Hot droughts in the Amazon:
A window to a future hypertropical climate (Chambers et al. 2025).

---

## Dependencies

All analyses were conducted using **Python 3.8+** and require the following packages:

- `numpy`
- `matplotlib`
- `xarray`
- `rioxarray`
- `rasterio`
- `seaborn`
- `pandas`
- `cartopy`

---

## Figure Descriptions & Reproduction Steps

### Figure 4a: Area Change Comparison Between Historical and Future Periods

Calculates and visualizes the change in total land area classified as hypertropical across 10 climate models, comparing historical vs. future (e.g., SSP585) scenarios.

---

### Figure 4b: Time Series of Hypertropical Land Area (SSP126, SSP370, SSP585)

Analyzes the year-by-year trend in hypertropical land area under different SSPs using percentile-based binning of historical temperature and precipitation data.

---

### Figure 4c: Spatial Overlap of Hypertropical Regions Across Models

Generates a global map showing model agreement on where hypertropical regions are projected to occur under future scenarios.

---
## Notes

- Make sure all NetCDF files are regridded to the same spatial resolution before analysis.
- Spatial raster masks must align across models for overlap computation in Figure 4c.
- All outputs can be saved using `plt.savefig(...)` as shown in the notebooks.

