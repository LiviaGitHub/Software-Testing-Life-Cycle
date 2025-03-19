## **🌟 Key Features of CI/CD Workflow Github Actions**

✅ Runs Playwright tests in **parallel** on:  
   - **Desktop Browsers** (Chromium, WebKit, Firefox)  
   - **Mobile Browsers** (Simulated mobile devices using Playwright’s emulation)  
✅ Uses **GitHub Actions matrix strategy** for parallel execution  
✅ Generates test **artifacts (videos, traces, screenshots)** for debugging  
✅ Runs on **Ubuntu** with Playwright dependencies  

---

## **📝 GitHub Actions Workflow (playwright.yml)**  

```yaml
name: Playwright Tests (Parallel Browsers)

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        browser: [chromium, firefox, webkit] # Parallel execution
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v3

      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: 18

      - name: Install Dependencies
        run: npm install

      - name: Install Playwright Browsers
        run: npx playwright install --with-deps

      - name: Run Playwright Tests (${{ matrix.browser }})
        run: npx playwright test --browser=${{ matrix.browser }}

      - name: Upload Test Artifacts (Screenshots, Videos, Traces)
        if: always()
        uses: actions/upload-artifact@v3
        with:
          name: playwright-artifacts-${{ matrix.browser }}
          path: test-results/
```

---

## **📝 Playwright Config (playwright.config.ts)**
Modify your Playwright **config file** to support **multiple browsers and mobile devices**.

```ts
import { defineConfig } from '@playwright/test';

export default defineConfig({
  testDir: './tests',
  timeout: 60000,
  reporter: [['html', { outputFolder: 'test-results' }]],
  use: {
    trace: 'on',
    screenshot: 'on',
    video: 'on',
  },
  projects: [
    {
      name: 'chromium',
      use: { browserName: 'chromium' },
    },
    {
      name: 'firefox',
      use: { browserName: 'firefox' },
    },
    {
      name: 'webkit',
      use: { browserName: 'webkit' }, // Safari engine
    },
    {
      name: 'Mobile Chrome',
      use: { 
        browserName: 'chromium', 
        viewport: { width: 375, height: 812 },
        isMobile: true,
      },
    },
    {
      name: 'Mobile Safari',
      use: { 
        browserName: 'webkit', 
        viewport: { width: 375, height: 812 },
        isMobile: true,
      },
    },
  ],
});
```

---

## **🚀 Explanation**
1. **Parallel Execution**:  
   - `strategy.matrix.browser` runs tests on **Chromium, Firefox, WebKit** in parallel.  
2. **Mobile Testing**:  
   - Playwright's `use: { isMobile: true }` simulates **mobile browsers**.  
3. **Test Artifacts (Debugging)**:  
   - Screenshots, videos, and traces are uploaded to GitHub Actions.  
4. **Cross-Browser Support**:  
   - Tests run on **desktop and mobile** environments.  

---

## **🔹 Running the Workflow**
1. Commit & Push your code  
2. Open **GitHub Actions** tab → Check **Playwright Tests (Parallel Browsers)**  
3. View test **results & artifacts (screenshots, videos, traces)**  

---

### **🔥 Benefits**
✅ **Parallel execution** → Faster test runs  
✅ **Cross-browser & mobile testing** → Ensures real-world coverage  
✅ **CI/CD integration** → Automated quality checks  
✅ **Debugging tools** → Screenshots, videos & traces  
