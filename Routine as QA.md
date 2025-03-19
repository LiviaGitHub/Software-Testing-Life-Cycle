# **📅 My Work Routine as a QA Engineer**  

Integrating **Shift Left Testing, Regression Testing, Agile Methodology, BDD, Exploratory Testing, CI/CD, Sprint Planning, Retrospectives, Test Planning Documentation, Bug Analysis & Monitoring, and Releases**.  

## **🗓 Weekly Agile Ceremonies & Planning**  

### **📌 Sprint Planning (Every Two Weeks)**
- Participate in **Sprint Planning** with developers, product managers, and designers.  
- Review upcoming features for **user signup, payment, and user profile**.  
- Define **test coverage, automation strategy, and potential risks**.  
- Ensure all acceptance criteria are **testable** and plan necessary test cases.  

✅ **Outcome:** A clear roadmap for testing efforts in the sprint.  

---

### **📌 Sprint Retrospective (Every Two Weeks)**
- Reflect on what went well, what needs improvement, and next steps.  
- Identify **testing bottlenecks** (e.g., flaky tests, slow regression suites).  
- Discuss **process improvements**, such as adding more automation coverage.  

✅ **Outcome:** A more efficient testing workflow for the next sprint.  

---

## **🕘 09:00 AM – Daily Standup (Agile Methodology)**  
- Join the **daily standup** with the team.  
- Provide updates on testing progress and blockers.  
- Collaborate with developers to resolve defects quickly.  

✅ **Outcome:** Daily alignment to maintain sprint velocity.  

---

## **🕙 10:00 AM – Test Planning Documentation & Shift Left Testing**
- **Review requirements** for new features (Signup, Payment, User Profile).  
- Write a **Test Plan** covering:
  - Test scenarios (Functional, UI, API, Performance)  
  - Automation strategy (What will be automated vs. manually tested?)  
  - Risk analysis and mitigation strategies  

🔹 **Example Test Plan for Signup Flow:**  
| Test Case | Description | Expected Result | Test Type | Automated? |
|-----------|------------|----------------|------------|------------|
| TC01 | Sign up with valid email & password | User receives confirmation email | Functional | ✅ |
| TC02 | Sign up with an invalid email | Error message displayed | Negative | ✅ |
| TC03 | Sign up with an already registered email | Error message displayed | Negative | ✅ |

✅ **Outcome:** Well-defined testing strategy before development starts (**Shift Left**).  

---

## **🕛 12:00 PM – Test Automation Development (CI/CD & Regression Testing)**
- Implement **Playwright & Jest** test cases for signup, payment, and profile features.  
- Run tests locally before committing.  
- Push code to GitHub and trigger **CI/CD pipeline**.  

🔹 **Example CI/CD Workflow (GitHub Actions)**
```yaml
name: Run Tests

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Code
        uses: actions/checkout@v3
      - name: Install Dependencies
        run: npm install
      - name: Run Unit Tests
        run: npm test
      - name: Run UI Tests
        run: npx playwright test
```
✅ **Outcome:** Early detection of defects before deployment.  

---

## **🕒 03:00 PM – Exploratory Testing & Bug Analysis**
- Perform **exploratory testing** on new features and bug fixes.  
- Identify **uncovered edge cases** and potential UX issues.  
- Log defects in **JIRA**, including steps, logs, and screenshots.  
- Work with developers to analyze logs and **monitor production issues**.  

🔹 **Example Bug Report (JIRA Ticket)**
**Summary:** Payment fails when using Visa card  
**Steps to Reproduce:**  
1. Navigate to the payment page  
2. Enter valid Visa card details  
3. Click "Submit"  
**Expected Result:** Payment is successful  
**Actual Result:** Error message "Payment Failed" displayed  
**Severity:** Critical  
**Logs & Screenshots:** Attached  

✅ **Outcome:** Quick defect resolution and fewer production issues.  

---

## **🕔 05:00 PM – Regression Testing & Pre-Release Validation**
- Run **automated regression tests** for signup, payment, and user profile.  
- Perform **manual sanity checks** on critical workflows.  
- Analyze test reports, investigate failures, and fix flaky tests.  

✅ **Outcome:** Stable release with minimal risk.  

---

## **🕕 06:00 PM – Release Management & Monitoring**
- Validate release readiness:  
  - Are all tests passing? ✅  
  - Are major bugs resolved? ✅  
  - Are deployment rollback plans in place? ✅  
- Work with DevOps to **monitor the release in production**.  
- Check for **real-time errors & crashes** using monitoring tools (**Datadog, Sentry, New Relic**).  
- Conduct a **post-release analysis**:  
  - Were there any critical issues?  
  - Do we need a hotfix?  

✅ **Outcome:** A smooth deployment with minimal post-release defects.  

---

# **🌟 Summary: My QA Routine at Zattoo**
| Time  | Activity |
|--------|------------|
| **Weekly** | Sprint Planning, Retrospective, Test Plan Documentation, Bug Monitoring |
| **09:00 AM** | Daily Standup |
| **10:00 AM** | Test Planning & Shift Left Testing |
| **12:00 PM** | Test Automation (CI/CD, Playwright) |
| **03:00 PM** | Exploratory Testing & Bug Analysis |
| **05:00 PM** | Regression Testing & Pre-Release Checks |
| **06:00 PM** | Release & Monitoring |

---

### 🚀 **Why This Routine Works?**
✅ **Shift Left Testing** → Bugs detected before coding starts  
✅ **Automated & Manual Testing** → Best of both worlds  
✅ **CI/CD Integration** → Faster feedback loops  
✅ **Exploratory Testing** → Catch unexpected issues  
✅ **Release Monitoring** → Stable production deployments  
