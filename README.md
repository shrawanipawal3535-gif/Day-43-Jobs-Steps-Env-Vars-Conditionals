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

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/da7016c3-4d72-47c2-902f-c4b91d9f2efe" />

### Task 3: Job Outputs

   - Create a job that sets an output — e.g., today's date as a string
   - Create a second job that reads that output and prints it
   - Pass the value using outputs: and needs.<job>.outputs.<name>

   <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/0ea74393-3050-4af9-97d7-5299253f86d8" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/892ede83-8166-4514-8cbc-6a34cd73292c" />

## Task 4: Conditionals

In a workflow, add:

   - A step that only runs when the branch is main
   - A step that only runs when the previous step failed
   - A job that only runs on push events, not on pull requests
   - A step with continue-on-error: true — what does this do?

     <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/4706c085-962f-4e49-83f7-6f1fae89cd72" />

### Task 5: Putting It Together

Create .github/workflows/smart-pipeline.yml that:

  - Triggers on push to any branch
  - Has a lint job and a test job running in parallel
  - Has a summary job that runs after both, prints whether it's a main branch push or a feature branch push, and prints the commit message
