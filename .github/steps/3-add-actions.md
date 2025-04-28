# Step 3: Add a step to your workflow file

_Nice work adding a job to your workflow! :dancer:_

Workflows have jobs, and jobs have steps. Now, we'll add a step to your workflow.

**What are _steps_?**: Steps are individual tasks that run in sequence within a job. Each step must pass for the next step to execute. Steps can either:

- Run shell scripts.
- Reference reusable actions.

In this activity, you'll add a step to post a comment on new pull requests using a [bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) script and [GitHub CLI](https://cli.github.com/).

## :keyboard: Activity: Add a step to your workflow file

1. Ensure you're still working on the `welcome-workflow` branch.
1. Open your `welcome.yml` file in the `.github/workflows/` directory.
1. Update the contents of the file to:

   ```yaml
   name: Post welcome comment
   on:
     pull_request:
       types: [opened]
   permissions:
     pull-requests: write
   jobs:
     build:
       name: Post welcome comment
       runs-on: ubuntu-latest
       steps:
         - name: Post a welcome comment
           run: gh pr comment $PR_URL --body "Welcome to the repository!"
           env:
             GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
             PR_URL: ${{ github.event.pull_request.html_url }}
   ```

   **Explanation of the Step:**
   - **`run`**: Executes the `gh pr comment` command to post a comment on the pull request.
   - **`env`**: Sets environment variables:
     - `GITHUB_TOKEN`: Automatically provided by GitHub to authenticate the workflow.
     - `PR_URL`: The URL of the pull request, retrieved from the event payload.

   For more details, see "[Automatic token authentication](https://docs.github.com/en/actions/security-guides/automatic-token-authentication)."

1. Save your changes and click **Commit changes**.
1. Type a commit message and commit your changes directly to the `welcome-workflow` branch.
1. Wait about 20 seconds, then refresh this page. A new workflow will run and replace the contents of this README file with instructions for the next step.
