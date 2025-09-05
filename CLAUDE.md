# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This project examines informal firm characteristics in Bangladesh using World Bank survey data from 2010. The analysis explores how annual revenue relates to variables like number of employees, industry sector, financing sources, and geography. This is the Python implementation converted from the original R analysis.

## Key Files and Data Structure

### Python Implementation
- **`Bangladesh_Informal_Firms_Analysis.ipynb`**: Part 1 - Geographic analysis, revenue distributions, ISIC classifications
- **`Bangladesh_Analysis_Part2.ipynb`**: Part 2 - Business size analysis, financing sources, final plots
- **`requirements.txt`**: Python dependencies

### Data Files
- **`informality_data_NEW.csv`**: Primary survey dataset from World Bank
- **`surveydata_with_ISIC.csv`**: Augmented survey data with ISIC industry classifications
- **`ISIC_Rev_3_english_structure.csv`**: Industry classification reference data
- **`shp/`**: Directory containing Bangladesh district boundary shapefiles for geographic visualization
- **`Sources of Information.txt`**: Data source documentation

## Python Environment and Dependencies

The project uses:
- `pandas`, `numpy` - Data manipulation and numerical operations
- `matplotlib`, `seaborn` - Visualization libraries
- `geopandas`, `shapely` - Geographic data handling
- `scipy` - Statistical analysis
- `plotly` - Interactive visualizations (optional)
- `jupyter` - Notebook environment

## Data Sources and Structure

The analysis combines multiple data sources:
1. **World Bank Bangladesh Informal Firms Survey 2010** - Main microdata
2. **UN ISIC Rev 3 Classification** - Industry sector categorization  
3. **WFP Bangladesh Administrative Boundaries** - Geographic shapefiles for district-level mapping

Key variables:
- `q4_7`: Annual revenue for 2009 (in Bangladesh Takas)
- `q1_12a5a`: Number of employees
- ISIC codes linked to industry sector descriptions

## Running the Analysis

### Setup
1. **Install dependencies**: `pip install -r requirements.txt`
2. **Start Jupyter**: `jupyter notebook`
3. **Run notebooks in order**: 
   - `Bangladesh_Informal_Firms_Analysis.ipynb` (Part 1)
   - `Bangladesh_Analysis_Part2.ipynb` (Part 2)
4. **Output**: Interactive notebook cells with analysis and visualizations

## Analysis Architecture

The analysis follows a structured exploratory approach:
1. **Geographic Analysis**: District-level revenue mapping using shapefiles
2. **Revenue Distribution**: Histogram analysis with different binwidths and log transformations
3. **Employee-Revenue Relationship**: Scatter plots with jittering and correlation analysis  
4. **Industry Sector Analysis**: Revenue patterns across ISIC industry classifications
5. **Statistical Testing**: Correlation tests and comparative analysis

The project demonstrates Python best practices for combining survey microdata with geographic boundaries and external classification systems for comprehensive analysis.

## Important Instructions

Do what has been asked; nothing more, nothing less.
NEVER create files unless they're absolutely necessary for achieving your goal.
ALWAYS prefer editing an existing file to creating a new one.
NEVER proactively create documentation files (*.md) or README files. Only create documentation files if explicitly requested by the User.