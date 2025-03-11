### **How to Calculate Test Coverage Percentage**  

Test coverage percentage helps measure how much of the application has been tested. The formula varies depending on the type of test coverage you're measuring (e.g., requirements, code, or test case coverage).  

---

### **1️⃣ Test Case Coverage**
This measures the percentage of executed test cases compared to the total planned test cases.  

**📌 Formula:**  
\[
\text{Test Coverage (\%)} = \left( \frac{\text{Number of executed test cases}}{\text{Total number of test cases}} \right) \times 100
\]

**Example:**  
- You planned **200 test cases** for a project.  
- You executed **150 test cases** successfully.  

\[
\text{Test Coverage} = \left( \frac{150}{200} \right) \times 100 = 75\%
\]

So, **75% of the test cases have been executed**.  

---

### **2️⃣ Requirement Coverage**
This measures how many requirements are covered by test cases.  

**📌 Formula:**  
\[
\text{Requirement Coverage (\%)} = \left( \frac{\text{Number of covered requirements}}{\text{Total number of requirements}} \right) \times 100
\]

**Example:**  
- The system has **50 requirements**.  
- **40 requirements** have at least one test case linked.  

\[
\text{Requirement Coverage} = \left( \frac{40}{50} \right) \times 100 = 80\%
\]

So, **80% of the requirements are covered by tests**.  

---

### **3️⃣ Code Coverage (for Automation & Unit Tests)**
This measures the percentage of code executed during testing. It is usually obtained using tools like **JaCoCo, Istanbul, or SonarQube**.  

**📌 Formula:**  
\[
\text{Code Coverage (\%)} = \left( \frac{\text{Number of lines executed}}{\text{Total lines of code}} \right) \times 100
\]

**Example:**  
- A project has **10,000 lines of code**.  
- The tests executed **8,000 lines** during execution.  

\[
\text{Code Coverage} = \left( \frac{8000}{10000} \right) \times 100 = 80\%
\]

So, **80% of the code was executed by tests**.  

---

### **📌 Summary of Test Coverage Calculations**
| Type of Coverage | Formula |
|-----------------|---------|
| **Test Case Coverage** | (Executed Test Cases / Total Test Cases) × 100 |
| **Requirement Coverage** | (Covered Requirements / Total Requirements) × 100 |
| **Code Coverage** | (Executed Lines of Code / Total Lines of Code) × 100 |

Would you like me to show an example with real test data or an automation scenario? 🚀