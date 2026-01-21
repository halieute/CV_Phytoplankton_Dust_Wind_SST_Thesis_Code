# Phytoplankton Response to Environmental Conditions in Cabo Verde

This repository contains the data analysis scripts and visualization tools for the Master's thesis titled **"Response of phytoplankton under varying environmental conditions in Cabo Verde: a seasonal and interannual analysis"** by Souleymane Maman Nouri Souley.

**Institution:** [West African Science Service Centre on Climate Change and Adapted Land Use (WASCAL Cabo Verde School)](https://wascalcv.org/), Institute of Engineering and Marine Sciences, [Atlantic Technical University](https://sga.uta.cv/en), São Vicente, Cabo Verde

## 📋 Overview

This project investigates how phytoplankton communities in the Cabo Verde region respond to varying environmental factors including dust deposition, wind patterns, and sea surface temperature (SST). The analysis spans both seasonal and interannual timescales and examines relationships with large-scale climate modes such as ENSO (El Niño-Southern Oscillation) and NAO (North Atlantic Oscillation).

## 🗂️ Repository Structure

### Jupyter Notebooks

- **[CV1_CV5.ipynb](CV1_CV5.ipynb)** - Comprehensive seasonal variations analysis across different Cabo Verde stations (CV1-CV5) with 2×2 subplot visualizations comparing CHL vs SST, Wind, AOD, and deposition patterns; includes seasonal anomaly calculations with 5-year moving average filter
- **[Correlations_analysis.ipynb](Correlations_analysis.ipynb)** - Correlation analysis between phytoplankton chlorophyll-a and environmental variables (dust, wind, SST) with statistical significance testing
- **[Inter_varia.ipynb](Inter_varia.ipynb)** - Interannual variability analysis of marine productivity and environmental drivers
- **[Large_scale_climate_modes_marine_productivity.ipynb](Large_scale_climate_modes_marine_productivity.ipynb)** - Analysis of relationships between large-scale climate indices (Niño 3.4, NAO) and marine productivity
- **[Seasonal_variability.ipynb](Seasonal_variability.ipynb)** - Seasonal patterns and cycles in phytoplankton and environmental variables
- **[Plotting PCA Explained Variance.ipynb](Plotting%20PCA%20Explained%20Variance.ipynb)** - Visualization of principal component analysis results and variance explained

### Python Scripts

- **[pca_analysis_script_for_cv_box_removed_seasonality_and_with_low_band_pass_filter.py](pca_analysis_script_for_cv_box_removed_seasonality_and_with_low_band_pass_filter.py)** - PCA analysis with seasonality removal and low-pass filtering for identifying dominant modes of variability
- **[por_mes_pca_analysis_script_for_cv_box_with_remove_seasonality.py](por_mes_pca_analysis_script_for_cv_box_with_remove_seasonality.py)** - Monthly PCA analysis with deseasonalized data
- **[stat_dcor.py](stat_dcor.py)** - Statistical independence testing using distance correlation and p-value computation for PCA components

### Study Area

- **Study_area/** - Contains geospatial data and QGIS project files
  - `cabo_verde_study_area.gpkg` - GeoPackage with study area boundaries
  - `cv-phytoplankton-seasonal-interannual.qgz` - QGIS project for visualization

## 🔬 Methodology

### Data Processing
- Time series preprocessing with seasonality removal
- Anomaly detection and detrending
- Low-pass filtering for interannual signals
- Standardization and normalization

### Statistical Analyses
- **Correlation Analysis:** Pearson correlation with significance testing
- **Principal Component Analysis (PCA):** Dimensionality reduction to identify dominant patterns
- **Distance Correlation:** Non-linear statistical independence testing
- **Seasonal Decomposition:** Separation of seasonal and interannual signals

### Environmental Variables
- Chlorophyll-a concentration (proxy for phytoplankton biomass)
- Sea Surface Temperature (SST)
- Wind speed and patterns
- Dust aerosol optical depth and deposition
- Climate indices: Niño 3.4 (ENSO) and NAO

## 🚀 Getting Started

### Prerequisites

```bash
# Core scientific computing
numpy
pandas
scipy

# Visualization
matplotlib
seaborn

# Statistical analysis
scikit-learn
statsmodels

# Specialized libraries
dcor  # Distance correlation
```

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/CV_Phytoplankton_Dust_Wind_SST_Thesis_Code.git
cd CV_Phytoplankton_Dust_Wind_SST_Thesis_Code

# Install required packages
pip install numpy pandas scipy matplotlib seaborn scikit-learn statsmodels dcor
```

### Usage

1. **Correlation Analysis:**
   ```bash
   jupyter notebook Correlations_analysis.ipynb
   ```

2. **PCA with Preprocessing:**
   ```bash
   python pca_analysis_script_for_cv_box_removed_seasonality_and_with_low_band_pass_filter.py
   ```

3. **Seasonal Patterns:**
   ```bash
   jupyter notebook Seasonal_variability.ipynb
   ```

## 📊 Key Features

- **Comprehensive temporal analysis** spanning seasonal to interannual timescales
- **Multi-variable approach** integrating biological, physical, and atmospheric variables
- **Robust statistical methods** with significance testing and uncertainty quantification
- **Geospatial context** with study area visualization tools
- **Reproducible workflows** with documented analysis pipelines

## 📝 Citation

If you use this code or methodology in your research, please cite:

```
Souley, S. M. N. (2025). Response of phytoplankton under varying environmental
conditions in Cabo Verde: a seasonal and interannual analysis.
Master's Thesis, Atlantic Technical University, São Vicente, Cabo Verde.
```

## 📄 License

This project is licensed under the MIT License - see the [License](License) file for details.

## 👤 Author

**Souleymane Maman Nouri Souley**
[West African Science Service Centre on Climate Change and Adapted Land Use (WASCAL Cabo Verde School)](https://wascalcv.org/)
Institute of Engineering and Marine Sciences
[Atlantic Technical University](https://sga.uta.cv/en)
São Vicente, Cabo Verde

## 🙏 Acknowledgments

Special thanks to the supervisors, WASCAL, and institutions that provided data and support for this research.

---

*For questions or collaboration inquiries, please open an issue or contact the author.*