## Why Devops
Devops is the process of product delivery by ensuring:
- Improving delivery
- Automation
- Quality
- Monitoring
- Testing

## SDLC (software development life cycle)
*Standard developed by a company to design , develop and test a high quality software
*structured process used by software development teams to design, develop, test, and deploy high-quality software efficiently
---
|Phase|Description|key Deliveries|
--------------|-------------------------|-----------------------|
|1. Requirement |Analysis	Collect and analyze business needs and user requirements.	|Requirements Specification Document (SRS)
|2. System Design 	|Plan the system architecture, data flow, and interfaces based on requirements.|	System Design Document, Database Schema
|3. Implementation (Coding)|	Developers write code according to the design documents.|	Source Code, Unit Tests
|4. Testing	|Verify that the software works as intended and meets all requirements.|	Test Cases, Bug Reports, QA Sign-off
|5. Deployment	|Release the software to users or production environment.|	Deployment Plan, Release Notes
|6. Maintenance	|Ongoing updates, bug fixes, and performance enhancements after deployment.|	Updated Software Versions, Patches
---
# 🧩 Software Development Life Cycle (SDLC)

## Step 1: Requirement Gathering
- Collect requirements from the customer and analyze feasibility (technical, financial, and operational).
- **Output:** Requirement Specification Document (SRS).

---

## Step 2: Planning
- Plan what needs to be implemented, define project scope, cost, timeline, and risks.
- Finalize the SRS document for design and development reference.

---

## Step 3: Designing
### High-Level Design (HLD)
- Overall architecture, scalability, which tools/technologies, and databases to use.
- Defines system structure and module relationships.

### Low-Level Design (LLD)
- Detailed component-level planning — functions, data flow, APIs, algorithms, performance optimizations.
- UI/UX designs (e.g., Figma) for visual structure.

---

## 🔧 Steps from here are key for a DevOps Engineer

### Step 4: Development (Implementation)
- Developers start coding based on the design.
- Code is uploaded to a central repo (Git/GitHub/GitLab).
- CI/CD pipelines may be configured for automated builds and tests.

### Step 5: Testing
- QA/QE teams test the software quality (unit, integration, system, and user acceptance testing).
- Bugs are fixed and verified before release.

### Step 6: Deployment
- Deploy the tested software to the production server using DevOps tools.
- Includes continuous deployment, containerization (Docker/K8s), and monitoring.

---

## Step 7: Maintenance (Ongoing)
- Monitor performance, fix bugs, and release updates or new features based on feedback.

---

✅ **End Result:** The customer receives a stable, tested, and scalable end product.
#### DevOps eningeer make sure that the step 4,5, and 6 is automated
Automation = Efficiency

(if somone ask about SDLC lifecycle, answer about the pillars of SDLC and then say "as a DevOps engineer im primarily focused on Automating and improving the Devolopment, Testing, and Deployment phase" )
---
# Types of SDLC and about Agile and Scrum:

## 🌊 1. Waterfall Model

### Concept
A step-by-step (linear) approach — like a waterfall, once you move to the next phase, you don’t go back.

---

### Phases
1. Requirement Gathering  
2. System Design  
3. Implementation (Coding)  
4. Testing  
5. Deployment  
6. Maintenance  

---

### Features
- Each stage must be completed before the next begins.  
- Requirements are fixed upfront.  
- Testing happens only after the coding phase.  

---

### Pros
- Simple to understand and manage.  
- Works well when requirements are clear and stable.  

---

### Cons
- Difficult to handle changes once a phase is completed.  
- Late testing = late discovery of issues.  

---

## Use Case
Government, banking, or hardware projects where changes are costly.

---

## ⚡ 2. Agile Model

### Concept
Agile is **iterative and incremental** — the project is divided into small parts (iterations or sprints) that are completed and reviewed continuously.

---

### Key Principles (from the Agile Manifesto)
- Individuals and interactions over processes and tools  
- Working software over documentation  
- Customer collaboration over contract negotiation  
- Responding to change over following a fixed plan  

---

### How It Works
- Work happens in short cycles (sprints) of 1–4 weeks.  
- Each sprint includes planning, coding, testing, and review.  
- Teams continuously get feedback and adapt requirements.  

---

### Pros
- Highly flexible and adaptable.  
- Continuous feedback from users.  
- Frequent releases with working software.  

---

### Cons
- Requires experienced teams and active customer involvement.  
- Less predictable cost and time if scope keeps changing.  

---

### Use Case
Modern software development (web, mobile, startups, DevOps environments).

---

## 🚀 3. Scrum (Agile Framework)

### Concept
Scrum is a **specific implementation of Agile** — it organizes work into short, time-boxed periods called **sprints** (usually 2 weeks).

---

### Key Roles
- **Product Owner:** Defines product goals and manages backlog.  
- **Scrum Master:** Facilitates the process, removes blockers, ensures Agile principles are followed.  
- **Development Team:** Builds, tests, and delivers increments of the product.  

---

### Key Artifacts
- **Product Backlog:** List of features and tasks.  
- **Sprint Backlog:** Items chosen for the current sprint.  
- **Increment:** Working software delivered after each sprint.  

---

### Events
1. **Sprint Planning:** Define what to build this sprint.  
2. **Daily Scrum (Stand-up):** 15-minute progress check.  
3. **Sprint Review:** Demo the completed work to stakeholders.  
4. **Sprint Retrospective:** Discuss improvements for the next sprint.  

---

### Pros
- Very adaptive and collaborative.  
- Clear visibility of pro
- Encourages continuous improvement.  

---

### Cons
- Needs disciplined teamwork.  
- Difficult for very large teams without scaling frameworks.  

---

### Use Case
Software teams working on dynamic, customer-driven projects.
.

# Roles in a Company
---
#### Buisness Analyst:
the one who collects the requirements for the buisness to grow from the customers.He creates a BRD (Buisness requirement Details Document)
#### Product Manager:
the one who connects with the Business Analyst and finalizes the requirements,Dates of completion, he fixes the priorities.The Pm cannot directly interact with the devolopers but interact with the PO.
#### Product owner:
Divides the priorities selected by the PM, breaking them doen to actionable items called Epics.They also dont directly interact with the developers, but interact with the Software Architects.
#### UI/UX designer:
Designs user interface and user experiences
#### Software Architects:
Designs technical system structure and frameworks. He is the person responsible for diving deep into the techincal parts of the Epics and requirements.interacts with the PO and creates the HLD and LLD. Then the new requirements is created.
**To complete this requirements, there is new team - scrum team**
#### Developers:
build based on the req
#### Devops Engineers:
help with dev and ops
#### QE(Quality engineers):
Test and ensure quality
#### SRE:
checks the reliablity of the software, Ensure uptime, peerformance, makes dashboards and documents, tests the final product entirely.
#### Technical writers:
Creates documentation for users and developers.

## Virtual machine
Creating virtual environments, we can create virtual machines inside a single server so that we can split the server into multiple servers logically. Virtual machines installed in a system act independently, in terms of memory, CPU, or processing.

**Hypervisor** is responsible for creating Virtual Machines.
example: VMware, Xen
