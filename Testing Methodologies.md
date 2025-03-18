### **Testing Methodologies**  

1. **Agile Testing**  
   - Integrated into the Agile development process, testing occurs continuously throughout sprints.  
   - **Example:** Implementing automated tests for each software increment to ensure that new features do not break existing functionality.  

2. **Shift Left Testing**  
   - Focuses on detecting defects earlier in the development lifecycle by involving QA from the initial stages.  
   - **Example:** Writing test cases and performing unit tests during the development phase rather than waiting until the end of the cycle.  

3. **Waterfall Testing**  
   - Testing is performed in a sequential manner, typically at the end of the development phase.  
   - **Example:** Conducting system and acceptance testing after the entire application is built.  

4. **Test-Driven Development (TDD)**  
   - Requires writing test cases before writing the actual code to guide development.  
   - **Example:** A developer writes a unit test first, sees it fail, then writes the code to pass the test, and refactors as needed.  

5. **Behavior-Driven Development (BDD)**  
   - Focuses on collaboration between developers, testers, and business stakeholders using natural language test scenarios.  
   - **Example:** Using **Cucumber** with Gherkin syntax to create feature files like:  
     ```gherkin
     Given a user is on the login page  
     When they enter valid credentials  
     Then they should be redirected to the dashboard  
     ```  
     
6. **Exploratory Testing**  
   - Testers dynamically explore the application without predefined test cases, focusing on uncovering unexpected issues.  
   - **Example:** Manually navigating through an app to find usability issues or edge cases that automated tests may not cover.  

7. **Regression Testing**  
   - Ensures that new code changes do not introduce defects in existing functionality.  
   - **Example:** Running a suite of automated regression tests after a new feature is deployed.  

8. **Risk-Based Testing**  
   - Prioritizes testing efforts based on the potential business impact and likelihood of failure.  
   - **Example:** Focusing more on testing payment and authentication features in an e-commerce application since they are critical.  
