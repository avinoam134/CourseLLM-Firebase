# Individual Work Report – Using LLM in the Project

## Student Details

**Name:** Tamar Margalit Mann (Peretz)  
**Mail:** ptamar@post.bguac.il  
**Part in project:** file-management feature

---

## 1. My Part in the Work

Setting up authentication on the page with Idan and Roee. Writing unit tests in Jest and listing and attempting to run E2E tests in Playwright with Idan. Understanding the code execution in GitHub environment after writing in Firebase.

**Personal note:** I should mention that towards the last month of the course, I entered my last month of pregnancy, and as a result, I was unable to attend in person during this period due to a medical condition and frequent hospital visits (a situation that also affected my level of involvement in the group work). I did my best to contribute my part, and without Idan, I would not have been able to express myself even in this.

---

## 2. LLM Usage During the Work

LLM was used for:

- Understanding how to activate Auth on our feature page by bringing in the explanation documents from the team that was responsible for it
- Organizing and arranging configuration files (package.json, playwright.config.ts)
- Analyzing existing code and suggesting fixes
- Installation instructions for testing environments (Jest, Playwright)
- Identifying causes of errors in running E2E tests
- Adapting solutions to Firebase Studio environment without root permissions and understanding the problem, which led us to move to work in the GitHub Codespaces environment

---

## 3. How the LLM Worked and the Difficulties Discovered

The LLM provided good technical guidance, suggested solutions based on common experience, and explained errors in a gradual manner. It explained step by step how to perform operations we didn't know in the code. It explained appendices of other groups when needed in a concise and good manner.

However, limitations were discovered when:

- The execution environment (Firebase Studio) limited the installation of system dependencies
- There was a need for specific knowledge about development environment configuration
- Manual testing of the system's capabilities in practice was required
- It repeated the same solution to a problem - even though it didn't work and wasn't in the right direction

---

## 4. Prompts I Used

Below are the main prompts I used during the work (in free wording, as they were actually performed):

### Organization and Configuration:
- "I need the scripts part to be in a logical order."
- "Here is my playwright.config.ts and my spec file."

### Working with Playwright and E2E Tests:
- "Help me fix my e2e tests."
- "This is the error I get when running npx playwright test."
- "How do I test role-based access with Playwright?"

### Development Environment:
- "I am in Firebase Studio."
- "I don't have root permissions, how can I install Playwright browsers?"
- "What's the difference between Firebase Studio vs GitHub Codespaces for tests?"

### Authentication and Integration:
- "Here is the auth documentation from the team - help me understand how to implement it."
- "How do I test protected routes that require authentication?"

### Error Analysis:
- "I'm getting ECONNREFUSED error when running tests."
- "Tests pass locally but fail in CI - what could be different?"
- "What's the difference between localhost and 127.0.0.1 for Firebase emulators?"

---

## 5. What I Learned from the Process

I learned how Playwright depends not only on the browser but also on system dependencies, and as a result, we moved to continue working in the GitHub Codespaces environment, which turned out to be a more convenient platform and faster response, similar to the environments we are used to. How a development environment can have a substantial impact. The importance of separating code issues from infrastructure issues. How to formulate precise prompts that lead to a more focused solution.

---

## 6. Actions Performed Manually

- Running CLI commands manually and checking error output
- Checking system permissions and availability of dependencies in the environment
- Adapting code and repeated runs according to environment limitations
- Trial and error with different configurations until finding the appropriate solution
- Decision to move to alternative solutions (GitHub Codespaces instead of Firebase Studio)
- Manual testing of functionality in the browser to verify that tests match reality

---

## 7. Expectations for Future Improvement in LLM

- Earlier and more accurate identification of execution environment limitations
- Proactive recommendation of environment-compatible alternative solutions from the start
- Better adaptation to Cloud IDE platforms and permission limitations
- Reduction of trial and error cycles by identifying the real problem faster
- Ability to identify when a solution has already been tried and didn't work, and to suggest a different direction
