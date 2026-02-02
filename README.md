# Economic Determinants and Structural Vulnerabilities of Crime in Europe (2010-2023)

## 📊 Overview

This project investigates the socio-economic determinants of homicide rates across 27 European Union countries from 2010 to 2023 using panel data econometrics. We employ various panel regression techniques to identify risk and protective factors influencing violent crime.

**Research Question:** What are the main economic and structural factors that explain variations in homicide rates across European countries?

## 👥 Authors

- **Mahamadou Issoufou Khadija**
- **Moudir Mohammed Anis**
- **Razanaboninahitra Miangaly**
- **Roland Jarlay**

*Academic Project - Panel Data Econometrics Course*  
*January 2026*

## 📁 Repository Structure

```
.
├── *.do                    # Stata analysis script
├── *.pdf                   # Project report
├── README.md               # This file
└── data/                   # Data files
    └── *.dta
```

## 🎯 Key Features

### 1. **Comprehensive Data Analysis**
- Panel data structure with 27 EU countries over 14 years
- Missing data diagnostics
- Variance decomposition (between vs. within)
- Temporal trend analysis

### 2. **Econometric Models**
The analysis implements five panel regression approaches:
- **POLS** (Pooled OLS)
- **FD** (First Differences)
- **BE** (Between Effects)
- **FE** (Fixed Effects)
- **RE** (Random Effects)

### 3. **Variables Analyzed**

**Dependent Variable:**
- `ln_homicides`: Log of homicide rate per 100,000 inhabitants

**Independent Variables:**
- **Economic factors:** Poverty rate, unemployment, GDP per capita
- **Social protection:** Social spending (% GDP)
- **Demographic factors:** Youth population (15-24), single-parent households
- **Structural factors:** Police density, urban overcrowding, inequality (Gini)
- **Interaction terms:** Unemployment × Youth population

### 4. **Visualizations**
- Geographic maps (spatial analysis)
- Time series plots
- Correlation matrices
- Box plots by country
- Between/Within variance decomposition charts

## 🔧 Requirements

### Software
- **Stata**
- Required Stata packages:
  - `estout` (for regression tables)
  - `spmap` (for spatial mapping)

### Data
The dataset is required but not included in this repository due to licensing constraints.

**Data Source:** Eurostat 

## 🚀 Usage

### Running the Analysis

1. **Set working directory** in the `.do` file (line 14):
```stata
cd "YOUR_PATH_HERE"
```

2. **Place data files** in the working directory or `/data` folder

3. **Run the analysis script:**
```stata
do your_script_name.do
```

### Script Sections

The `.do` file is organized in three main parts:

#### **I. Data Diagnostics** (Lines 21-42)
- Panel structure declaration
- Missing data assessment
- Data completeness verification

#### **II. Exploratory Data Analysis** (Lines 44-281)
- Descriptive statistics
- Variance decomposition
- Temporal evolution
- Correlation analysis
- Scatter plots (risk vs. protective factors)
- Spatial mapping

#### **III. Econometric Modeling** (Lines 283-350)
- Variable transformations (log)
- Model estimations (POLS, FD, BE, FE, RE)
- Hausman test
- Breusch-Pagan LM test
- Comparative regression table

## 📈 Key Findings

### Main Results

1. **Poverty as a Risk Factor** (r = +0.34)
   - Higher poverty rates correlate with increased homicide rates

2. **Social Protection as Protective Factor** (r = -0.31)
   - Greater social spending (% GDP) associated with lower crime

3. **Variance Structure**
   - Between-country variation dominates over temporal variation
   - Suggests structural factors matter more than short-term changes

4. **Temporal Trend**
   - Declining trend in homicides across EU (2010-2023)
   - Linear trend statistically significant

### Model Selection
- **Hausman test** used to choose between FE and RE models
- **Breusch-Pagan test** confirms presence of individual effects

## 📚 Methodology

### Econometric Approach

```stata
# Fixed Effects Model (preferred specification)
ln_homicides_it = β₀ + β₁·ln_poverty_it + β₂·ln_social_spending_it 
                  + β₃·ln_police_it + ... + αᵢ + γₜ + εᵢₜ
```

Where:
- `αᵢ` = Country fixed effects
- `γₜ` = Time fixed effects
- `εᵢₜ` = Error term

### Robustness
- Clustered standard errors at country level
- Log transformations to handle skewness
- Centered variables for interpretable interactions

## 📊 Visualizations Generated

The script produces several publication-ready graphs:

1. **Variance Decomposition Bar Chart** (Figure 1)
2. **Time Series Plot** - EU-wide homicide trend
3. **Scatter Plots** - Risk (poverty) vs. Protective (social spending) factors
4. **Box Plots** - Country-level distributions
5. **Choropleth Maps** - Spatial distribution of crime and social protection

## 🤝 Contributing

This is an academic project completed in January 2026. While the repository is primarily for archival and demonstration purposes, suggestions and discussions are welcome via Issues.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🔗 References

**Data Source:**
- Eurostat 
- Coverage: EU-27 countries, 2010-2023

**Course:**
Panel Data Econometrics  
Academic Year 2025-2026

## 📧 Contact

For questions or collaboration inquiries, please contact me.

