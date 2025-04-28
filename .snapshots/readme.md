# Snapshots Directory

This directory contains snapshots of your code for AI interactions. Each snapshot is a markdown file that includes relevant code context and project structure information.

---

## What's Included in Snapshots?

- **Selected Code Files**: Snapshots include the contents of selected code files for reference.
- **Project Structure**: If enabled, snapshots capture the directory structure of your project.
- **User Prompts/Questions**: Your prompt or question for the AI is included for context.

---

## Configuration

You can customize snapshot behavior in the `config.json` file. Options include:
- Enabling or disabling project structure capture.
- Specifying which files or directories to include in snapshots.
- Defining custom tags or metadata for snapshots.

---

## Azure Best Practices

If this project involves Azure, ensure that snapshots and configurations align with Azure best practices:
- Use the `azure_development-get_best_practices` tool if available to validate your repository and workflows.
- Avoid including sensitive information (e.g., credentials or secrets) in snapshots.

---

## Example Snapshot

Here’s an example of what a snapshot might look like:

```markdown
# Sponsors Snapshot

## Project Structure

└─ LICENSE  
└─ [README.md](http://_vscodecontentref_/1)  
└─ [config.json](http://_vscodecontentref_/2)  

## Selected Code

```python
# Example Python Code
def hello_world():
    print("Hello, world!")
```

---

## Additional Resources

- [Azure Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/)
- [GitHub Actions Documentation](https://docs.github.com/actions)
- [Markdown Guide](https://www.markdownguide.org/)
