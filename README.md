# NBA Player Salary Analysis


## Research Title
**How do different factors of NBA player statistics affect their salaries?**

### Overview
This research analyzes how various factors in NBA player statistics impact their salaries, offering valuable insights into how skilled players are financially rewarded. It also provides an understanding of how NBA salaries are distributed among players based on their performance metrics.

### Variables
- **Dependent Variable (Y):**
  - **Salary:** The salary of NBA players (in dollars).
- **Independent Variables (X):**
  - **OFFRTG:** Offensive Rating
  - **DEFRTG:** Defensive Rating
  - **PGP:** Playoff Games Played
  - **Award:** Number of Awards

### Importance of the Dependent Variable
Examining the relationship between salary and performance metrics (such as offensive rating, defensive rating, playoff games played, and awards) helps identify the key factors affecting players' market value. This is critical for teams when making contract decisions and for players when negotiating their contracts.

### Hypotheses
- **Null Hypothesis (H0):** No statistically significant relationship exists between the independent variables (OFFRTG, DEFRTG, PGP, Award) and salary.
- **Alternative Hypothesis (H1):** There is a statistically significant relationship between the independent variables (OFFRTG, DEFRTG, PGP, Award) and salary.

### Literature Review
1. **Berri, D. J., Schmidt, M. B., & Brook, S. L. (2004):** Investigates how NBA players' star power influences team revenues (Journal of Sports Economics).
2. **Leeds, M. A., & von Allmen, P. (2002):** Examines salary determinants of NBA players (Journal of Sports Economics).
3. **Simmons, R., & Mills, J. D. (2005):** Discusses the effect of non-sporting performances on basketball attendance (Journal of Sports Economics).

### Research Gap
Existing studies focus too narrowly on player statistics like offensive and defensive ratings, neglecting other factors like marketability, off-court behavior, and advanced analytics. Our study aims to provide a more comprehensive analysis, using recent data and advanced methods like machine learning.

---

## Data Description

- **Data Sources:** ESPN, statistical reports on NBA performance and salaries.
- **Data Characteristics:** 188 observations, including variables such as offensive rating, defensive rating, playoff games played, number of awards, and player salaries.
- **Key Variables:**
  - **Salary:** Mean: $16,392,242, SD: $12,761,318
  - **OFFRTG:** Mean: 114.88, SD: 4.79
  - **DEFRTG:** Mean: 114.20, SD: 3.83
  - **PGP:** Mean: 32.03, SD: 40.82
  - **Award:** NA (Discrete variable)

### Data Distribution
- **Histogram:** The NBA player salary distribution is right-skewed, with a few players earning significantly higher salaries than most others. This skew may be influenced by star players like LeBron James, which raises questions regarding salary cap structures.
  
- **Boxplot Summary:**
  - Minimum: $1,119,563
  - First Quartile (Q1): $5,848,167
  - Median: $12,015,150
  - Third Quartile (Q3): $24,107,143
  - Maximum: $51,915,615

---

## Methodology

### Simple Linear Regression (SLR)
The simple linear regression model helps analyze how changes in the **OFFRTG** (Offensive Rating) affect **Salary**:
- Formula: `Salary = β0 + β1 * OFFRTG + ε`

### Multiple Linear Regression (MLR)
The MLR model includes multiple factors (OFFRTG, DEFRTG, PGP, Award) to examine their combined effect on salary:
- Formula: `Salary = β0 + β1 * OFFRTG + β2 * DEFRTG + β3 * PGP + β4 * Award + ε`

### Assumptions:
1. **Linearity:** The relationship between salary and explanatory variables should be linear.
2. **Independence:** Observations should be independent of each other.
3. **Normality:** Residuals should be normally distributed.
4. **Homoscedasticity:** The variance of residuals should remain constant across levels of the predictors.

### Heatmap & VIF Analysis
- **Heatmap:** Strong positive correlations were found between the variables, suggesting that players excelling in offensive rating also tend to perform better in other metrics.
- **VIF:** All variables showed low multicollinearity (VIF values near 1), indicating minimal issues with multicollinearity.

---

## Results

### Models:
1. **Model 1:** `lm(Salary ~ OFFRTG)`
2. **Model 2:** `lm(Salary ~ OFFRTG + DEFRTG)`
3. **Model 3:** `lm(Salary ~ OFFRTG + DEFRTG + PGP)`
4. **Model 4:** `lm(Salary ~ OFFRTG + DEFRTG + PGP + Award)`

---

## Conclusion
This analysis provides insights into how NBA player statistics, including offensive and defensive ratings, playoff performance, and awards, impact salaries. By understanding these relationships, NBA teams can make better-informed decisions, while players can use this knowledge to negotiate better contracts.

---

Feel free to contribute or suggest improvements to the analysis!

