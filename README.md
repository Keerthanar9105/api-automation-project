# 🧩 API Automation Project

[![API Tests](https://github.com/Keerthanar9105/api-automation-project/actions/workflows/newman-tests.yml/badge.svg)](https://github.com/Keerthanar9105/api-automation-project/actions/workflows/newman-tests.yml)

**View the latest API test report:**  
[📄 Click here to see the report](https://Keerthanar9105.github.io/api-automation-project/reports/)

---

## 📌 Project Overview
This repository contains a **Postman collection** and **environment** for API automation testing using [JSONPlaceholder](https://jsonplaceholder.typicode.com/).  
The tests are executed automatically through **GitHub Actions** using **Newman**, and generate an **HTML report**.  

---

## ⚡ Workflow Details
- **Workflow Name:** API Test Workflow (`newman-tests.yml`)  
- **Triggers:**  
  - Push to `main`  
  - Pull Request targeting `main`  
  - Manual run (workflow_dispatch)  
  - Scheduled (cron, 2 AM UTC)  
- **Runner:** `ubuntu-latest`  
- **Steps:**  
  1. Checkout repository  
  2. Setup Node.js  
  3. Install Newman & Newman HTML Extra reporter  
  4. Run Postman collection  
  5. Upload HTML report as artifact  
  6. Deploy report to GitHub Pages  

---

## 🧪 Running Tests Locally
If you want to run the tests on your machine using Newman:

```bash
# Install Newman and reporter
npm install -g newman
npm install -g newman-reporter-htmlextra

# Run the collection
newman run "API_Automation_Project.postman_collection.json" \
  -e "API_Automation_Project.postman_environment.json" \
  -d data/testdata.csv \
  -r htmlextra \
  --reporter-htmlextra-export reports/index.html
