 # All about Software Testing

Software testing is the  activity of checking if the actual results match the expected results, and also ensures that the softwaare is defect free. 

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

Here’s a concise and easy-to-copy **Markdown version** with single-paragraph explanations 👇

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
| **Contract Acceptance Testing**          | Checks if software meets agreed requirements in the contract. |
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




