# Step 5: Trigger the workflow

_You've now added a fully functioning workflow to your repository! :smile:_

The shell script in the workflow will run whenever a new pull request is opened.

**Seeing your _action_ in action**: The status of each workflow run that's triggered is shown in the pull request before it's merged. Look for **All checks have passed** when you try out the steps below. You can also see a list of all the workflows that are running, or have finished running, in the **Actions** tab of your repository. From there, you can click on each workflow run to view more details and access log files.

![A screenshot of the Actions tab showing a list of workflow runs.](https://user-images.githubusercontent.com/16547949/62388049-4e64e600-b52a-11e9-8bf5-db0c5452360f.png)

## :keyboard: Activity: Trigger the workflow

1. Create a new branch named `test-workflow`.
1. Make a change, such as adding an emoji to your `README.md` file, and commit the change directly to your new branch.
1. In the **Pull Requests** tab, create a pull request to merge `test-workflow` into `main`.
1. Watch the workflow running in the **Checks** section of the pull request.
1. Observe the comment that the workflow adds to the pull request.
1. Wait about 20 seconds, then refresh this page (the one you're following instructions from). Another workflow will run and replace the contents of this README file with instructions for the next step.

---

### Notes

- Ensure that your workflow file is correctly configured before triggering the workflow.
- If you're working with Azure, ensure that your workflow aligns with [Azure DevOps best practices](https://learn.microsoft.com/en-us/azure/devops/pipelines/best-practices).
- If you encounter any issues, refer to the [GitHub Actions Documentation](https://docs.github.com/actions) for troubleshooting.
