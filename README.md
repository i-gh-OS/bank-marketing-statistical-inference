# Statistical Inference on Bank Marketing Campaigns

Statistical inference project in **R** analyzing customer behavior and the effectiveness of a Portuguese bank's term-deposit marketing campaigns.

The project applies parametric and non-parametric hypothesis tests, statistical power analysis, and Type I/II error analysis to evaluate customer conversion and campaign performance.

## Project Overview

Each observation represents a customer contacted by telephone as part of a marketing campaign offering a term deposit.

The dataset includes both numerical and categorical variables describing customer characteristics and campaign interactions, including:

- `age` — customer age
- `balance` — average account balance
- `duration` — duration of the last call
- `campaign` — number of contacts during the current campaign
- `previous` — number of previous contacts
- `pdays` — days since the previous contact
- `y` — whether the customer subscribed to the term deposit

Additional categorical variables include employment, marital status, education, housing loans, personal loans, contact type, month, and previous campaign outcome.

## Objectives

The analysis addresses several statistical questions:

- Do the main quantitative variables follow a normal distribution?
- Does call duration differ between customers who subscribe and those who do not?
- Has average call duration increased relative to a historical benchmark?
- Is mortgage status associated with customer default?
- How should a decision rule for a new marketing campaign balance Type I and Type II errors?
- Are call duration and subscription related without assuming normality?
- Is there a monotonic association between the number of campaign contacts and call duration?

## Statistical Methods

### Normality Analysis

The distributions of `age`, `balance`, `duration`, and `campaign` were evaluated using:

- Shapiro-Wilk tests
- Histograms
- Q-Q plots

The Shapiro-Wilk tests rejected normality for all four variables.

An interesting case was `age`: its histogram and Q-Q plot appeared relatively close to normal, while the formal test still rejected normality. This illustrates how large samples can make hypothesis tests sensitive to relatively small deviations from the theoretical distribution.

### Difference in Call Duration

A two-sample **Welch t-test** was used to compare average call duration between customers who subscribed to the deposit and those who did not.

The null hypothesis of equal means was rejected at the 5% significance level.

Customers who subscribed tended to have substantially longer calls, suggesting a strong relationship between customer engagement during the call and eventual conversion.

### Comparison with a Historical Benchmark

A one-sample t-test evaluated whether mean call duration in the current campaign exceeded a historical benchmark of **250 seconds**.

The test rejected the null hypothesis, providing evidence that average call duration was greater than the historical reference value.

### Proportion Test

A two-sample proportion test investigated whether default rates differed between customers with and without a mortgage.

The resulting p-value was approximately **0.73**, so the null hypothesis could not be rejected.

The data therefore provided no evidence of a meaningful difference in default rates between the two groups.

## Type I / Type II Error and Statistical Power

A separate experiment studied the decision rule for adopting a more expensive marketing strategy.

The historical campaign conversion rate was assumed to be approximately **12%**, and the analysis considered a random sample of **25 customers**.

Two possible critical thresholds were compared for deciding whether the new strategy represented an improvement.

Lowering the decision threshold increased the probability of a Type I error, but simultaneously:

- reduced the Type II error probability
- increased statistical power
- improved the ability of the test to detect a real improvement

This illustrates the fundamental trade-off between false positives and false negatives when designing a statistical test.

## Non-Parametric Analysis

Because several variables showed substantial deviations from normality, non-parametric methods were also applied.

### Wilcoxon Rank-Sum Test

A Wilcoxon test compared the distribution of `duration` between customers who subscribed and those who did not.

The null hypothesis was rejected, confirming that call duration differs significantly between the two groups.

This result is consistent with the earlier Welch t-test.

### Spearman Correlation

Spearman's rank correlation was used to investigate the association between:

- `campaign` — number of contacts during the current campaign
- `duration` — duration of the latest call

The relationship was statistically significant but very weak:

**Spearman ρ ≈ -0.09**

This suggests that customers contacted more frequently tended to have slightly shorter calls, although the effect size is too small to indicate a strong practical relationship.

## Key Findings

- The main numerical variables show significant departures from normality.
- Customers who subscribe to the term deposit tend to have substantially longer calls.
- Average campaign call duration exceeds the historical 250-second benchmark.
- No statistically significant relationship was found between mortgage status and default rates.
- Decision thresholds create a clear trade-off between Type I error and statistical power.
- The Wilcoxon test independently confirms the relationship between call duration and subscription.
- Campaign contact frequency and call duration have a statistically significant but very weak negative association.

## Tools and Techniques

- **R**
- Statistical inference
- Hypothesis testing
- Welch t-test
- One-sample t-test
- Two-sample proportion tests
- Shapiro-Wilk test
- Wilcoxon rank-sum test
- Spearman rank correlation
- Type I and Type II error analysis
- Statistical power analysis
- Data visualization

## Project Context

Academic statistical inference project developed as part of the **Telecommunications Engineering & Business Analytics** program at ICAI – Universidad Pontificia Comillas.
