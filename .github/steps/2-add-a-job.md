# Step 2: Add a job to your workflow file

_Nice work! :tada: You added a workflow file!_

Here's what the entries in the `welcome.yml` file, on the `welcome-workflow` branch, mean:

- `name: Post welcome comment` gives your workflow a name. This name will appear in the Actions tab of your repository.
- `on: pull_request: types: [opened]` indicates that your workflow will execute whenever someone opens a pull request in your repository.
- `permissions` assigns the workflow permissions to operate on the repository.
- `pull-requests: write` gives the workflow permission to write to pull requests. This is needed to create the welcome comment.

Next, we need to specify jobs to run.

**What is a _job_?**: A job is a set of steps in a workflow that execute on the same runner (a runner is a server that runs your workflows when triggered). Workflows have jobs, and jobs have steps. Steps are executed in order and are dependent on each other. You'll add steps to your workflow later in the course. To read more about jobs, see "[Jobs](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions#jobs)".

In this activity, you'll add a "build" job to your workflow. This job will serve as the foundation for automating tasks, such as building your code or running tests. You'll specify `ubuntu-latest` as the fastest and cheapest job runner available. If you want to read more about why we'll use that runner, see the code explanation for the line `runs-on: ubuntu-latest` in the "[Understanding the workflow file](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions#understanding-the-workflow-file)" article.

## :keyboard: Activity: Add a job to your workflow file

1. In a separate browser tab, make sure you are on the `welcome-workflow` branch and open your `.github/workflows/welcome.yml` file.
1. Edit the file and update its contents to:

   ```yaml
   name: Post welcome comment # Name of the workflow
   on:
     pull_request: # Trigger the workflow on pull request events
       types: [opened]
   permissions:
     pull-requests: write # Grant write permissions to pull requests
   jobs:
     build:
       name: Build Job # Name of the job
       runs-on: ubuntu-latest # Specify the runner environment
   ```

1. After editing the file, validate the workflow syntax using the GitHub Actions workflow editor or a linter.
1. Click **Commit changes** in the top right of the workflow editor.
1. Type a commit message and commit your changes directly to the `welcome-workflow` branch.
1. Wait about 20 seconds, then refresh this page (the one you're following instructions from). Another workflow will run and will replace the contents of this README file with instructions for the next step.

---

### Notes:
- If you're working with Azure, you can use Azure-hosted runners. Learn more about [Azure-hosted runners](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/hosted).
