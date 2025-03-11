### **Equivalence Partitioning (EP) Explained with Practical Examples**  

**Equivalence Partitioning (EP)** is a **black-box testing technique** used to divide input data into different groups (partitions) that are expected to behave similarly. Instead of testing all possible inputs, you select **one representative value** from each partition, reducing the number of test cases while maintaining effective coverage.  

---

## **How It Works in Practice?**  
1. Identify the **input range** of the system.  
2. Divide the inputs into **valid and invalid partitions**.  
3. Select **one representative value** from each partition for testing.  

---

### **Example 1: Age Validation in a Registration Form**  
#### 📌 **Scenario**  
A website requires users to enter their **age (between 18 and 65)** to register.  

#### ✅ **Equivalence Partitions**  
- **Valid Partition:** 18 to 65 → Example: **25 (valid test case)**  
- **Invalid Partition (Too Young):** Less than 18 → Example: **15 (invalid test case)**  
- **Invalid Partition (Too Old):** More than 65 → Example: **70 (invalid test case)**  

💡 **Instead of testing every single age (e.g., 18, 19, 20, …, 64, 65), we pick one from each partition (15, 25, and 70) to efficiently test the system.**  

---

### **Example 2: Password Length Validation**  
#### 📌 **Scenario**  
A system requires a password to be **between 8 and 12 characters long**.  

#### ✅ **Equivalence Partitions**  
- **Valid Partition:** 8 to 12 characters → Example: **"Passw0rd" (valid test case)**  
- **Invalid Partition (Too Short):** Less than 8 characters → Example: **"Pass" (invalid test case)**  
- **Invalid Partition (Too Long):** More than 12 characters → Example: **"SuperLongPassword123" (invalid test case)**  

💡 **This reduces unnecessary tests while covering key scenarios.**  

---

### **Example 3: ATM Withdrawal Limits**  
#### 📌 **Scenario**  
An ATM allows withdrawals between **$20 and $500 per transaction**.  

#### ✅ **Equivalence Partitions**  
- **Valid Partition:** $20 to $500 → Example: **$100 (valid test case)**  
- **Invalid Partition (Too Low):** Less than $20 → Example: **$10 (invalid test case)**  
- **Invalid Partition (Too High):** More than $500 → Example: **$600 (invalid test case)**  

💡 **Testing just three values ($10, $100, and $600) instead of every possible amount saves time and ensures coverage.**  

---

# How to Calculate Test Coverage Using Equivalence Partitioning

To calculate **test coverage** using EP, follow these steps:  

## 📌 Formula for Equivalence Partitioning Coverage
```
EP Coverage (%) = (Tested Partitions / Total Identified Partitions) × 100
```
Where:  
- **Tested Partitions** = The number of partitions covered by at least one test case.  
- **Total Identified Partitions** = The total number of equivalence partitions defined.  

---

## Example 1: Age Validation in a Registration Form
A system allows users to register only if they are between **18 and 65 years old**.  

### ✅ Identified Equivalence Partitions
1. **Valid Partition:** 18 to 65 (**Valid Input**)  
2. **Invalid Partition (Too Young):** Less than 18 (**Invalid Input**)  
3. **Invalid Partition (Too Old):** More than 65 (**Invalid Input**)  

### 🧪 Test Cases Executed
- ✔ **Test Case 1:** Age = `25` (Valid Partition)  
- ✔ **Test Case 2:** Age = `15` (Invalid Partition - Too Young)  
- ❌ **Test Case 3:** Age = `70` (Invalid Partition - Too Old) → **Not tested**  

### 📊 EP Coverage Calculation

EP Coverage = (2 / 3) × 100 = 66.67%

🔹 Since one partition (**Invalid - Too Old**) was **not tested**, the coverage is **66.67%** instead of 100%.  

---

## Example 2: Password Length Validation
A system requires a password to be between **8 and 12 characters long**.  

### ✅ Identified Equivalence Partitions
1. **Valid Partition:** 8 to 12 characters (**Valid Input**)  
2. **Invalid Partition (Too Short):** Less than 8 characters (**Invalid Input**)  
3. **Invalid Partition (Too Long):** More than 12 characters (**Invalid Input**)  

### 🧪 Test Cases Executed
- ✔ **Test Case 1:** Password = `"Passw0rd"` (Valid Partition)  
- ✔ **Test Case 2:** Password = `"Pass"` (Invalid Partition - Too Short)  
- ✔ **Test Case 3:** Password = `"SuperLongPassword123"` (Invalid Partition - Too Long)  

### 📊 EP Coverage Calculation

EP Coverage = (3 / 3) × 100 = 100%

✅ **100% coverage achieved** because all partitions were tested.  

---

### **Benefits of Equivalence Partitioning**  
- **Reduces test cases** without losing coverage.  
- **Ensures all major input types are tested.**  
- **Saves time and effort** compared to exhaustive testing.  
- **Helps identify edge cases efficiently.**  
- **If a partition is missing from tests, the coverage is reduced.**  
- **The goal is to reach 100% EP coverage by ensuring at least one test per partition.**  


