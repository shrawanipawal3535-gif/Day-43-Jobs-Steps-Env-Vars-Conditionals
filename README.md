# Day-43-Jobs-Steps-Env-Vars-Conditionals

### Challenge Tasks

### Task 1: Multi-Job Workflow

1. Create .github/workflows/multi-job.yml with 3 jobs:

    - build — prints "Building the app"
    - test — prints "Running tests"
    - deploy — prints "Deploying"
      
Make test run only after build succeeds. Make deploy run only after test succeeds.
