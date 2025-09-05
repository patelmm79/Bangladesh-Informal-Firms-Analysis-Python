# Bangladesh Informal Firms Analysis - Python Version

This is a Python conversion of the original R-based analysis of World Bank Bangladesh Informal Firms Survey data from 2010.

## Project Structure

- `Bangladesh_Informal_Firms_Analysis.ipynb` - Part 1: Geographic analysis, revenue distributions, and ISIC classifications
- `Bangladesh_Analysis_Part2.ipynb` - Part 2: Business size analysis, financing sources, and final plots
- `requirements.txt` - Python dependencies
- Data files:
  - `informality_data_NEW.csv` - Main survey data
  - `surveydata_with_ISIC.csv` - Survey data with ISIC classifications
  - `ISIC_Rev_3_english_structure.csv` - Industry classification reference
  - `shp/` directory - Bangladesh district boundary shapefiles
  - `Sources of Information.txt` - Data source documentation

## Setup

1. Install Python dependencies:
```bash
pip install -r requirements.txt
```

2. Start Jupyter Notebook:
```bash
jupyter notebook
```

3. Run the notebooks in order:
   - First: `Bangladesh_Informal_Firms_Analysis.ipynb`
   - Second: `Bangladesh_Analysis_Part2.ipynb`

## Key Features Converted from R

### Geographic Analysis
- **R**: `rgdal`, `rgeos`, `maptools` → **Python**: `geopandas`, `shapely`
- District-level choropleth mapping with average revenue data
- Major cities overlay with population-scaled markers

### Statistical Visualizations  
- **R**: `ggplot2` → **Python**: `matplotlib`, `seaborn`, `plotly`
- Multiple histogram binwidths and log transformations
- Correlation analysis with scatter plots and jittering
- Box plots for categorical comparisons

### Data Manipulation
- **R**: `dplyr`, `plyr`, `reshape2` → **Python**: `pandas`
- ISIC industry classification merging
- Financial source data reshaping (melt operations)
- Aggregation and grouping operations

### Advanced Features
- Faceted visualizations by industry sectors
- Trend line analysis with regression statistics
- Complex financing source analysis across sectors
- Three comprehensive final plots matching R output

## Output

The notebooks generate visualizations and analysis very similar to the original R output, including:

1. **Geographic Analysis**: Bangladesh district map with average revenue
2. **Revenue Distributions**: Multiple histogram approaches with different binwidths
3. **Business Size Analysis**: Employee vs revenue relationships by sector
4. **Industry Classification**: ISIC section analysis with pie charts and box plots  
5. **Financing Analysis**: Sources of credit by sector and revenue levels
6. **Final Plots**: Three publication-ready visualizations with urban analysis

## Key Differences from R Version

- Uses `geopandas` instead of `rgdal` for shapefile handling
- `matplotlib`/`seaborn` instead of `ggplot2` for plotting
- `pandas` for all data manipulation instead of R's `dplyr`/`plyr`
- Some statistical functions use `scipy.stats` instead of R's built-in stats
- Interactive plots available via `plotly` (optional enhancement)

## Notes

- All analysis logic and statistical approaches remain identical to the original R version
- File paths are set for the current directory structure
- The Python version includes additional summary statistics and correlation details
- Visualizations maintain the same style and insights as the original analysis