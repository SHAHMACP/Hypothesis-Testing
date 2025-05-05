

# Hypothesis Testing in Statistics

This repository provides a comprehensive overview of **Hypothesis Testing** in statistics, designed to support learners, educators, and data science practitioners. The content is based on foundational statistical principles and includes clearly explained concepts, definitions, and examples.

---

## Table of Contents

* [Introduction](#introduction)
* [Basic Terminology](#basic-terminology)
* [Types of Hypotheses](#types-of-hypotheses)
* [Errors in Hypothesis Testing](#errors-in-hypothesis-testing)
* [Test Statistic](#test-statistic)
* [Level of Significance](#level-of-significance)
* [p-Value and Decision Rule](#p-value-and-decision-rule)
* [Steps in Hypothesis Testing](#steps-in-hypothesis-testing)
* [One-tailed vs Two-tailed Tests](#one-tailed-vs-two-tailed-tests)
* [Types of Tests](#types-of-tests)
* [When to Use Which Test](#when-to-use-which-test)
* [Illustrative Examples](#illustrative-examples)


---

## Introduction

**Hypothesis testing** is a statistical method used to make decisions about population parameters based on sample data. It is a core concept in inferential statistics used in scientific studies, data analysis, and quality control.
![image](https://github.com/user-attachments/assets/40ef34de-3eab-45d6-a2bd-718ed43cd1fa)


---

## Basic Terminology

* **Population**: The entire group you're interested in studying.
* **Sample**: A subset of the population selected for analysis. ![image](https://github.com/user-attachments/assets/53c1abf9-d0db-4915-a6c6-0a3ffc922788)
* **Parameter**: A measurable characteristic of a population.
* **Statistic**: A measurable characteristic derived from a sample.
* **Null Hypothesis (H₀)**: Assumes no effect or no difference; the default assumption.
* **Alternative Hypothesis (H₁ or Hₐ)**: Represents what you are trying to prove.
![image](https://github.com/user-attachments/assets/f1c518e6-e247-4f81-a49d-f43ab3984d8b)


---

## Types of Hypotheses

1. **Simple Hypothesis**: Specifies the population distribution completely.
2. **Composite Hypothesis**: Does not completely specify the distribution.
3. **Null Hypothesis (H₀)**: Represents the status quo.
4. **Alternative Hypothesis (H₁ or Hₐ)**: Indicates a change or effect.
![image](https://github.com/user-attachments/assets/d680675a-61fb-41b1-a3e1-e6bce7a3831a)
![image](https://github.com/user-attachments/assets/7cebe65c-80c1-4e6b-8b1a-ec8b1d028d80)

---
## One-tailed vs Two-tailed Tests

* **One-tailed test**: Tests for deviation in one direction (greater than or less than).
* **Two-tailed test**: Tests for deviation in both directions (not equal to).
![image](https://github.com/user-attachments/assets/cd07bf0c-6fd4-4a99-be06-cf88118f2252)

Examples:

Does a New Drug Affect Blood Pressure?
Imagine a pharmaceutical company has developed a new drug that they believe can effectively lower blood pressure in patients with hypertension. Before bringing the drug to market, they need to conduct a study to assess its impact on blood pressure.
> Null Hypothesis: (H0)
The new drug has no effect on blood pressure.

> Alternate Hypothesis: (H1) - Two tailed test 
The new drug has an effect on blood pressure.

> Alternate Hypothesis: (H1) - One tailed test.
- The new drug increases blood pressure 
    (Right tailed)
- The new drug decreases blood pressure 
    (Left tailed) 



---
## Errors in Hypothesis Testing

* **Type I Error (α)**: Rejecting a true null hypothesis.
* **Type II Error (β)**: Failing to reject a false null hypothesis.
![image](https://github.com/user-attachments/assets/dd1be08f-a015-4fc3-9a35-957a0b7c6bda)

**Power of the test** = 1 - β

---

## Test Statistic

A **test statistic** is a standardized value computed from sample data. It is used to decide whether to reject the null hypothesis.

Examples:

* z-test
* t-test
* Chi-square test
* F-test


> if test-statistic (t) > critical Value (C), we reject Null Hypothesis.
> If test-statistic (t) ≤ critical value (C), we fail to reject Null Hypothesis.

---

## Level of Significance (α)

The **significance level** (usually 0.05 or 0.01) is the probability of committing a Type I error. Common notations:

* α = 0.05 (5%)
* α = 0.01 (1%)
![image](https://github.com/user-attachments/assets/20ed9352-a282-4408-ac35-21aadebf8eb0)

---

## p-Value and Decision Rule

* **p-value**: Probability of obtaining test results at least as extreme as the results actually observed, under the assumption that the null hypothesis is true.
* **Decision Rule**:

  * If p-value < α: Reject H₀
  * If p-value ≥ α: Do not reject H₀
![image](https://github.com/user-attachments/assets/6204b4ef-c4a1-4417-b1b5-aefb2c0bc21c)
> The region inside which the null hypothesis is going to be accepted is called Acceptance Region. 
> The region where it is going to be rejected is called Critical Region /Rejection Region. 
> The point where the level of significance separating both the region is called Critical value.

---

## Steps in Hypothesis Testing

1. Problem Statement
2. Formulate Hypotheses
3. Choose Significance Level (α)
4. Select Appropriate Test
5. Collect Data and Calculate Test Statistic
6. Determine Critical Region
7. Calculate P-value
8. Make Decision
9. Draw Conclusion
10. Check Assumptions and Validate Results


---



## Types of Tests

1. **z-test**: Used when population variance is known and sample size is large (n > 30).
2. **t-test**: Used when population variance is unknown and sample size is small (n ≤ 30).
3. **Chi-square test**: Used for categorical data to test independence or goodness-of-fit.
4. **F-test**: Used to compare two variances.

---

## When to Use Which Test

| Situation                      | Test Type       |
| ------------------------------ | --------------- |
| Large sample, known variance   | z-test          |
| Small sample, unknown variance | t-test          |
| Categorical data               | Chi-square test |
| Comparing variances            | F-test          |

---
