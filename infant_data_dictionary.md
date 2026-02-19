# Data Dictionary: Nigerian Demographic Health Survey 2018

## Dataset Overview

**Source**: 2018 Nigerian Demographic Health Survey (NDHS)  
**Study Design**: Nationally representative cross-sectional survey  
**Geographic Focus**: Northern Nigeria regions  
**Original Sample**: 127,545 women aged 15-49  
**Analysis Sample**: 80,110 women (after exclusions)  
**Response Rate**: 99%

## Study Population Selection

### Inclusion Criteria
- Women aged 15-49 years residing in Northern Nigeria
- Children who died before 12 months of age (infant mortality cases)
- Complete responses for all variables of interest
- Singleton births (twins/multiples excluded for independence)

### Exclusion Criteria
- Women from Central, Eastern, or Southern Nigerian regions
- Children with age at death >12 months
- Missing data on key predictor or outcome variables
- Non-resident/visitor status

## Variable Definitions

### Primary Outcome Variable

| Variable | Original Code | Type | Coding | Description |
|----------|---------------|------|--------|-------------|
| **Infant Mortality** | B5 | Binary | 0 = No, 1 = Yes | Death of child before first birthday |

### Primary Predictor Variables

#### Demographic Characteristics

| Variable | Original Code | Type | Categories | Description |
|----------|---------------|------|------------|-------------|
| **Child Sex** | B4 | Categorical | Male, Female | Biological sex of child |
| **Maternal Age** | V013 | Categorical | 15-19, 20-24, 25-29, 30-34, 35-39, 40-44, 45-49 | Mother's age at time of birth (years) |

#### Socioeconomic Factors

| Variable | Original Code | Type | Categories | Description |
|----------|---------------|------|------------|-------------|
| **Maternal Education** | V106 | Ordinal | No education, Primary, Secondary, Higher | Highest level of education completed |
| **Wealth Index** | V190 | Ordinal | Poorest, Poorer, Middle, Richer, Richest | Household wealth quintiles based on asset ownership |

#### Health and Reproductive Factors

| Variable | Original Code | Type | Categories | Description |
|----------|---------------|------|------------|-------------|
| **Maternal BMI** | BMI | Categorical | Underweight (<18.5), Normal (18.5-24.9), Overweight (25-29.9), Obese (≥30) | Body Mass Index calculated from height/weight |
| **Preceding Birth Interval** | Birth_interval | Ordinal | ≤11 months, 1-2 years, >2 years | Time between previous birth and index birth |

## Variable Construction Details

### Wealth Index Construction
The NDHS wealth index is constructed using Principal Components Analysis (PCA) from household assets:
- **Consumer goods**: Television, radio, bicycle, motorcycle, car
- **Dwelling characteristics**: Flooring material, wall material, roof material
- **Utilities**: Water source, sanitation facilities, cooking fuel, electricity
- **Assets**: Land ownership, livestock ownership, bank account

**Scoring**: Standardized factor scores (mean=0, SD=1) divided into population quintiles

### BMI Calculation
- **Formula**: Weight (kg) / Height (m)²
- **Data source**: Anthropometric measurements taken during survey
- **Missing values**: Cases with implausible values excluded (BMI <10 or >60)

### Birth Interval Calculation
- **Method**: Calculated as months between consecutive births
- **Reference**: Time from previous birth to index birth
- **Missing values**: First births excluded (no previous interval)

## Data Quality and Validation

### Missing Data Patterns
| Variable | Missing Rate | Handling Strategy |
|----------|--------------|-------------------|
| Child Sex | <0.1% | Complete case analysis |
| Maternal Age | <0.1% | Complete case analysis |
| Education | <1% | Complete case analysis |
| Wealth Index | <0.5% | Complete case analysis |
| BMI | 65.1% | Separate analysis subset |
| Birth Interval | 22.3% | Excludes first births |

### Data Cleaning Procedures

1. **Range Validation**
   - Age: 15-49 years (survey eligibility)
   - BMI: 10-60 kg/m² (physiologically plausible)
   - Birth interval: 6-300 months (reasonable reproductive span)

2. **Consistency Checks**
   - Education level vs. age consistency
   - Birth interval vs. maternal age alignment
   - Wealth index vs. geographic region patterns

3. **Outlier Detection**
   - BMI values >3 standard deviations from mean investigated
   - Birth intervals >5 years flagged for review
   - Maternal age-parity combinations assessed for plausibility

## Sampling Design and Weighting

### Sampling Framework
- **Design**: Two-stage cluster sampling
- **Primary Sampling Units**: Enumeration areas from 2006 census
- **Secondary Units**: Households within enumeration areas
- **Stratification**: Urban/rural and geographic regions

### Geographic Coverage (Northern Nigeria)
- **North Central**: Benue, Kogi, Kwara, Nasarawa, Niger, Plateau, FCT
- **North East**: Adamawa, Bauchi, Borno, Gombe, Taraba, Yobe
- **North West**: Jigawa, Kaduna, Kano, Katsina, Kebbi, Sokoto, Zamfara

### Sample Weights
- **Household weights**: Adjust for sampling probability and non-response
- **Individual weights**: Account for within-household selection
- **Analysis approach**: Unweighted analysis (descriptive focus on associations)

## Statistical Considerations

### Reference Categories
- **Maternal Age**: 15-19 years (youngest, highest risk group)
- **Education**: No education (most common, highest risk)
- **Wealth**: Poorest quintile (highest risk)
- **BMI**: Underweight (highest risk category)
- **Birth Interval**: ≤11 months (highest risk)
- **Child Sex**: Male (higher baseline mortality)

### Model Development Strategy
1. **Univariate screening**: Individual predictor-outcome associations
2. **Confounding assessment**: Systematic evaluation of potential confounders
3. **Model building**: Forward selection based on likelihood ratio tests
4. **Interaction testing**: Effect modification by key demographics
5. **Diagnostics**: Multicollinearity, goodness of fit, influence analysis

## Ethical Considerations

### Original Data Collection
- **IRB Approval**: National Health Research Ethics Committee of Nigeria
- **Informed Consent**: Verbal consent obtained from all participants
- **Confidentiality**: No personal identifiers in public dataset
- **Voluntary Participation**: Right to refuse or withdraw maintained

### Secondary Analysis Ethics
- **Data Access**: Publicly available through DHS Program registration
- **Privacy Protection**: All analyses conducted on de-identified data
- **Results Reporting**: Aggregate results only, no individual-level reporting
- **Beneficence**: Research aims to improve maternal-child health outcomes

## Data Limitations

### Measurement Limitations
- **Self-reported data**: Education, birth history subject to recall bias
- **Survival bias**: Only surviving mothers interviewed
- **Cross-sectional design**: Cannot establish temporal sequence/causality
- **Missing cause of death**: Cannot analyze specific mortality causes

### Generalizability Constraints
- **Geographic**: Results specific to Northern Nigeria context
- **Temporal**: 2018 data may not reflect current conditions
- **Population**: Women aged 15-49 with birth experience only
- **Selection**: Household-based sampling may miss marginalized populations

### Analytical Limitations
- **Clustering**: Complex sampling design not fully accounted for in standard errors
- **Multiple testing**: No formal adjustment for multiple comparisons
- **Residual confounding**: Unmeasured variables may influence associations
- **Effect modification**: Limited power for subgroup analyses

## Quality Assurance Procedures

### Data Validation Steps
1. **Range checks**: All variables within expected bounds
2. **Logic checks**: Consistent relationships between variables
3. **Duplicate detection**: No duplicate records in analysis dataset
4. **Missing pattern analysis**: Systematic assessment of non-response

### Statistical Validation
1. **Model diagnostics**: VIF, Cook's distance, Hosmer-Lemeshow tests
2. **Sensitivity analyses**: Alternative model specifications tested
3. **External validation**: Results compared to published literature
4. **Reproducibility**: Analysis code documented and version controlled

## File Structure and Naming Conventions

```
project/
├── data/
│   ├── raw/                     # Original SPSS files (NDHS 2018)
│   ├── processed/               # Cleaned analysis datasets
│   └── codebooks/               # Variable documentation
├── analysis/
│   ├── infant_mortality_analysis.Rmd  # Main analysis file
│   ├── model_diagnostics.R             # Validation procedures
│   └── sensitivity_analyses.R          # Alternative specifications
├── results/
│   ├── tables/                  # Summary statistics and model results
│   ├── figures/                 # Data visualizations
│   └── appendices/              # Supplementary materials
└── documentation/
    ├── data_dictionary.md       # This file
    ├── analysis_plan.md         # Statistical analysis plan
    └── ethics_documentation/    # IRB and ethical approvals
```

## Contact Information and Metadata

**Author**: Adashi Odama  
**Institution**: Washington University  
**Contact**: odamaadashi@gmail.com
**Date**: April 2022  
**Last Updated**: `r Sys.Date()`  
**Version**: 1.0  

**Data Citation**: 
National Population Commission (NPC) [Nigeria] and ICF. 2019. Nigeria Demographic and Health Survey 2018. Abuja, Nigeria, and Rockville, Maryland, USA: NPC and ICF.

**Software**: R version 4.0.5 with tidyverse, haven, blorr, car, lmtest packages

---

*This data dictionary provides comprehensive documentation for reproducible epidemiological research on infant mortality determinants in Northern Nigeria, following international standards for public health data analysis and reporting.*
