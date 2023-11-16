## Batch File Repository: Automating GitHub Actions Setup

This repository offers a batch file (`deploy_gh_p.bat`) to automate the GitHub Actions workflow setup and configure a `vite.config.js` file. This automation process simplifies deploying your project on GitHub Pages to just a few clicks by creating a global task in Visual Studio Code.

### Usage Instructions

1. **Understanding the Files:**

   - This repository provides essential files to automate the GitHub Actions setup. You can refer to ErickKs [tutorial repository](https://github.com/ErickKS/vite-deploy) for a better understanding of how the files should look.

2. **Save the Batch File Locally:**

   - Save the `deploy_gh_p.bat` file to your preferred location on your local machine.

3. **Setting up the Task in Visual Studio Code:**
   - Open Visual Studio Code.
   - Open the Command Palette (Ctrl+Shift+P or Cmd+Shift+P on Mac).
   - Type ">" then "Tasks: Open User Tasks" and select it.
   - Choose "Others" as the template.
   - Replace the content of `tasks.json` with your task configuration:

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Run Deployment Script",
      "type": "shell",
      "command": "C:\\path\\to\\your\\batchfile\\deploy_gh_p.bat",
      "group": {
        "kind": "build",
        "isDefault": true
      },
      "presentation": {
        "reveal": "always",
        "panel": "new"
      },
      "problemMatcher": []
    }
  ]
}
```

- Replace the "command" field with the actual path where you've stored your deploy_gh_p.bat file.
- Note: The "label" field represents the name for your task in Visual Studio Code.

4. **Save the tasks.json file.**

5. **Running the Task:**

- You can now run this task globally from any project in Visual Studio Code.
- Open the Command Palette,Type ">" then "Run Tasks"and select your task ("Run Deployment Script").
