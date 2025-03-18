# **Test Design Techniques**  

Test design techniques help QA engineers create **efficient and effective test cases**, maximizing coverage while minimizing effort. Below are some commonly used techniques, along with practical examples:  

---

## **1. Equivalence Partitioning (EP)**  
**Concept:** Divides input data into partitions where all values in a group are expected to behave similarly.  

**Scenario:** Testing a video streaming service’s **subscription flow**.  

**Example:** The system has different plans: **Free, Standard, and Premium**. Instead of testing all possible inputs, you divide them into categories:  
- **Free Plan** → No payment required  
- **Standard Plan** → Requires valid payment  
- **Premium Plan** → Requires valid payment + additional verification  

By testing one value from each partition, you **reduce redundant test cases while ensuring comprehensive coverage**.  

---

## **2. Boundary Value Analysis (BVA)**  
**Concept:** Focuses on testing values at the **edges** of input ranges, where defects are more likely to occur.  

**Scenario:** Validating **payment limits** in a subscription-based app.  

**Example:** If the minimum payment allowed is **$5** and the maximum is **$500**, test cases include:  
✅ **Valid inputs:** $5, $6, $499, $500  
❌ **Invalid inputs:** $4, $501  

This ensures the system **handles boundary cases correctly**, preventing errors in real transactions.  

---

## **3. Decision Table Testing**  
**Concept:** Uses a table to define inputs and expected outputs based on different conditions.  

**Scenario:** **Multi-device login rules** for a streaming service.  

**Example Decision Table:**  
| Subscription Plan | Device Limit Exceeded? | Login Allowed? |  
|------------------|----------------------|---------------|  
| Free             | No                   | ✅ Yes        |  
| Free             | Yes                  | ❌ No         |  
| Standard         | No                   | ✅ Yes        |  
| Standard         | Yes                  | ❌ No         |  
| Premium          | No                   | ✅ Yes        |  
| Premium          | Yes                  | ✅ Yes        |  

This technique ensures the **system enforces the correct rules** across different scenarios.  

---

## **4. State Transition Testing**  
**Concept:** Evaluates how the system moves between different states based on user interactions.  

**Scenario:** Testing **Two-Factor Authentication (2FA) login flow**.  

**Example:**  
1️⃣ **Logged Out** → User enters correct credentials → **Awaiting 2FA Code**  
2️⃣ **Awaiting 2FA Code** → User enters correct OTP → **Logged In**  
3️⃣ **Awaiting 2FA Code** → User enters incorrect OTP 3 times → **Account Locked**  
4️⃣ **Account Locked** → User requests password reset → **Logged Out**  

This ensures **proper handling of authentication states**, improving security and user experience.  

---

## **5. Use Case Testing**  
**Concept:** Ensures that real-world **user scenarios** function as expected.  

**Scenario:** Testing **subscription cancellation and refund processing**.  

**Example:**  
- Cancelling **during a free trial** → No charge  
- Cancelling **midway through billing cycle** → Partial refund  
- Cancelling **on the last day** → No refund  

By automating these cases using **Playwright and Jest assertions**, we ensure correct **refund calculations** and **seamless user experience**.  

---

## **6. Exploratory Testing**  
**Concept:** Involves **real-time interaction** with the system to discover unexpected issues.  

**Scenario:** Testing how a **streaming app adapts on mobile devices**.  

**Example:** Using **Playwright’s mobile emulation**, we manually explore:  
- **Video player responsiveness** on iPhone 13 vs. Samsung Galaxy S22  
- **Network interruptions** affecting playback behavior  
- **Subscription button visibility** on smaller screens  

Findings from exploratory testing are later **automated** to prevent regressions.  

---

## **7. Risk-Based Testing**  
**Concept:** Prioritizes test cases based on **business impact** and **failure probability**.  

**Scenario:** Optimizing test execution in **CI/CD pipelines**.  

**Example:**  
- **High-risk areas** (Login, Payments, Video Playback) → **Tested on every deployment**  
- **Medium-risk areas** (User Profile Updates) → **Tested nightly**  
- **Low-risk UI changes** (Color themes, Text updates) → **Tested weekly**  

This reduces **test execution time** while ensuring business-critical features remain stable.  

---

### 🚀 **Why These Techniques Matter?**  
✅ Improve **test efficiency** and **coverage**  
✅ Reduce **manual effort** by **focusing on critical scenarios**  
✅ Ensure **better stability in CI/CD pipelines**  
✅ Prevent **critical defects** from reaching production  
