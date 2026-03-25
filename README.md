# Day-43-Jobs-Steps-Env-Vars-Conditionals

### Challenge Tasks

### Task 1: Multi-Job Workflow

1. Create .github/workflows/multi-job.yml with 3 jobs:

    - build — prints "Building the app"
    - test — prints "Running tests"
    - deploy — prints "Deploying"
      
Make test run only after build succeeds. Make deploy run only after test succeeds.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/77fad340-7d37-49c0-bb85-d27f62a6b0d1" />

## Task 2: Environment Variables

In a new workflow, use environment variables at 3 levels:

   - Workflow level — APP_NAME: myapp
   - Job level — ENVIRONMENT: staging
   - Step level — VERSION: 1.0.0
     
Print all three in a single step and verify each is accessible.

Then use a GitHub context variable — print the commit SHA and the actor (who triggered the run).
