# 📊 Types of Hypothesis Tests

This document summarizes how to choose an appropriate statistical hypothesis test based on the characteristics of your data. 

Hypothesis tests are like detective tools that help us make decisions about data.

We use different tests depending on:
- How much information we have (Sample size).
- How many groups or samples we are comparing (Number of sample).
- Data type
- Is the Data Normal or not. 


---

## 🧭 Flowchart for Selecting the Right Hypothesis Test

![image](https://github.com/user-attachments/assets/e73ba172-7861-4d39-8ee9-095d541b2b78)

![image](https://github.com/user-attachments/assets/1441b5d5-401b-40c9-af45-0b566a55d433)


---

## ✅ Step-by-Step Decision Guide

### **Step 1: Data Type**

* Begin with **Quantitative Data** (continuous or interval-scale).

---

### **Step 2: Is the Data Normally Distributed?**

* ✅ Yes → Proceed to parametric tests.
* ❌ No → Use **Non-Parametric Tests** (see section below).

---

### **Step 3: Number of Samples**

* 🔹 **1 Sample**
* 🔹 **2 Samples**
* 🔹 **>2 Samples** → Use **One-Way ANOVA**

---

## 🔬 Parametric Tests

### ▶ 1-Sample Tests

| Condition                                       | Use This Test         |
| ----------------------------------------------- | --------------------- |
| Population standard deviation known & n > 30    | **One-Sample z-test** |
| Population standard deviation unknown or n < 30 | **One-Sample t-test** |

---

### ▶ 2-Sample Tests

#### Are the samples independent?

* ❌ No → Use **Paired t-test** or **Paired z-test**
* ✅ Yes → Check variance equality:

  * Equal Variances → **Independent t-test/z-test**
  * Unequal Variances → **Welch's t-test**

---

## ⚖ Non-Parametric Tests

Use these when the data is **not normally distributed**.

| Use Case                        | Test Name                     |
| ------------------------------- | ----------------------------- |
| One-sample, non-normal          | **Wilcoxon Signed-Rank Test** |
| Two independent samples         | **Mann-Whitney U Test**       |
| More than 2 independent samples | **Kruskal-Wallis Test**       |

---

## 🧪 Multiple Samples (k > 2)

* ✅ Normal distribution: Use **One-Way ANOVA**
* ❌ Non-normal distribution: Use **Kruskal-Wallis Test**

---

## 📎 Summary Table

| Scenario                             | Normal? | Sample Size | Std Dev Known? | Independent? | Equal Variance? | Recommended Test          |
| ------------------------------------ | ------- | ----------- | -------------- | ------------ | --------------- | ------------------------- |
| One-sample, normal, known std dev    | Yes     | Any         | Yes            | —            | —               | One-Sample z-test         |
| One-sample, normal, unknown std dev  | Yes     | Any         | No             | —            | —               | One-Sample t-test         |
| Two-sample, independent, equal var   | Yes     | Any         | —              | Yes          | Yes             | Independent t-test        |
| Two-sample, independent, unequal var | Yes     | Any         | —              | Yes          | No              | Welch's t-test            |
| Two-sample, paired                   | Yes     | Any         | —              | No           | —               | Paired t-test             |
| One-sample, non-normal               | No      | Any         | —              | —            | —               | Wilcoxon Signed-Rank Test |
| Two-sample, non-normal               | No      | Any         | —              | —            | —               | Mann-Whitney U Test       |
| k-sample, normal                     | Yes     | Any         | —              | —            | —               | One-Way ANOVA             |
| k-sample, non-normal                 | No      | Any         | —              | —            | —               | Kruskal-Wallis Test       |

---
![image](https://github.com/user-attachments/assets/81e825a7-ff6d-4dff-a302-5fdd609f454c)
