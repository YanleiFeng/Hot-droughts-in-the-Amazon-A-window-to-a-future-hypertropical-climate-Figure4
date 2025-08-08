# README: Reproducing Figure 4 (Panels a–c)

This repository contains the analysis code and workflows to generate **Figure 4a**, **4b**, and **4c** from the study on hypertropical region changes under historical and future climate scenarios.

---

## 🔧 Dependencies

All analyses were conducted using **Python 3.8+** and require the following packages:

- `numpy`
- `matplotlib`
- `xarray`
- `rioxarray`
- `rasterio`
- `seaborn`
- `pandas`
- `cartopy`

You can install all required packages using:

```bash
pip install numpy matplotlib xarray rioxarray rasterio seaborn pandas cartopy
```

---

## 📊 Figure Descriptions & Reproduction Steps

### ▶️ Figure 4a: Area Change Comparison Between Historical and Future Periods

**Notebook**: `Fig4a_AreaChange_Hypertropics_WithSections.ipynb`

**Purpose**:  
Calculates and visualizes the change in total land area classified as hypertropical across 10 climate models, comparing historical vs. future (e.g., SSP585) scenarios.

**Inputs**:  
- Raster masks representing hypertropical regions for each model and scenario
- Masked land surface data (`sftlf`)

**How to Run**:
1. Update the file paths to the raster datasets.
2. Run the notebook to generate a bar plot comparing area changes across models.

---

### ▶️ Figure 4b: Time Series of Hypertropical Land Area (SSP126, SSP370, SSP585)

**Notebook**: `Fig4b_Hypertropics_SSP_Trends_Documented.ipynb`

**Purpose**:  
Analyzes the year-by-year trend in hypertropical land area under different SSPs using percentile-based binning of historical temperature and precipitation data.

**Inputs**:
- Historical and future temperature (`tas`) and precipitation (`pr`) data
- A land mask (`sftlf`) to restrict analysis to terrestrial areas

**How to Run**:
1. Load or download `tas`, `pr`, and `sftlf` data in NetCDF format.
2. Run the notebook to generate time series plots of hypertropical area fractions for each scenario.

---

### ▶️ Figure 4c: Spatial Overlap of Hypertropical Regions Across Models

**Notebook**: `Figure4c_Code_Hypertropics_Documented.ipynb`

**Purpose**:  
Generates a global map showing model agreement on where hypertropical regions are projected to occur under future scenarios.

**Inputs**:
- Binary raster masks from multiple climate models

**How to Run**:
1. Set paths to the model-specific raster mask files.
2. Run the notebook to produce an overlay map with model agreement visualization.

---

## 📁 Folder Structure

```bash
.
├── Fig4a_AreaChange_Hypertropics_WithSections.ipynb
├── Fig4b_Hypertropics_SSP_Trends_Documented.ipynb
├── Figure4c_Code_Hypertropics_Documented.ipynb
├── data/  # <-- Place your input NetCDF and raster files here
└── README.md
```

---

## 📌 Notes

- Make sure all NetCDF files are regridded to the same spatial resolution before analysis.
- Spatial raster masks must align across models for overlap computation in Figure 4c.
- All outputs can be saved using `plt.savefig(...)` as shown in the notebooks.

