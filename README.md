# Hello GitHub Actions

_Create and run a GitHub Actions workflow._

## README for `README.md`

This file serves as the main documentation for the "Hello GitHub Actions" course. It provides an introduction to GitHub Actions and guides users through creating and running their first GitHub Actions workflow.

## Table of Contents

1. [Introduction](#hello-github-actions)
2. [File Structure](#file-structure)
3. [Key Features](#key-features)
4. [How to Use](#how-to-use)
5. [License](#license)
6. [Step 1: Create a Workflow File](#step-1-create-a-workflow-file)

## File Structure

The file is structured as follows:

1. **Header Section**: Contains the title and a brief description of the course.
2. **Step-by-Step Instructions**: Guides users through creating a workflow file, setting up a pull request, and understanding GitHub Actions concepts.
3. **Footer Section**: Includes helpful links for further learning, support, and licensing information.

## Key Features

- **Introduction to GitHub Actions**: Explains what GitHub Actions are and their benefits.
- **Step-by-Step Activities**: Provides detailed instructions for creating and running workflows.
- **Helpful Resources**: Links to GitHub Actions documentation and other learning materials.

## How to Use

1. Follow the instructions in the "Activity" sections to complete each step of the course.
2. Use the provided links to explore additional resources and documentation.
3. Refer to the footer for support and licensing information.

## License

This file is licensed under the MIT License. See the footer section for more details.

## Step 1: Create a Workflow File

_Welcome to "Hello GitHub Actions"! :wave:_

**What is _GitHub Actions_?**: GitHub Actions is a flexible way to automate nearly every aspect of your team's software workflow. You can automate testing, continuously deploy, review code, manage issues and pull requests, and much more. The best part is that these workflows are stored as code in your repository and can be easily shared and reused across teams. To learn more, check out these resources:

- The GitHub Actions feature page: [GitHub Actions](https://github.com/features/actions)
- The "GitHub Actions" user documentation: [GitHub Actions](https://docs.github.com/actions)

**What is a _workflow_?**: A workflow is a configurable automated process that will run one or more jobs. Workflows are defined in special files in the `.github/workflows` directory and they execute based on your chosen event. For this exercise, we'll use a `pull_request` event.

- To read more about workflows, jobs, and events, see "[Understanding GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)".
- If you want to learn more about the `pull_request` event before using it, see "[pull_request](https://docs.github.com/en/developers/webhooks-and-events/webhooks/webhook-events-and-payloads#pull_request)".

To get you started, we ran an Actions workflow in your new repository that, among other things, created a branch for you to work in, called `welcome-workflow`.

### :keyboard: Activity: Create a Workflow File

1. Open a new browser tab, and navigate to this same repository. Then, work on the steps in your second tab while you read the instructions in this tab.
1. Create a pull request. This will contain all of the changes you'll make throughout this part of the course.

   - Click the **Pull Requests** tab.
   - Click **New pull request**, set `base: main` and `compare: welcome-workflow`, click **Create pull request**, then click **Create pull request** again.

1. Navigate to the **Code** tab.
1. From the **main** branch dropdown, click on the **welcome-workflow** branch.
1. Navigate to the `.github/workflows/` folder, then select **Add file** and click on **Create new file**.
1. In the **Name your file** field, enter `welcome.yml`.
1. Add the following content to the `welcome.yml` file:

   ```yaml
   name: Post welcome comment # Name of the workflow
   on:
     pull_request: # Trigger the workflow on pull request events
       types: [opened]
   permissions:
     pull-requests: write # Grant write permissions to pull requests
   ```

1. After editing the file, validate the workflow syntax using the GitHub Actions workflow editor or a linter.
1. To commit your changes, click **Commit changes**.
1. Type a commit message, select **Commit directly to the welcome-workflow branch**, and click **Commit changes**.
1. Wait about 20 seconds, then refresh this page (the one you're following instructions from). A separate Actions workflow in the repository (not the workflow you created) will run and will automatically replace the contents of this README file with instructions for the next step.

---

### Get Help

- [Post in our discussion board](https://github.com/orgs/skills/discussions/categories/hello-github-actions)
- [Review the GitHub status page](https://www.githubstatus.com/)

&copy; 2025 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)
