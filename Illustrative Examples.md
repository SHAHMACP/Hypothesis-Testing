## 🌱 Hypothesis Testing Example: Effect of Bio-Fertilizer on Plant Growth

### 📌 Problem Statement

A researcher wants to verify if a **bio-fertilizer increases the height of plants**. A random sample of plants treated with the bio-fertilizer is compared with the known average height of untreated plants.
![image](https://github.com/user-attachments/assets/bd9ae225-2fac-45f8-a52f-62c6c683ab91)

### 🎯 Objective

Determine whether the bio-fertilizer has a statistically significant effect on plant height using hypothesis testing.

---

### 🔬 Step 1: Define the Hypotheses

Let:

* μ = average height of plants with fertilizer
* μ₀ = average height of plants without fertilizer (known = 50 cm)

We test:

* **Null Hypothesis (H₀):** μ = μ₀ (the fertilizer has no effect)
* **Alternative Hypothesis (H₁):** μ > μ₀ (the fertilizer increases plant height)
![image](https://github.com/user-attachments/assets/e034d467-2936-4852-a2ed-4d128d33d9cd)

This is a **right-tailed one-sample t-test**.

---

### 📊 Step 2: Sample Data

A sample of **30 plants** treated with the fertilizer yielded the following heights (in cm):


Population mean (μ₀): 50 cm
Significance level (α): 0.05

---

### 🧮 Step 3: Perform the One-Sample T-Test

```python
import numpy as np
from scipy.stats import ttest_1samp

# Sample data
population_mean = 50
![image](https://github.com/user-attachments/assets/3a231650-9050-4a85-9dae-e38b2c50561a)

# One-sample t-test
t_stat, p_value = ttest_1samp(plant_heights, population_mean)

# For a one-tailed test (μ > μ₀), divide the p-value by 2
p_value_one_tailed = p_value / 2

print(f"t-statistic: {t_stat:.4f}")
print(f"one-tailed p-value: {p_value_one_tailed:.4f}")
if t_stat > 0 and p_value_one_tailed < 0.05:
    print("✅ Reject the null hypothesis — Bio-fertilizer increases plant height.")
else:
    print("❌ Fail to reject the null hypothesis — No sufficient evidence.")
```

> Set the significance level 𝛼 to 0.05 (5%). 
This means there’s a 5% risk of concluding that the bio-fertilizer increases plant growth when, in reality, it doesn’t.

> Check Assumptions: 
- Normality: Plant growth in both groups should follow a normal distribution.
- Independent Samples: The control and treated groups must be independent.

The researcher collects plant height data:

![image](https://github.com/user-attachments/assets/cc6db0cf-c509-46fd-88a7-04a8bb5363c4)

Use the formula to calculate the t-statistic:

![image](https://github.com/user-attachments/assets/8421b659-345a-49e2-b4bc-07d937e7dca0)
> Select Appropriate Test: 
Since we're comparing the means of two groups (treated vs. control), use a two-sample t-test (assuming plant growth follows a normal distribution).

---

### 📈 Step 4: Results

- Determine Critical Value: 
From a t-table, the critical value for 𝛼=0.05 (one-tailed) and 𝑑𝑓=58(Degrees of freedom (𝑑𝑓) can be approximated as 𝑛1+𝑛2−2=58) is 1.671.

- **The critical region is t>1.671.**

- Make a Decision : 
The calculated t-value is **2.52**, which is greater than the critical value **1.671**.

- Decision: **Reject 𝐻0​.**
"The bio-fertilizer significantly increases plant growth at a 5% significance level."

* **T-statistic**: \~2.52

![image](https://github.com/user-attachments/assets/aa7f51ac-447e-4af9-b1ee-da961b483d5a)

---

### ✅ Conclusion

There is strong statistical evidence at the 5% significance level to conclude that the **bio-fertilizer increases plant height**.

---
