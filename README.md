# AMR Governance in Bulgaria: Policy Feedback Analysis of the 2023 eRx Mandate
## Capstone Research Project

## Overview
This project investigates why antimicrobial resistance (AMR) remains persistently high in Bulgaria — one of the EU's highest-burden countries — and evaluates whether the 2023 mandatory electronic prescribing (eRx) reform is designed to address the governance failures driving resistance. Using Policy Feedback Theory (PFT) as an analytical framework, the study identifies three overlapping path-dependent feedback legacies (institutional capacity, socioeconomic barriers, and behavioral/governance norms) and tests their relative empirical importance through domain-specific regression models on EARS-Net surveillance data (2006–2023).

The central finding is that governance quality — specifically rule of law and corruption perceptions — explains substantially more variation in E. coli resistance rates than institutional capacity or socioeconomic factors alone (R² = 0.72), suggesting that the eRx mandate's effectiveness depends not on its formal design but on whether it strengthens enforcement credibility in practice.

## Research Questions 
- Which policy feedback domain — institutional capacity, socioeconomic barriers, or behavioral/governance norms — is most strongly associated with Bulgaria's sustained high AMR rates?
- Is the 2023 eRx mandate designed to disrupt the specific feedback mechanisms sustaining resistance, or does it risk producing symbolic compliance on an unchanged institutional substrate?

## Methods
This study combines **quantitative regression analysis** with **qualitative policy feedback 
analysis** — the empirical models are used to identify which governance domains, first explained qualitatively, are most 
strongly associated with resistance feedbacks. The core argument about *why* these 
associations exist and what they mean for the eRx mandate is developed through 
institutional and historical analysis grounded in Policy Feedback Theory.

Quantitative component:  
- Framework: Policy Feedback Theory (Pierson, 1993; Mettler & Soss, 2004)
- Outcome variable: Annual % of E. coli isolates resistant to third-generation cephalosporins (3GC), from EARS-Net surveillance data
- Analytical approach: Three domain-specific OLS regression models with standardized coefficients and variance decomposition; diagnostic testing for heteroskedasticity (Breusch-Pagan), multicollinearity (VIF), and autocorrelation (Durbin-Watson)
- Results are interpreted as robust associations, not causal claims; see the 
  full paper for a discussion of limitations and alternative explanations
- Time period: 2006–2023 (N = 18)
- Software: R (version 2024.12.0+467)
  
| Feedback Domain | Indicator | Variable Name | Units | Source |
|----------------|-----------|---------------|-------|--------|
| Institutional Capacity | Public health expenditure | `expenditure` | % GDP | World Bank Group |
| Institutional Capacity | Healthcare personnel density | `personnel` | physicians per 1,000 population | Eurostat |
| Institutional Capacity | Government effectiveness index | `goe` | scale from -2.5 (weak) to +2.5 (strong) | UNDP |
| Socioeconomic Barriers | Gini coefficient (income inequality) | `gini` | 0–1; 0 = perfect equality, 1 = perfect inequality | Eurostat |
| Socioeconomic Barriers | Out of pocket payments | `out_of_pocket` | % of all payments for medical services | World Bank Group |
| Behavioral Norms | Corruption perception index | `cpi` | 0–100; 0 = highly corrupt, 100 = very clean | Transparency International |
| Behavioral Norms | Rule of Law index | `rol` | 0–100 percentile rank; higher = better | UNDP (2005–2021), World Justice Project (2021–2023) |
| NA (outcome) | Antimicrobial resistance | `resistance` | proportion of *E. coli* isolates resistant to third-generation cephalosporins, measured at the regional level | EARS-Net |

## Key Findings
- Governance quality (Model 3) explains the most variation in resistance rates (R² = 0.72); both CPI and Rule of Law are statistically significant predictors
- Socioeconomic inequality (Gini coefficient) is a strong positive predictor of AMR (β = 2.41, p < 0.001), supporting the argument that structural stratification shapes antibiotic misuse patterns
- Institutional capacity alone (Model 1) does not predict resistance reductions, suggesting that spending and staffing without targeted stewardship are insufficient
- The eRx mandate's ambiguous penalty regime and fragmented enforcement authority risk generating symbolic compliance rather than behavioral change

| Model | Domain | R² |
|-------|--------|----|
| Model 1 | Institutional Capacity | 0.56 |
| Model 2 | Socioeconomic Barriers | 0.62 |
| Model 3 | Behavioral/Governance Norms | 0.72 |

## Links to Public Data Sets
- Health expenditure (2000-2022): https://data.worldbank.org/indicator/SH.XPD.CHEX.GD.ZS?locations=BG 
- Healthcare personnel density; practicing; per hundred thousand population (2000-2023): https://ec.europa.eu/eurostat/databrowser/view/hlth_rs_prs2__custom_20071945/default/table
- Gini coefficient (2006-2023): https://data.worldbank.org/indicator/SI.POV.GINI?end=2023&locations=BG&start=2005 
- Out-of-pocket expenditure (% of current health expenditure) (2005-2023) https://data.worldbank.org/indicator/SH.XPD.OOPC.CH.ZS 
- Government effectiveness index (2005-2021) https://data.undp.org/governance 
  Government effectiveness index (2017-2024) https://www.theglobaleconomy.com/Bulgaria/wb_government_effectiveness/ 
- Corruption perception index (2001-2025) https://statbase.org/data/bgr-corruption-perceptions-index/ 
- Rule of law (2015-2025) https://worldjusticeproject.org/rule-of-law-index/country/2025/Bulgaria 
	Rule of law (2002-2021) https://data.undp.org/governance 
- Resistance as % isolates of E. coli resistant to 3GC https://ncipd.org/index.php?option=com_content&view=featured&Itemid=730&lang=en 


### Author
Yana Rasheva
