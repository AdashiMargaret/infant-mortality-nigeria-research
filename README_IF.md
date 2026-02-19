# Infant Mortality Risk Factors in Northern Nigeria: A Demographic Health Survey Analysis

## 🔬 Project Overview

This epidemiological study investigates the sociodemographic determinants of infant mortality in Northern Nigeria using data from the 2018 Nigerian Demographic Health Survey (NDHS). The research employs advanced statistical modeling to identify key risk factors that contribute to infant deaths before the first birthday, providing critical insights for public health interventions and policy development.

## 📊 Research Impact & Significance

### Public Health Value
- **Population Health Assessment**: Analyzed 80,110 women to identify preventable infant mortality risk factors
- **Healthcare Policy Support**: Generated evidence-based recommendations for maternal and child health interventions
- **Health Disparities Research**: Quantified the impact of socioeconomic inequalities on infant survival outcomes
- **Global Health Contribution**: Addressed critical knowledge gaps in Sub-Saharan African infant mortality patterns

### Statistical & Methodological Rigor
- **Large-Scale Analysis**: Processed nationally representative survey data with 99% response rate
- **Multivariable Modeling**: Applied advanced logistic regression with proper confounding control
- **Model Validation**: Comprehensive diagnostic testing including multicollinearity and influence analysis
- **Regulatory Standards**: Followed epidemiological best practices for observational research

## 🎯 Key Research Findings

### Primary Risk Factors Identified (Adjusted Odds Ratios):

**Socioeconomic Determinants:**
- **Wealth Index**: Richest families had 67% lower infant mortality risk (OR=0.33, 95%CI: 0.28-0.37)
- **Maternal Education**: Higher education reduced risk by 18% (OR=0.82, 95%CI: 0.69-0.96)
- **Birth Spacing**: >2 year intervals reduced risk by 73% (OR=0.27, 95%CI: 0.24-0.31)

**Demographic Patterns:**
- **Child Sex**: Female infants had 14% lower mortality risk (OR=0.86, 95%CI: 0.82-0.90)
- **Maternal Age**: Optimal outcomes for mothers aged 25-39 years
- **Maternal BMI**: Overweight mothers showed 25% lower risk vs. underweight (OR=0.75, 95%CI: 0.64-0.88)

### Clinical Significance
- **9% infant mortality rate** in the study population (7,270 out of 80,110 cases)
- Strong dose-response relationships across wealth and education gradients
- Clear evidence of modifiable risk factors for targeted interventions

## 🛠 Technical Skills Demonstrated

### Advanced Statistical Analysis
- **Multivariable Logistic Regression** - Complex outcome prediction modeling
- **Confounding Control** - Systematic evaluation and adjustment for covariates
- **Model Diagnostics** - Variance inflation factors, Cook's distance analysis
- **Effect Size Interpretation** - Odds ratios and confidence interval analysis

### Large-Scale Data Management
- **Survey Data Analysis** - Complex sampling design handling
- **Missing Data Management** - Strategic inclusion/exclusion criteria application
- **Variable Engineering** - Categorical recoding and reference group optimization
- **Quality Assurance** - Multi-level data validation and integrity checks

### Research & Programming Excellence
- **R Programming** - Advanced statistical computing and modeling
- **Epidemiological Methods** - Cross-sectional study design and analysis
- **Scientific Writing** - Peer-review quality methodology and reporting
- **Reproducible Research** - Documented analysis pipeline and version control

### Public Health Applications
- **Population Health Analytics** - Large-scale health outcome prediction
- **Health Equity Analysis** - Socioeconomic disparity quantification
- **Evidence-Based Policy** - Research translation for intervention development
- **Global Health Research** - International development and humanitarian applications

## 📁 Repository Structure

```
infant-mortality-nigeria-analysis/
├── README.md                           # Project overview and findings
├── analysis/
│   ├── infant_mortality_analysis.Rmd   # Complete R Markdown analysis
│   └── infant_mortality_report.html    # Knitted research report
├── data/
│   └── data_documentation.md           # NDHS dataset information and variables
├── methodology/
│   ├── statistical_analysis_plan.md    # Pre-specified analysis approach
│   └── model_diagnostics.md           # Validation and assumption testing
└── results/
    ├── summary_tables.csv              # Key findings and effect estimates
    └── risk_factor_plots.png           # Data visualizations
```

## 🚀 Getting Started

### Prerequisites
```r
# Required R packages for replication
install.packages(c("tidyverse", "haven", "blorr", "car", "lmtest", 
                   "odds.n.ends", "table1", "knitr", "foreign"))
```

### Running the Analysis
1. Clone this repository
2. Download NDHS 2018 dataset (registration required)
3. Update file paths in `infant_mortality_analysis.Rmd`
4. Execute analysis chunks sequentially

## 📈 Methodology Summary

### Study Design & Population
- **Design**: Cross-sectional analysis of nationally representative survey data
- **Population**: Women aged 15-49 from Northern Nigeria (n=80,110)
- **Outcome**: Infant mortality (death before 12 months of age)
- **Exposures**: Maternal age, education, wealth, BMI, birth interval, child sex

### Statistical Approach
1. **Descriptive Analysis** - Population characteristics and outcome prevalence
2. **Univariate Screening** - Individual predictor-outcome associations
3. **Multivariable Modeling** - Adjusted analysis with confounder control
4. **Model Validation** - Diagnostic testing and sensitivity analysis
5. **Effect Interpretation** - Clinical and public health significance assessment

### Quality Assurance Framework
- ✅ **Multicollinearity Testing**: All VIF values < 3
- ✅ **Goodness of Fit**: Hosmer-Lemeshow test validation
- ✅ **Influential Observations**: Cook's distance outlier analysis
- ✅ **Model Comparison**: Likelihood ratio testing for nested models
- ✅ **Effect Size Validation**: Clinically meaningful odds ratio interpretation

## 🌍 Applications & Industry Relevance

### Healthcare & Public Health
- **Clinical Research**: Risk stratification and outcome prediction methodologies
- **Health Services Research**: Population health analytics and intervention targeting
- **Epidemiological Surveillance**: Disease pattern recognition and trend analysis
- **Global Health**: International development and humanitarian health programs

### Data Science & Analytics
- **Predictive Modeling**: Binary outcome classification with complex survey data
- **Feature Engineering**: Categorical variable optimization and reference selection
- **Model Validation**: Comprehensive diagnostic testing and assumption verification
- **Statistical Consulting**: Evidence-based analysis for policy and program evaluation

### Regulatory & Compliance
- **FDA/WHO Standards**: International guidelines for observational research
- **GCP Compliance**: Good Clinical Practice for epidemiological studies
- **Publication Standards**: STROBE guidelines for cross-sectional studies
- **Ethical Research**: IRB-approved secondary data analysis protocols

## 📊 Key Research Findings

### 🎯 Strongest Protective Factors (Adjusted Odds Ratios)

| **Risk Factor** | **Comparison** | **Adjusted OR** | **95% CI** | **Risk Reduction** | **Significance** |
|----------------|----------------|-----------------|------------|-------------------|------------------|
| **🌟 Birth Spacing** | **>2 years vs ≤11 months** | **0.27** | 0.24 - 0.31 | **73% ⬇️** | *** |
| **💰 Wealth Index** | **Richest vs Poorest** | **0.33** | 0.28 - 0.37 | **67% ⬇️** | *** |
| **💰 Wealth Index** | **Richer vs Poorest** | **0.52** | 0.47 - 0.56 | **48% ⬇️** | *** |
| **⏰ Birth Spacing** | **1-2 years vs ≤11 months** | **0.54** | 0.47 - 0.61 | **46% ⬇️** | *** |
| **🎓 Education** | **Higher vs None** | **0.82** | 0.69 - 0.96 | **18% ⬇️** | ** |
| **👶 Child Sex** | **Female vs Male** | **0.86** | 0.82 - 0.90 | **14% ⬇️** | *** |

**Legend:** `***` p<0.001, `**` p<0.01 | `⬇️` = Risk Reduction

### 💡 Wealth Gradient Analysis

| **Wealth Quintile** | **Sample Size** | **Mortality Rate** | **Adjusted OR** | **vs Poorest** |
|--------------------|-----------------|-------------------|----------------|----------------|
| **Poorest* | 25,849 | **10.3%** | **1.00** | — |
| **Poorer** | 21,885 | **10.1%** | **0.95** | 5% ⬇️ |
| **Middle** | 15,745 | **8.7%** | **0.72** | 28% ⬇️ |
| **Richer** | 10,652 | **6.9%** | **0.52** | 48% ⬇️ |
| **Richest**  | 5,979 | **4.9%** | **0.33** | **67% ⬇️** |

### ⏰ Birth Spacing Impact

| **Birth Interval** | **Sample Size** | **Mortality Rate** | **Adjusted OR** | **Interpretation** |
|-------------------|-----------------|-------------------|----------------|-------------------|
| **≤ 11 months**  | 1,406 | **20.4%** | **1.00** | **Highest Risk** |
| **1-2 years**  | 20,435 | **12.1%** | **0.54** | **46% Lower Risk** |
| **> 2 years** | 40,900 | **6.5%** | **0.27** | **73% Lower Risk** |

**📋 [View Complete Results Tables →](visual_results_tables.md)**

##  Career Applications

This research demonstrates expertise valuable for:

**Healthcare Analytics Roles:**
- Population health data scientist
- Clinical research analyst  
- Epidemiological researcher
- Public health data specialist

**Pharmaceutical & Biotech:**
- Real-world evidence analyst
- Regulatory affairs specialist
- Clinical development researcher
- Health economics analyst

**Global Health & Policy:**
- International development researcher
- Health policy analyst
- Humanitarian data scientist
- NGO research coordinator

**Consulting & Academia:**
- Healthcare consulting analyst
- Academic research scientist
- Statistical consulting specialist
- Grant writing and research development

## 📚 Research Impact

### Strengths
- **Large Sample Size**: Nationally representative with high response rates
- **Robust Methodology**: Advanced statistical techniques with proper validation
- **Clinical Relevance**: Actionable findings for intervention development
- **Reproducible Research**: Comprehensive documentation and code availability

### Public Health Implications
- Evidence supports targeted interventions for high-risk populations
- Economic case for education and poverty reduction programs
- Clinical guidance for optimal birth spacing recommendations
- Policy framework for maternal and child health program development

---

**Author**: Adashi Odama  
**Institution**: Washington University  
**Contact**: odamaadashi@gmail.com
**Date**: April 2022

*This analysis contributes to the global effort to reduce preventable infant deaths through evidence-based public health interventions and health equity promotion.*
