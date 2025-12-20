 # All about Software Testing

Software testing is the  activity of checking if the actual results match the expected results, and also ensures that the software is defect free. 

Testing makes sure the software does what it should and doesn’t do what it shouldn’t.

## 🎯 Objectives of Software Testing

1. ✅ Ensure the software meets the client’s requirements.
2. 🐞 Detect and fix defects early in the development process.
3. ⚙️ Validate that every component and function performs correctly.
4. 🔒 Ensure security, usability, and performance.
5. 📈 Deliver a quality product that provides a good user experience.

## 🔍 Why is Testing Important?

* Prevents costly bugs in production.
* Builds confidence in the software’s stability.
* Reduces maintenance costs.
* Improves customer satisfaction.
* Supports continuous integration and deployment in DevOps environments.

---

## 🧱 Key Components in Testing

| Component            | Description                                                                        |
| -------------------- | ---------------------------------------------------------------------------------- |
| **Test Case**        | A set of steps, inputs, and expected outcomes to verify a feature.                 |
| **Test Plan**        | A document that outlines the strategy, scope, resources, and schedule for testing. |
| **Bug / Defect**     | A mismatch between expected and actual behavior of the software.                   |
| **Test Suite**       | A collection of related test cases.                                                |
| **Test Environment** | Hardware, software, and configurations used to perform testing.                    |

---

## ⚡ Example

Suppose you have a **Login Page**.
A simple test case could be:

| Test Scenario                         | Steps                                        | Expected Result                        |
| ------------------------------------- | -------------------------------------------- | -------------------------------------- |
| Verify login with valid credentials   | Enter valid username & password, click Login | Redirects to Dashboard                 |
| Verify login with invalid credentials | Enter wrong password, click Login            | Displays “Invalid Credentials” message |

---

## 🧠 Key Takeaway

> “Testing is not just about finding bugs — it’s about ensuring software quality and confidence.”

---
# ⚖️ Principles of Software Testing

| Principle                     | Key Idea                                        |
| ----------------------------- | ----------------------------------------------- |
| Presence of Defects           | Testing finds bugs, not proves the absence of them. |
| Exhaustive Testing Impossible | Focus on risk-based testing.                    |
| Early Testing                 | Find bugs early → cheaper fix.                  |
| Defect Clustering             | Most bugs occur in a few modules.                 |
| Pesticide Paradox             | Running the same set of tests repeatedly will no longer find new bugs.
Update test cases often.                        |
| Context Dependent             | Testing approach depends on the type of application, No one-size-fits-all testing.                   |
| Absence of Errors Fallacy     | Correct code ≠ correct product.it can still **fail to meet user needs**              |

---

# 🔍 Verification and Validation (V&V) in Software Testing

**Verification and Validation (V&V)** are two key activities in software testing that ensure a product is built correctly and meets user expectations.

| Concept          | Meaning                                                                                                     |
| ---------------- | ----------------------------------------------------------------------------------------------------------- |
| **Verification** | “Are we building the product right?” — ensures the software follows requirements and design specifications. |
| **Validation**   | “Are we building the right product?” — ensures the final software meets user needs and expectations.        |

---

## 🧱 1. User Requirements Phase → Acceptance Testing

### 🔹 Verification

During this phase, **interviews, meetings, and discussions** are held with clients to gather and confirm requirements.
Artifacts created include:

* **SRS (Software Requirement Specification) Document**
* **Requirement Understanding Documents**
* **UAT Test Cases**
* **Acceptance Test Plan**

### 🔹 Validation

Once the product is ready, **Acceptance Testing** is performed to ensure the software aligns with user expectations.

---

## ⚙️ 2. Software Specification Phase → System Testing

### 🔹 Verification

This phase focuses on **designing the software** and checking the **technical feasibility** of requirements.
Documents produced:

* **System Test Cases**
* **Feasibility Reports**
* **System Test Plan**

### 🔹 Validation

**System Testing** validates that the complete and integrated system meets all functional and non-functional requirements.

---

## 🧩 3. High-Level Design (HLD) Phase → Integration Testing

### 🔹 Verification

Based on the HLD, the **software architecture** is designed — including module interactions, data flow, and database structure.
Artifacts include:

* **Integration Test Plan**
* **Design Documents**
* **Integration Test Cases**
* **Database Table Designs**

### 🔹 Validation

**Integration Testing** ensures that different modules or components work together correctly.

---

## 🔧 4. Low-Level Design (LLD) Phase → Unit Testing

### 🔹 Verification

At this stage, each software component is designed individually with detailed logic.
Activities include:

* **Creation and Review of Unit Test Cases**
* **Unit Test Planning**

### 🔹 Validation

**Unit Testing** validates that individual modules or functions perform as intended.

---

## 🧠 Summary Table

| Phase                      | Verification Artifacts               | Validation Activity     |
| -------------------------- | ------------------------------------ | ----------------------- |
| **User Requirements**      | SRS, UAT Plan, Requirement Docs      | **Acceptance Testing**  |
| **Software Specification** | Feasibility Report, System Test Plan | **System Testing**      |
| **High-Level Design**      | Design Docs, Integration Test Cases  | **Integration Testing** |
| **Low-Level Design**       | Unit Test Cases, Unit Test Plan      | **Unit Testing**        |

---

## 💡 Key Insight

> **Verification** ensures you build the product correctly.
> **Validation** ensures you build the correct product.
---

                     V-MODEL OF SOFTWARE TESTING

                VERIFICATION                            VALIDATION
────────────────────────────────────────────────────────────

        User Requirements Phase                →      Acceptance Testing
               (SRS, UAT Plan)                        (User validation)

                    ↓                                       ↑

        System Specification Phase              →      System Testing
            (Feasibility, System Plan)                 (Entire system check)

                    ↓                                       ↑

        High-Level Design (HLD) Phase            →      Integration Testing
           (Architecture, Module Design)                (Module interaction)

                    ↓                                       ↑

        Low-Level Design (LLD) Phase              →      Unit Testing
           (Component Logic, Functions)                 (Code-level testing)

                    ↓
             Code Implementation

---

# STLC (Software tesing life cycle)

**Software Testing Life Cycle (STLC)** is a sequence of **specific steps** or **phases** followed during the testing process to ensure software quality.
It defines **how testing should be carried out systematically**, from planning to test closure.

---

## 🧩 Phases of STLC

### 🧱 1. Requirement Analysis
Understand *what* needs to be tested.

* Study **SRS (Software Requirement Specification)** or **BRS (Business Requirement Specification)**.
* Identify **testable requirements**.
* Determine testing priorities and risks.
* Identify **types of testing** (functional, performance, security, etc.).

**Deliverables:**

* Requirement Traceability Matrix (RTM) **
* Testable Requirements List

---

### 📝 2. Test Planning
Define the *strategy and approach* for testing.

* Prepare a **Test Plan document**. **
* Define **scope, objectives, resources, environment, and schedule**.
* Identify tools and responsibilities.
* Estimate effort and timelines.

**Deliverables:**

* Test Plan Document
* Effort Estimation Report

---

### 🧪 3. Test Case Design & Development
Create detailed **test cases, test scripts, and test data**.

* Design **positive, negative, edge, and boundary test cases**.
* Create or identify **test data**.
* Prepare **automation test scripts** (if required).
* Review and finalize test cases.

**Deliverables:**

* Test Cases Document **
* Test Data
* Automation Scripts

---

### 🧰 4. Test Environment Setup
Prepare the hardware and software environment for testing.

* Set up **testing servers, databases, and tools**.
* Install the build for testing.
* Ensure environment readiness and connectivity.

**Deliverables:**

* Test Environment Configuration Report
* Smoke Test Results (environment validation) (test if an application is stable)

---

### 🚀 5. Test Execution
Execute tests and compare results with expected outcomes.

**Activities:**

* Run manual or automated test cases.
* Log **defects** in bug tracking tools (like Jira, Bugzilla).
* Retest after fixes and perform regression testing.

**Deliverables:**

* Test Execution Report
* Defect Report

---

### ✅ 6. Test Closure

**Goal:** Wrap up testing and evaluate overall quality.

**Activities:**

* Ensure all test cases are executed or deferred.
* Prepare **test summary and metrics**.
* Conduct **lessons learned / retrospective** meeting.
* Archive test artifacts for future reference.

**Deliverables:**

* Test Closure Report
* Test Summary Report
* Lessons Learned Document

---

## 🧠 STLC Summary Table

| Phase                  | Objective                       | Deliverables                 |
| ---------------------- | ------------------------------- | ---------------------------- |
| Requirement Analysis   | Understand testing scope        | RTM, Requirements List       |
| Test Planning          | Define test approach & strategy | Test Plan, Estimates         |
| Test Case Development  | Create test cases & scripts     | Test Cases, Test Data        |
| Test Environment Setup | Prepare system for testing      | Environment Setup Report     |
| Test Execution         | Run tests & report defects      | Execution Report, Defect Log |
| Test Closure           | Evaluate and close testing      | Summary & Closure Report     |

---

# 🧩 Types of Software Testing — Short Notes

## 🧪 1. Manual Testing
Testing the software **manually without using automation tools**. Testers execute test cases, observe results, and log defects.

* Involves **human effort** and **exploratory testing**.
* Slower but helps find **unexpected issues**.
* Suitable for **small projects** or early development stages.

**Advantages:**

* Flexible and adaptable.
* Better for visual feedback and user experience validation.

**Disadvantages:**

* Time-consuming.
* Prone to human error.
* Difficult to repeat for regression testing.

---

## ⚙️ 2. Automation Testing
Testing done using **automation tools or scripts** to execute test cases automatically.

**Common Tools:**

* **Selenium** (Web UI)
* **Cypress / Playwright** (Frontend)
* **Postman / Newman** (API)
* **Jest / Mocha** (Unit Testing)

**Key Points:**

* Uses code to test code.
* Ideal for **regression, performance, and load testing**.
* Faster, repeatable, and integrates well with **CI/CD** pipelines.

**Advantages:**

* Saves time in long-term testing.
* Increases test coverage.
* Provides detailed reports and metrics.

**Disadvantages:**

* Initial setup cost is high.
* Requires programming knowledge.
* Not suitable for all types of testing (e.g., usability).

---

## 🧠 Quick Comparison Table

| Feature            | Manual Testing        | Automation Testing      |
| ------------------ | --------------------- | ----------------------- |
| **Execution**      | Human                 | Tool / Script           |
| **Speed**          | Slow                  | Fast                    |
| **Accuracy**       | Prone to error        | Highly accurate         |
| **Best for**       | UI, usability, ad-hoc | Regression, performance |
| **Cost (initial)** | Low                   | High                    |
| **Maintenance**    | Low                   | High                    |


---

# 🎨 Methods of Software Testing (Short Notes)

### ⚫ Black Box Testing

Black box testing is where the tester has **no knowledge of the internal code** and focuses only on the **inputs and outputs** of the system. It checks whether the software works as expected without worrying about how it works internally. For example, testing a login form to see if it accepts valid credentials and rejects invalid ones. It mainly focuses on **functionality, user interface, and overall behavior**, and is mostly done by **QA or manual testers**.

---

### ⚪ White Box Testing

White box testing is where the tester has **complete knowledge of the code and logic**. It focuses on testing the **internal workings**, such as loops, conditions, and paths in the program. This helps ensure the code runs correctly and efficiently. It’s usually performed by **developers or automation engineers** using techniques like **unit testing** and **code coverage analysis**.

---

### ⚫⚪ Grey Box Testing

Grey box testing is a mix of both black and white box methods, where the tester has **partial knowledge** of the internal structure or logic. This limited understanding helps design better test cases that cover both **functional behavior** and **data flow** between modules. It’s often used for **integration and web application testing**, typically performed by **SQA or advanced testers**.

---


# ⚙️ Functional vs Non-Functional Testing — Quick Difference

| Functional Testing                     | Non-Functional Testing                 |
| -------------------------------------- | -------------------------------------- |
| Performs before non-functional testing            |  Performs after functional testing          |
| Based on customer requirements             | Based on customer expectations          |
| Tests what the system does             | Tests how the system performs          |
| Features and functionalities, Unit testing, Acceptance testing, Integration testing, regression testing          | Performance Testing, Scalability, Volume testing, Load testing, Stress testing, security, usability       |
| Business requirements                  | Quality attributes                     |
| Login, signup, order placement         | Load time, scalability, reliability    |
| Manual or automation of feature checks | Performance or stress tools            |
| Ensure correct behavior                | Ensure good performance and experience |

---

**In short:**

> Functional = *What it does*
> Non-Functional = *How it does it*
---

# 🐞 Defect Management Stages

1. **Defect Detection** – Testers find and confirm bugs during testing.
2. **Bug Report Formulation** – A detailed report is created with steps, expected vs actual results, and severity.
3. **Bug Fixing** – Developers analyze, fix the defect, and send the updated build for retesting.
4. **Bug List Creation** – All bugs are logged and tracked until verified as fixed and closed. This helps in future reference for solving similar bugs

---
> In short: Detect → Report → Fix → Track ✅

---

# 🪲 Bug Life Cycle (Concise)

**Flow:**

> New → Assigned → Open → Fixed → Retested → Verified → Closed

**Possible alternate paths:**

> Rejected / Deferred / Reopened

---

### 🧭 Explanation 

1. **New** – Tester logs a new defect.
2. **Assigned** – Bug assigned to a developer.
3. **Open** – Developer starts working on it.
4. **Fixed** – Developer resolves the issue.
5. **Retested** – Tester checks the fix.
6. **Verified** – Tester confirms the bug is resolved.
7. **Closed** – Defect is officially closed.
8. **Reopened/Rejected/Deferred** – If issue persists, invalid, or postponed.

---

# 🧩 Unit Testing — (Level 1 of Software Testing)
Tested by: Developers

Unit testing is the process of **testing individual components, functions, or modules** of your application **in isolation** — without depending on databases, APIs, or UI.
The goal is to verify that each “unit” (like a function or class) **works as expected**.

---

### ⚙️ Example 
Let’s say you have this function:

```js
function add(a, b) {
  return a + b;
}
```

Your unit test will check if:

```js
expect(add(2, 3)).toBe(5);
```

### 🧰 Common Tools
 - Backend:  **Jest** / Mocha + Chai
 - Frontend: Jest + React Testing Library
 - MongoDB Mocking: mongodb-memory-server


1. **Test in Isolation** – Mock dependencies like APIs, DB calls, or external services.
2. **Write Small, Focused Tests** – One test per function/behavior.
3. **Use AAA Pattern - (Arrange [set up test data], Act[ call the function], Assert[verify the result])**
4. **Run Tests Automatically** – Integrate with CI tools like GitHub Actions later.


---

# 🔗 Integration Testing (Level 2 of Software Testing)
Tested by: Developers/ Testers

Integration testing checks how **multiple modules or components work together** once they are combined.
It ensures that **data flow, interactions, and communication** between units happen correctly.
In short, it’s about testing **connections**, not just logic.


### ⚙️ Example

* You’ve already tested your `loginController()` and `UserModel` separately (unit tests).
* Now you test **them together** — does the controller properly call the model, validate user credentials, and return the right response?

This verifies that your **backend modules integrate properly**.


### 🧰 Tools for Integration Testing (MERN)
- Backend APIs:**Supertest** (with Jest or Mocha)
- Database Integration: mongodb-memory-server
- Frontend–Backend: Cypress / Playwright

### 🎯 Goal

To ensure that **modules interact correctly**, **data passes smoothly**, and the system behaves as a whole.

---
Here’s a clean, concise note on **System Testing**, perfectly aligned with your roadmap 👇

---

# 🖥️ System Testing (Level 3 of Software Testing)
Tested by: Testers

System testing validates the **entire software system as a whole**.
After integration testing confirms modules work together, system testing ensures the **complete application meets the specified requirements** — both functional and non-functional.
It’s performed on a fully integrated environment, similar to the real-world setup.

---

### ⚙️ Example (MERN Context)

Once your full MERN app (frontend + backend + database) is ready:
You test real user actions like:

* Register → Login → Add to cart → Checkout
  This checks if the entire flow works correctly — not just individual APIs or components.

---

### 🧠 Types of System Testing

- **Functional Testing**  : Ensures features work as expected (e.g., user can place orders).Tools: Selenium, Cypress, Playwright
- **Performance Testing**: Checks speed, load handling, and responsiveness.Tools: JMeter, k6
- **Security Testing**: Ensures data protection and access control.Tools: OWASP ZAP
- **Usability Testing**: Verifies ease of use and design clarity.
- **Compatibility Testing**: Confirms the app works across devices, OS, and browsers.Tools: BrowserStack.

### 🎯 Goal

To verify that the **entire system functions correctly**, satisfies **business requirements**, and is ready for **release testing (UAT)**.


---

# ✅ Acceptance Testing (Level 4 of Software Testing)
Tested by: Client/Testers

Acceptance testing is the **final level of testing**, done to confirm whether the software is **ready for delivery** to the client or end-users.
It ensures the system meets **business requirements** and behaves as expected in real-world use.
This stage often involves both testers and the **client or end-user**.

### ⚙️ Example (MERN Context)

You’ve built a full eCommerce site.
Now, the client checks if they can:

* Create an account
* Add items to the cart
* Place an order and receive confirmation

If all works smoothly, the software is **accepted**.

---

### 🧠 Types of Acceptance Testing

| Type                                     | Description                                                   |
| ---------------------------------------- | ------------------------------------------------------------- |
| **User Acceptance Testing (UAT)**        | Done by end-users or clients to verify business flow.Tools: TestLink, Jira, Zephyr     |
| **Business Acceptance Testing (BAT)**    | Ensures all business goals and processes are met.             |
| **Contract Acceptance Testing**          | Checks if software meets the agreed requirements in the contract. |
| **Operational Acceptance Testing (OAT)** | Validates deployment, backup, and maintenance readiness.      |

---

### 🧰 Tools

| Purpose            | Tools                    |
| ------------------ | ------------------------ |
| UAT Management     | TestLink, Jira, Zephyr   |
| Automation Support | Selenium, Cucumber (BDD) |

---
Tools: Selenium, Cucumber (BDD)

### 🎯 Goal

To ensure the **software fulfills business needs**, **works as intended**, and is ready for **production release**.

---
# JEST

**Jest** is a JavaScript testing framework created by Facebook.
It’s mainly used for testing **JavaScript and Node.js** code — including frontend (React) and backend (Express) projects.

✅ Key Features:

* No config needed — works out of the box
* Built-in test runner, assertion library, and mocking
* Snapshot testing (for UIs)
* Fast execution using parallel test runs

---

## ⚙️ Setup Jest in a Node.js Project

```bash
###  Install Jest
npm init -y
npm install --save-dev jest
```

###  Update your `package.json`

Add this line inside `"scripts"`:

```json
"scripts": {
  "test": "jest"
}
```

Your `package.json` should now look like this:

```json
{
  "name": "jest-demo",
  "version": "1.0.0",
  "scripts": {
    "test": "jest"
  },
  "devDependencies": {
    "jest": "^29.0.0"
  }
}
```

---

## 🧠 Create Your First Function to Test

Inside your project, make a file:
📁 `sum.js`

```js
function sum(a, b) {
  return a + b;
}
module.exports = sum;
```

Then create a test file:
📁 `sum.test.js`

```js
const sum = require('./sum');

test('adds 2 + 3 to equal 5', () => {
  expect(sum(2, 3)).toBe(5);
});
```

---

## Run the Test
```bash
npm test
```

✅ Output should be:

```
PASS  ./sum.test.js
✓ adds 2 + 3 to equal 5 (5 ms)
```

That means your first **unit test** passed! 🎉

---

## 🧩 Understanding Jest Syntax

| Keyword                        | Description                           |
| ------------------------------ | ------------------------------------- |
| `test()`                       | Defines a single test case            |
| `expect()`                     | Used for assertions (to check values) |
| `toBe()`                       | Checks for equality                   |
| `describe()`                   | Groups related tests together         |
| `beforeEach()` / `afterEach()` | Setup and cleanup before/after tests  |

---

## 🧪  A Few Common Matchers

```js
expect(5).toBe(5);                    // strict equality
expect(obj).toEqual({name: "Aiden"}); // object comparison
expect(value).toBeNull();
expect(array).toContain("item");
expect(fn).toThrow("error message");
```

---

## 🕒 Testing Async Functions

Example: `fetchData.js`

```js
async function fetchData() {
  return "Aiden C Terrence";
}
module.exports = fetchData;
```

Test: `fetchData.test.js`

```js
const fetchData = require('./fetchData');

test('resolves to Aiden C Terrence', async () => {
  await expect(fetchData()).resolves.toBe("Aiden C Terrence");
});
```

---

## 🧰Mocking (Advanced)

You can mock external dependencies (like APIs) to test behavior without real calls:

```js
const mockFn = jest.fn();
mockFn('hello');
expect(mockFn).toHaveBeenCalledWith('hello');
```

---

# VITEST

**Vitest** is a modern, blazing-fast testing framework built by the creators of **Vite**.
It’s designed as a drop-in alternative to Jest — but optimized for speed and simplicity.

✅ **Key Features:**

* Lightning-fast startup (powered by Vite)
* Works seamlessly with ES modules
* Supports mocking, snapshots, and coverage
* Jest-compatible syntax (you can reuse Jest tests!)
* Built-in TypeScript & JSX support

---

## ⚙️ Setup Vitest in a Node.js Project

```bash
### Initialize project
npm init -y

### Install Vitest
npm install --save-dev vitest
```

### Update your `package.json`

Add this line inside `"scripts"`:

```json
"scripts": {
  "test": "vitest"
}
```

Your `package.json` should now look like this:

```json
{
  "name": "vitest-demo",
  "version": "1.0.0",
  "scripts": {
    "test": "vitest"
  },
  "devDependencies": {
    "vitest": "^2.0.0"
  }
}
```

---

## 🧠 Create Your First Function to Test

Inside your project, make a file:
📁 `sum.js`

```js
export function sum(a, b) {
  return a + b;
}
```

Then create a test file:
📁 `sum.test.js`

```js
import { test, expect } from 'vitest';
import { sum } from './sum.js';

test('adds 2 + 3 to equal 5', () => {
  expect(sum(2, 3)).toBe(5);
});
```

---

## ▶️ Run the Test

```bash
npm test
```

✅ Output should be:

```
✓ adds 2 + 3 to equal 5 (2 ms)
Test Files  1 passed (1)
      Tests  1 passed (1)
```

That means your first **Vitest unit test** passed! 🎉

---

## 🧩 Understanding Vitest Syntax

| Keyword                        | Description                       |
| ------------------------------ | --------------------------------- |
| `test()` / `it()`              | Defines a single test case        |
| `expect()`                     | Used for assertions               |
| `toBe()`                       | Checks equality                   |
| `describe()`                   | Groups related tests              |
| `beforeEach()` / `afterEach()` | Setup and cleanup                 |
| `vi`                           | Vitest’s mocking & spying utility |

---

## 🧪 Common Matchers

```js
expect(5).toBe(5);
expect(obj).toEqual({ name: "Aiden" });
expect(value).toBeTruthy();
expect(array).toContain("item");
expect(fn).toThrow("error");
```

---

## 🕒 Testing Async Functions

📁 `fetchData.js`

```js
export async function fetchData() {
  return "Aiden C Terrence";
}
```

📁 `fetchData.test.js`

```js
import { test, expect } from 'vitest';
import { fetchData } from './fetchData.js';

test('resolves to Aiden C Terrence', async () => {
  await expect(fetchData()).resolves.toBe("Aiden C Terrence");
});
```

---

## 🧰 Mocking Functions

Vitest uses `vi` for mocking — similar to `jest.fn()`:

```js
import { vi, test, expect } from 'vitest';

test('mock function example', () => {
  const mockFn = vi.fn();
  mockFn('hello');
  expect(mockFn).toHaveBeenCalledWith('hello');
});
```

---

## 📸 Snapshot Testing

Vitest also supports snapshots (just like Jest):

```js
import { test, expect } from 'vitest';

test('matches snapshot', () => {
  const user = { name: "Aiden", role: "SQA Consultant" };
  expect(user).toMatchSnapshot();
});
```

Run once → creates a `__snapshots__` folder.
Run again → compares output; use `--update` to update snapshots:

```bash
npx vitest --update
```

---

## 🧱 Coverage Report

To see test coverage (like Jest):

```bash
npm install --save-dev @vitest/coverage-v8
```

Add this to your `package.json`:

```json
"scripts": {
  "test": "vitest run --coverage"
}
```

Then run:

```bash
npm test
```

✅ You’ll get a full coverage summary in your terminal.

---

## ⚖️ Jest vs Vitest — Quick Comparison

| Feature          | Jest ⚙️                  | Vitest ⚡                 |
| ---------------- | ------------------------ | ------------------------ |
| Speed            | Moderate                 | Very fast (Vite-powered) |
| ESM / TS Support | Limited by setup         | Built-in                 |
| Snapshot Testing | ✅ Yes                    | ✅ Yes                    |
| Mocking          | ✅ jest.fn()              | ✅ vi.fn()                |
| Coverage         | ✅ Built-in               | ✅ Via plugin             |
| Ecosystem        | Mature, stable           | Modern, lightweight      |
| Ideal For        | Node, React, Legacy Apps | Vite, Vue, React, Node   |

---

# 🧪 Supertest 

**Supertest** is a **Node.js library** used to test HTTP APIs.
It allows you to send fake requests (`GET`, `POST`, `PUT`, etc.) to your **Express app** and check the **response** — without actually running the server on a port.

---

### ✅ Why It’s Used

* To test **Express routes** easily
* Works perfectly with **Jest** or **Mocha** or **Vitest**
* You can test endpoints like `/register`, `/login`, `/api/products`
* Helps ensure your **controllers and middleware** work as expected

---

## ⚙️ Setup

```bash
npm install --save-dev supertest jest
```

---

## 🧩 Example — Testing an Express API

📁 `app.js`

```js
const express = require('express');
const app = express();
app.use(express.json());

app.get('/hello', (req, res) => {
  res.status(200).json({ message: 'Hello, Aiden!' });
});

module.exports = app;
```

📁 `app.test.js`

```js
const request = require('supertest');
const app = require('./app');

describe('GET /hello', () => {
  test('should return Hello, Aiden!', async () => {
    const res = await request(app).get('/hello');
    expect(res.statusCode).toBe(200);
    expect(res.body.message).toBe('Hello, Aiden!');
  });
});
```

Then run:

```bash
npm test
```

✅ Output:

```
PASS  ./app.test.js
✓ should return Hello, Aiden! (30 ms)
```

---

## 🧠 How It Works (In Simple Words)

* `request(app)` → creates a virtual request to your Express app
* `.get('/hello')` → simulates a GET request
* `.send()` → sends JSON data for POST/PUT requests
* `.expect()` or `expect()` → checks status codes or responses

---

## 🧰 Example for POST

```js
app.post('/login', (req, res) => {
  if (req.body.username === 'Aiden' && req.body.password === '1234') {
    res.status(200).json({ success: true });
  } else {
    res.status(401).json({ success: false });
  }
});
```

**Test:**

```js
test('should login successfully', async () => {
  const res = await request(app)
    .post('/login')
    .send({ username: 'Aiden', password: '1234' });
  
  expect(res.statusCode).toBe(200);
  expect(res.body.success).toBe(true);
});
```
---
# 🧪 React Testing Library (with Vitest)

**React Testing Library (RTL)** helps test React components in a way that focuses on **user behavior** rather than implementation details.
It simulates how users interact with the UI — clicking buttons, typing, etc.
We’ll use it along with **Vitest** as the test runner.

---

## ⚙️ Setup

```bash
# 1️⃣ Create a new project
npm create vite@latest my-app
cd my-app
npm init -y

# 2️⃣ Install dependencies
npm install -D vitest jsdom
npm install -D @testing-library/react @testing-library/jsdom @testing-library/user-event @testing-library/jest-dom
```

---

## 🧰 Vitest UI (Optional)

Vitest also provides a browser-based UI for running tests visually.

### Install UI:

```bash
npm install -D @vitest/ui
```

### Run Tests with UI:

```bash
npx vitest --ui
```
---

## 📦 Update `package.json`

```json
"scripts": {
  "test": "vitest"
}
```

---

## ⚙️ Configure `vite.config.js`

Add this inside your config file:

```js
test: {
  environment: 'jsdom',
  globals: true
}
```

🧠 **Why jsdom?**
`jsdom` simulates a browser-like environment inside Node.js, so React components can be rendered and tested.

---

## 🧩 Basic Syntax

```js
import { render, screen } from '@testing-library/react';
import { describe, it, expect } from 'vitest';
import MyComponent from './MyComponent';

describe("MyComponent", () => {
  it("renders correctly", () => {
    render(<MyComponent />);
    screen.debug(); // prints the entire screen DOM for debugging
    expect(screen.getByText("Hello Aiden")).toBeInTheDocument();
  });
});
```

---

## 🔍 Query Methods (screen.*)

| Method    | Description                                           | When to Use                            |
| --------- | ----------------------------------------------------- | -------------------------------------- |
| `getBy`   | Finds element immediately (throws error if not found) | Element **must exist**                 |
| `findBy`  | Returns a Promise (waits for element)                 | Element appears **after async action** |
| `queryBy` | Returns null if not found (no error)                  | To check if element **is not present** |

---

## 🖱️ fireEvent vs userEvent

| Method        | Description                                      | Best For                     |
| ------------- | ------------------------------------------------ | ---------------------------- |
| **fireEvent** | Low-level DOM event trigger                      | Simple clicks or key presses |
| **userEvent** | Simulates real user actions (typing, tabs, etc.) | Realistic user interactions  |

Example:

```js
import userEvent from '@testing-library/user-event';

userEvent.type(screen.getByPlaceholderText("Name"), "Aiden");
userEvent.click(screen.getByText("Submit"));
```

---

## 🧠 Mocking & Wrappers (Redux / Router / Context)

When your component uses **Redux**, **Context**, or **React Router**,
wrap it inside a **provider** before testing:

```js
import { Provider } from 'react-redux';
import { BrowserRouter } from 'react-router-dom';

render(
  <Provider store={store}>
    <BrowserRouter>
      <MyComponent />
    </BrowserRouter>
  </Provider>
);
```

This ensures your component behaves exactly like it does in the real app.

---

## 🧩 Utilities

| Utility        | Use                                                            |
| -------------- | -------------------------------------------------------------- |
| `act()`        | Ensures all updates (state, DOM) are applied before assertions |
| `waitFor()`    | Waits for async actions (like API updates)                     |
| `renderHook()` | Tests **custom React hooks** directly                          |

Example:

```js
import { renderHook } from '@testing-library/react';

const { result } = renderHook(() => useCounter());
expect(result.current.count).toBe(0);
```

---

## 💡 VS Code Extensions

* 🧩 **Vitest Snippets** — quick test boilerplates
* 🧩 **Testing Library Snippets** — faster test writing (`rtl` templates)

---
# Integration testing

challenges of integeration testing:
difficult test data management 
multilple ways for testing 
issues when integrated with lagacy system 
challenging test cases
time constraints

## 🧠 What Is Integration Testing?

Integration testing checks whether **different modules or components** of an application work together correctly.
It ensures that data and control flow between components as expected after **unit testing**.

---

## 🧱 Types of Integration Testing

| Type                  | Description                                                                        | Example                                                     |
| --------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| **Big Bang**          | All modules combined and tested at once.                                           | Full-stack app test (backend + frontend) after development. |
| **Top-Down**          | Higher-level modules tested first; lower ones integrated step-by-step using stubs. | Testing API routes first, mocking DB below.                 |
| **Bottom-Up**         | Lower modules tested first; higher integrated later using drivers.                 | Test DB + repo layer, then add controllers.                 |
| **Sandwich (Hybrid)** | Mix of top-down and bottom-up.                                                     | Middle layer integrated both ways.                          |

---

## ⚙️ Integration Testing in Backend

### ✅ Example: Node.js + Express + MongoDB (Using Jest & Supertest)

```js
// __tests__/cart.test.js
import request from 'supertest';
import mongoose from 'mongoose';
import app from '../server.js';
import Cart from '../models/Cart.js';

// Mock Database Connection
beforeAll(async () => {
  const mongoUrl = "mongodb://127.0.0.1:27017/testdb";
  await mongoose.connect(mongoUrl);
});

afterAll(async () => {
  await mongoose.connection.close();
});

// Integration Test
describe('POST /cart/add', () => {
  it('should add product to cart', async () => {
    const res = await request(app)
      .post('/cart/add')
      .send({ userId: '123', productId: 'abc', qty: 2 });

    expect(res.statusCode).toBe(200);
    expect(res.body.success).toBe(true);
  });

  it('should return error if product not found', async () => {
    const res = await request(app)
      .post('/cart/add')
      .send({ userId: '123', productId: 'invalid', qty: 1 });

    expect(res.statusCode).toBe(404);
  });
});
```

### 🧰 Tools Used

| Tool                               | Purpose                                            |
| ---------------------------------- | -------------------------------------------------- |
| **Jest**                           | Test runner & assertions.                          |
| **Supertest**                      | HTTP requests simulation for Express APIs.         |
| **MongoMemoryServer** *(optional)* | Creates an in-memory MongoDB instance for testing. |

---

## 🧩 Frontend Integration Testing
 
### Example: React + Jest + Testing Library

```jsx
// __tests__/LoginIntegration.test.js
import { render, screen, fireEvent, waitFor } from '@testing-library/react';
import Login from '../components/Login';
import axios from 'axios';

jest.mock('axios');

test('login form submits and redirects', async () => {
  axios.post.mockResolvedValue({ data: { success: true } });

  render(<Login />);

  fireEvent.change(screen.getByLabelText(/email/i), { target: { value: 'test@mail.com' } });
  fireEvent.change(screen.getByLabelText(/password/i), { target: { value: '123456' } });
  fireEvent.click(screen.getByText(/login/i));

  await waitFor(() => expect(axios.post).toHaveBeenCalledWith('/api/login', {
    email: 'test@mail.com',
    password: '123456'
  }));
});
```

---

## 🐳 Integration Testing with Docker

### Example: Docker Compose Setup

```yaml
# docker-compose.yml
version: '3.8'
services:
  api:
    build: .
    ports:
      - "4000:4000"
    depends_on:
      - db
    environment:
      MONGO_URL: mongodb://db:27017/testdb
  db:
    image: mongo:6
    ports:
      - "27017:27017"
```

### 🧪 Testing the Integration

```bash
# Start services
docker-compose up -d

# Run tests inside container
docker exec -it api npm test

# Or using Jest command
docker-compose run api npm run test: integration
```

---

## 🧠 Key Notes

* **Mock external dependencies** like APIs or payment gateways.
* **Do not mock DB** for full integration tests; use a test database.
* **Use CI/CD pipelines** (GitHub Actions, Jenkins) to automate test execution.
* **Clean test data** before/after each test to avoid data pollution.
---

# E2E testing(End to End)

## why Playwright over Selenium??

“Since my background is in MERN development, Playwright aligns perfectly with my skill set.
It provides faster execution, auto-waiting, and native support for modern web frameworks,
which helps in creating more reliable end-to-end automation.
Selenium is great for legacy systems, but Playwright gives cleaner and more scalable test automation for CI/CD setups.”

playwright is a frame work built by microsoft.
headlessmode and headed mode , pick locator , record option for instant code genreation, trace, config file of playwright ,various costumizations in playwright, page function , commands like --test ui , and show report, options with testing commands,
