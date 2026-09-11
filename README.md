# Cybersecurity Knowledge, Attitude & Practice (KAP): Digital Skills, Risk Exposure, and Cyber Victimization

*An Advanced Partial Least Squares Structural Equation Modeling (PLS-SEM) Empirical Investigation*

## Technical & Methodological Specification

- **Domain**: Behavioral Cybersecurity, Human Factors in Information Security, Youth Online Protection
- **Tech Tools & Software**: SmartPLS 4 (v4.1.0+), IBM SPSS Statistics (v28.0), Microsoft Excel (XML Engine), Python 3.14
- **Core Approaches**: Knowledge-Attitude-Practice (KAP) Behavioral Model, Routine Activity Theory (Cohen & Felson), Reflective Measurement Model Purification, Exploratory & Confirmatory Factor Analysis (EFA/CFA)
- **Algorithms Employed**: Wold's Iterative Partial Least Squares (PLS) Algorithm (Mode A Outer Estimation, Path Weighting Scheme Inner Estimation), Non-parametric Bootstrapping (5,000 Resamples, Two-Tailed Bias-Corrected Confidence Intervals), HTMT Discriminant Ratio Algorithm, Cohen's f² Effect Size Formulation
- **Sample & Dataset**: N = 139 Validated Adolescent/Young Adult Survey Respondents across 7 Latent Constructs
- **Deliverable Files**: cyber security final.xlsx (SmartPLS 4 full matrix), cyber OUTPUT.doc (Full SPSS report), cyber security.spv (SPSS Viewer output), KAP_CyberSecurity_FINAL new (2).sav

---

## 1. Executive Summary & Problem Scope

With the accelerating digitization of daily life, adolescents and young adults face escalating exposure to sophisticated online threats. While technical digital proficiency is often promoted as a protective shield, empirical behavioral research shows that advanced digital competence frequently fosters higher engagement in risk-prone online spaces.

This research project conducts an end-to-end structural equation modeling investigation into how technical competence (`DigSkills`) and institutional/parental supervision (`ParTeaSuper`) influence behavioral manifestations such as Information Sharing with Strangers (`InfoShare`), Online Gaming (`OnlineGaming`), and Content Creation (`ContentCreation`), and how these in turn mediate Exposure to Online Risks (`OnlineRisks`) and subsequent severe Cyber Victimization (`CyberVictim`).

The final models reveal that Information Sharing with Strangers is the paramount direct driver of online risk exposure, which subsequently translates directly into cyber victimization, whereas supervisory mediation acts primarily as a suppressor of online gaming rather than stranger disclosure.

## 2. Theoretical Framework & Methodological Approaches

**1. Routine Activity Theory (RAT)**: Originally formulated by Cohen and Felson (1979) for criminological analysis, RAT is adapted here to cyberspace. Online victimization requires the convergence in time and space of three elements: (1) A suitable target (adolescent sharing personal identifiers, photos, or passwords); (2) A motivated offender (cyber stalkers, scammers, data harvesters); and (3) The absence of capable guardians (lack of parental/teacher mediation or protective software).

**2. The Knowledge-Attitude-Practice (KAP) Paradigm**: Examines whether cognitive awareness (Digital Skills) translates effectively into protective attitudes and safe execution practices. The findings reveal a prominent 'KAP-Gap'—technical literacy alone does not curtail unsafe stranger disclosures.

**3. Reflective Measurement Model Architecture**: All 7 constructs were conceptualized as reflective latent variables. A psychometric retention floor of outer loading >= 0.50 was enforced to maintain measurement integrity without artificially discarding vital behavioral indicators.

## 3. Algorithms, Mathematical Formulations & Data Pipeline

**1. Wold-Lohmöller Iterative PLS Algorithm**: The model was computed using standard Mode A outer estimation where latent variable scores are estimated as linear combinations of their indicators: Y_j = sum(w_jk * x_jk). The inner structural relationships are estimated using the **Path Weighting Scheme**, which solves directional regressions between adjacent constructs based on their structural dependencies.

**2. Non-Parametric Bootstrapping Algorithm**: To test hypotheses without assuming multivariate normality, 5,000 bootstrap resamples were generated. For each path coefficient beta, standard errors SE(beta) and empirical t-statistics (t = beta / SE) were computed along with 95% bias-corrected percentile confidence intervals.

**3. Discriminant Validity Algorithms**:

• **Heterotrait-Monotrait Ratio (HTMT)**: HTMT_ij = (average heterotrait correlations) / sqrt((average monotrait correlations_i) * (average monotrait correlations_j)). All construct pairs remained strictly below the conservative 0.85 threshold (and liberal 0.90 threshold), confirming discriminant distinctiveness.

• **Fornell-Larcker Criterion**: Evaluated by checking that the square root of each construct's Average Variance Extracted (sqrt(AVE)) exceeds its highest correlation with any other latent variable.

**4. Collinearity & Effect Size Algorithms**: Multicollinearity was audited using Variance Inflation Factors (VIF = 1 / (1 - R_k^2)), confirming all structural inner VIF values were between 1.000 and 1.041 (far below the conservative 3.3 threshold). Cohen's effect size f^2 was computed as: f^2 = (R^2_incl - R^2_excl) / (1 - R^2_incl).

## 4. Empirical Results & Structural Hypotheses Testing

The PLS-SEM structural analysis evaluated 8 core hypothesized paths (tested at alpha = 0.05, two-tailed). Four hypotheses were firmly supported, revealing the exact transmission mechanism of digital victimization:

• **H5 (InfoShare -> OnlineRisks)**: Highly significant positive path (Beta = 0.415, SE = 0.088, t = 4.735, p < 0.001, medium effect f^2 = 0.214). Disclosing home addresses, phone numbers, and school names to strangers represents the primary vulnerability catalyst.

• **H8 (OnlineRisks -> CyberVictim)**: Highly significant direct path (Beta = 0.309, SE = 0.124, t = 2.493, p = 0.0127, f^2 = 0.105). Direct exposure to online risks significantly increases the likelihood of suffering financial extortion, account hijacking, and harassment.

• **H2 (DigSkills -> ContentCreation)**: Robust positive path (Beta = 0.385, SE = 0.085, t = 4.537, p < 0.001, f^2 = 0.174). Advanced technical competencies actively empower blogging, civic participation, and portfolio building.

• **H7 (ContentCreation -> OnlineRisks)**: Significant positive path (Beta = 0.166, SE = 0.072, t = 2.312, p = 0.0208). Public content generation inadvertently creates digital footprints accessible to malicious actors.

• **H4 (ParTeaSuper -> OnlineGaming)**: Strong negative path (Beta = -0.366, SE = 0.079, t = -4.600, p < 0.001, f^2 = 0.154). Proactive discussion and monitoring by parents and teachers successfully reduce excessive gaming participation.

• **H1 (DigSkills -> InfoShare, p = 0.4595) & H3 (ParTeaSuper -> InfoShare, p = 0.6375)**: Not statistically supported, demonstrating that neither general digital proficiency nor generic adult lectures deter online oversharing.

| Hypothesis | Path Relationship | Beta (Std. Coef.) | Std. Error | t-statistic | p-value | Decision (alpha = 0.05) | f² Effect Size |
| --- | --- | --- | --- | --- | --- | --- | --- |
| H1 | Digital Skills -> Information Sharing | 0.066 | 0.089 | 0.740 | 0.4595 | Not Supported | 0.004 (Negligible) |
| H2 | Digital Skills -> Content Creation | 0.385 | 0.085 | 4.537 | < 0.001 | Supported | 0.174 (Medium) |
| H3 | Parent/Teacher Supervision -> Info Sharing | 0.041 | 0.087 | 0.471 | 0.6375 | Not Supported | 0.002 (Negligible) |
| H4 | Parent/Teacher Supervision -> Online Gaming | -0.366 | 0.079 | -4.600 | < 0.001 | Supported | 0.154 (Medium) |
| H5 | Information Sharing -> Online Risks | 0.415 | 0.088 | 4.735 | < 0.001 | Supported | 0.214 (Medium) |
| H6 | Online Gaming -> Online Risks | -0.104 | 0.074 | -1.415 | 0.1569 | Not Supported | 0.013 (Negligible) |
| H7 | Content Creation -> Online Risks | 0.166 | 0.072 | 2.312 | 0.0208 | Supported | 0.033 (Small) |
| H8 | Online Risks -> Cyber Victimization | 0.309 | 0.124 | 2.493 | 0.0127 | Supported | 0.105 (Small) |


## 5. Variance Explained (R²) & Measurement Model Diagnostics

• **Exposure to Online Risks**: R² = 0.218 (Adjusted R² = 0.200) — 21.8% of variance explained by Information Sharing, Content Creation, and Gaming.

• **Content Creation & Participation**: R² = 0.148 (Adjusted R² = 0.142) — 14.8% explained by Digital Skills.

• **Online Gaming**: R² = 0.134 (Adjusted R² = 0.127) — 13.4% explained by Supervisory Mediation.

• **Cyber Victimization**: R² = 0.095 (Adjusted R² = 0.089) — Direct exposure accounts for 9.5% of overall victim incidence.

• **Indicator Trimming Log**: 8 problematic items with outer loadings < 0.50 were systematically removed (neg_tricked [0.406], neg_identitytheft [0.433], pw_buyonline [0.440], skill_video [0.455], neg_cyberbully [0.490], skill_payments [0.497], neg_stalked [0.499], and pw_postmsg [0.339]), guaranteeing structural stability.

## 6. Strategic Implications for Educators, Parents & Cybersecurity Policy

1. **Rethinking Cyber Literacy Curricula**: Schools must shift from teaching procedural computing (how to use tools) to risk-calibrated behavioral governance (evaluating the consequences of personal metadata exposure).

2. **Guardian Capability Engineering**: Rather than imposing device confiscations or blanket gaming bans, parents and educators must deploy communication-based mediation focused on social-engineering red flags and stranger interactions.
