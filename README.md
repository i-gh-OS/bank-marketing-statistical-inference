# Statistical Inference on Bank Marketing Campaigns

Statistical analysis of a Portuguese bank marketing dataset using R,
focused on hypothesis testing, distributional assumptions, and customer
campaign outcomes.

## Overview

This project applies statistical inference techniques to evaluate customer
behavior and marketing campaign performance.

The analysis includes:

- Normality testing using Shapiro-Wilk tests and graphical diagnostics
- One-sided and two-sided hypothesis tests for differences in means
- Two-sample proportion tests
- Type I and Type II error analysis
- Statistical power analysis
- Wilcoxon non-parametric tests
- Spearman rank correlation

## Business Problem

The bank historically achieved approximately a 12% conversion rate for
term-deposit marketing campaigns. A more expensive marketing strategy is
being considered, raising the question of whether the new campaign produces
a statistically significant improvement in conversion.

Using a random sample of 25 customers, the project defines a decision rule,
quantifies Type I and Type II errors, evaluates statistical power, and
explores how the test design could be improved.

## Methods

### Distribution Analysis
Shapiro-Wilk tests and graphical diagnostics are used to assess normality
assumptions for quantitative variables.

### Hypothesis Testing
Both one-sided and two-sided tests are used to investigate differences
between customer groups.

### Proportion Testing
A hypothesis test evaluates differences in conversion rates.

### Statistical Power
The relationship between sample size, significance level, Type II error,
and statistical power is analyzed in the context of the marketing decision.

### Non-Parametric Analysis
- Wilcoxon test: comparison of call duration between customers who subscribed
  and those who did not.
- Spearman correlation: association between campaign contact frequency and
  call duration.

## Technologies

- R
- Statistical hypothesis testing
- Statistical power analysis
- Non-parametric statistics
- Data visualization
