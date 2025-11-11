# 🧩 API Automation Project

![API Tests](https://github.com/Keerthanar9105/api-automation-project/actions/workflows/newman-tests.yml/badge.svg)

This repository contains a Postman collection and environment for **API automation testing** using [JSONPlaceholder](https://jsonplaceholder.typicode.com/).  
The tests are executed automatically through **GitHub Actions** using **Newman**, and generate an HTML report.

---

## 📁 Project Structure
| File | Description |
|------|--------------|
| `API_Automation_Project.postman_collection.json` | Postman collection (CRUD APIs + tests) |
| `API_Automation_Project.postman_environment.json` | Postman environment (base URL, token, etc.) |
| `data/testdata.csv` | Test data used for parameterized runs |
| `.github/workflows/newman-tests.yml` | GitHub Actions workflow to automate Newman execution |
| `reports/` | Folder to store generated Newman HTML reports (artifact) |

---

## ⚙️ Run Locally

1. **Install Node.js & Newman**
   ```bash
   npm install -g newman newman-reporter-htmlextra
