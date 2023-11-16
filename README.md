<div align = "center"> <h1>Automating Vite Deploy </h1>
</div>
This repository offers a batch file `deploy_gh_p.bat` to automate the GitHub Actions workflow setup and configure a `vite.config.js` file. This automation process simplifies deploying your project on GitHub Pages to just a few clicks by creating a global task in Visual Studio Code.

### Usage Instructions

1. **Understanding the Files:**

   - This repository provides essential files to automate the Vite Deploying process. You can refer to ErickKs <a href="https://github.com/ErickKS/vite-react-router">
     <img src="https://img.shields.io/badge/Repository%20-%0A66C2.svg?&style=for-the-badge&logo=GitHub&logoColor=FFFFFF&color=282828" />
     </a>
     or <a href="https://www.youtube.com/watch?v=XhoWXhyuW_I">
     <img src="https://img.shields.io/badge/Youtube_Video%20-%0A66C2.svg?&style=for-the-badge&logo=YouTube&logoColor=FF0000&color=282828" />
     </a> for a better understanding of how the files should look.

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
