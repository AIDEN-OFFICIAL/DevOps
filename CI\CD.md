# 🚀 CI/CD (Continuous Integration and Continuous Deployment)
Together, they represent **automation practices** that help developers **build, test, and release code faster and more reliably**.

**Note:** inside the CD, there is a difference between Continuous Delivery (manual intervention of the product manager to approve ) and Continuous Deployment (nothing manual, fully automated), it depends upon the company policies.

## Stages:
 - Source: pushes a code to a central repository
 - CI monitors a new change in commits
 - Build: automatically combiles the source code and builds it.
 - Test: Run testing scripts
 - Deployment
## 🧠 What is CI/CD?
## ⚙️ Continuous Integration (CI)
Continuous Integration is the practice of **automatically building and testing code** every time a developer pushes changes to a shared repository (like GitHub or GitLab).
### 💡 Goal
To detect bugs early by **integrating code frequently** and ensuring that new changes don’t break existing functionality.

### 🔁 CI Workflow Example
1. Developer pushes code to the main branch.
2. CI server (like GitHub Actions or Jenkins) runs:
   - **Build scripts**
   - **Automated tests**(QA team)
   - **Linting or code analysis (code scanning)**
   - **Image building**
   - **Image Scan**
   - **Image push to registry(Dockerhub)**  
3. If everything passes ✅ → Code is merged.
4. If it fails ❌ → Developer fixes the issue.

---

## 🚚 Continuous Deployment / Delivery (CD)
**Continuous Delivery** ensures that the app is **always in a deployable state** after CI passes.
**Continuous Deployment** goes one step further, it **automatically deploys the changes to production** once tests are successful.

### ⚙️ Example Flow
1. CI finishes building and testing.
2. CD takes over to:
   - Deploy to a staging environment (for testing)
   - Or automatically release to production

---

## 🧩 Why CI/CD Matters

| Benefit | Description |
|----------|--------------|
| 🧪 **Faster Testing** | Every commit is tested automatically |
| ⚡ **Quicker Releases** | New features can reach users faster |
| 🧍‍♂️ **Less Human Error** | Automation reduces manual mistakes |
| 🛡️ **Better Quality** | Bugs are caught early |
| 📈 **Scalability** | Easier to handle large projects and teams |
|🫂**Collaboration**| Effective collaboration between teams|

---

## 🛠️ Common CI/CD Tools

| Category | Tools |
|-----------|-------|
| CI Servers | **GitHub Actions**, **GitLab CI**, **Jenkins**, **CircleCI**, **Travis CI** |
| CD/Deployment | **ArgoCD**, **Spinnaker**, **AWS CodeDeploy**, **Azure Pipelines**, **Heroku** |
| Container Integration | **Docker**, **Kubernetes**, **GitHub Actions runners** |

---
## 🚀 Deployment Strategies in CI/CD
### 1. 🟦🟩 **Blue-Green Deployment**

#### 💡 Concept
Maintain **two identical environments**:
- **Blue**: The current live (production) version.
- **Green**: The new version to be deployed.

You deploy the new release to the **Green environment** while **Blue** continues to serve users.

Once everything in Green is tested and verified (staging):
- The **traffic is switched** (load balancer) from Blue → Green.
- Green becomes live production.
- Blue becomes the backup.

#### ✅ Pros
- **Zero downtime**
- **Instant rollback** possible
- **Easy testing** in a real environment

#### ❌ Cons
- Requires **double infrastructure**
- Slightly **costlier** for large systems

---

---

### 2. 🐤 **Canary Deployment**

#### 💡 Concept
Deploy the new version **gradually** to a **small percentage** of users (the “canaries”), then slowly increase rollout if everything is stable.

#### ⚙️ Workflow
1. Deploy v2 to 5% of users.
2. Monitor metrics (errors, latency, user feedback).
3. If stable → increase rollout to 25%, 50%, 100%.
4. If unstable → rollback to v1.

#### ✅ Pros
- **Low risk**, since only a few users see new version first.
- **Real-world testing** in production.
- **Rollback** affects only a small user group.

#### ❌ Cons
- Requires **traffic control** (load balancer or service mesh).
- **Complex monitoring** setup needed.

---

### 3. 🔁 **Rolling Deployment**

#### 💡 Concept
Deploy the new version **incrementally** by replacing old instances with new ones in **batches** until all are updated.

There’s only **one environment**, but deployment happens gradually.

#### ⚙️ Workflow
1. Take a few old servers offline.
2. Deploy new version to them.
3. Bring them online, continue with next batch.

#### ✅ Pros
- No need for duplicate infrastructure.
- Minimal downtime.
- Works well with containerized apps (Kubernetes).

#### ❌ Cons
- Harder rollback (partially updated environment).
- Possible **inconsistencies** if versions mix.

---

## 🧩 Comparison Table

| Strategy | Downtime | Rollback Ease | Infrastructure Cost | Risk Level | Ideal For |
|-----------|-----------|----------------|---------------------|-------------|------------|
| **Blue-Green** | ❌ None | ✅ Easy | 💸 High | 🔹 Low | Production releases |
| **Canary** | ❌ None | ✅ Easy | 💸 Medium | 🔹 Low | Gradual rollouts |
| **Rolling** | ⚙️ Minimal | ⚠️ Moderate | 💸 Low | 🔹 Medium | Container apps |
| **A/B Testing** | ❌ None | ⚙️ Complex | 💸 High | 🔹 Low | UX/feature tests |
| **Recreate** | ⏸️ Yes | ❌ Hard | 💸 Low | 🔹 High | Small apps/dev testing |

---

## 🧭 Choosing the Right Strategy

| Goal | Recommended Strategy |
|------|-----------------------|
| Fast, risk-free deployment | **Blue-Green** |
| Gradual rollout & monitoring | **Canary** |
| Continuous small updates | **Rolling** |
| Experiment with features | **A/B Testing** |
| Quick simple deploy | **Recreate** |

---
```yaml
# =========================================================
# 🚀 Example: Full CI/CD Pipeline using GitHub Actions
# =========================================================
# This pipeline:
# 1️⃣ Runs tests on every push (Continuous Integration)
# 2️⃣ Builds a Docker image
# 3️⃣ Pushes it to Docker Hub
# 4️⃣ Deploys to a remote server via SSH (Continuous Deployment)
# =========================================================

name: Full CI/CD Pipeline

on:
  push:
    branches:
      - main  # Run the pipeline whenever code is pushed to 'main'

jobs:
  # =========================================================
  # 1️⃣ Continuous Integration: Build and Test
  # =========================================================
  test:
    name: 🧪 Run Build & Tests
    runs-on: ubuntu-latest

    steps:
      - name: 📥 Checkout Repository
        uses: actions/checkout@v4

      - name: 🧰 Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '20'

      - name: 📦 Install Dependencies
        run: npm install

      - name: 🧪 Run Tests
        run: npm test

  # =========================================================
  # 2️⃣ Continuous Deployment: Build & Push Docker Image
  # =========================================================
  build_and_push:
    name: 🐳 Build and Push Docker Image
    runs-on: ubuntu-latest
    needs: test   # Run this job only if tests pass ✅

    steps:
      - name: 📥 Checkout Repository
        uses: actions/checkout@v4

      - name: 🔧 Set up Docker Buildx
        uses: docker/setup-buildx-action@v3

      - name: 🔐 Login to Docker Hub
        uses: docker/login-action@v3
        with:
          username: ${{ secrets.DOCKER_USERNAME }}
          password: ${{ secrets.DOCKER_PASSWORD }}

      - name: 🐳 Build and Push Docker Image
        uses: docker/build-push-action@v6
        with:
          context: .
          push: true
          tags: ${{ secrets.DOCKER_USERNAME }}/myapp:latest

  # =========================================================
  # 3️⃣ Deployment to Remote Server (CD)
  # =========================================================
  deploy:
    name: 🚀 Deploy to Server
    runs-on: ubuntu-latest
    needs: build_and_push  # Run this job only after Docker image is pushed

    steps:
      - name: 📥 Checkout Repository
        uses: actions/checkout@v4

      - name: 🔐 Connect to Server and Deploy
        uses: appleboy/ssh-action@v1.1.0
        with:
          host: ${{ secrets.SERVER_HOST }}
          username: ${{ secrets.SERVER_USER }}
          key: ${{ secrets.SERVER_SSH_KEY }}
          script: |
            echo "🚀 Pulling latest Docker image..."
            docker pull ${{ secrets.DOCKER_USERNAME }}/myapp:latest

            echo "🧹 Stopping old container..."
            docker stop myapp || true && docker rm myapp || true

            echo "🏗️ Starting new container..."
            docker run -d --name myapp -p 80:3000 ${{ secrets.DOCKER_USERNAME }}/myapp:latest

            echo "✅ Deployment Complete!"
```
