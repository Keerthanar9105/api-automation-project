# API Automation Project

This repo contains a Postman collection and environment for API automation using JSONPlaceholder.
It runs automatically via GitHub Actions using Newman.

## Files
- `API_Automation_Project.postman_collection.json` - Postman collection (CRUD + tests)
- `API_Automation_Project.postman_environment.json` - Postman environment (variables)
- `.github/workflows/newman-tests.yml` - GitHub Actions workflow that runs Newman

## Run locally
1. Install Node.js and Newman:
   ```bash
   npm install -g newman
