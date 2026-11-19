# Setup GitHub Repository Template and Issues

## Getting Started with the GitHub Repository Template

This template starts your own project with the starter code and predefined issues.

> 💡 **Recommendation**: Read this entire guide before you start.

### Step 1: Use the Template

This is an individual project: everybody creates their own repository.

1. Click on the "Use this template" button on the GitHub template repository page.
2. Choose **Public** as the visibility.
3. Open the **"Issues"** tab of your new repository. After a short moment, 9 issues appear: 1 setup issue, 7 core stories and 1 bonus story.

> 💡 Do not run the action twice: if the issues are already there, you are done with this step. Only if the "Issues" tab is still empty after a few minutes, open the **"Actions"** tab, select the workflow **create-issues** and click "Run workflow".

### Step 2: Create a GitHub Project Board

1. Go to your repository on GitHub and click on "Projects".
2. Click "New project", choose the "Board" template and name your project.
3. Make sure that "Import items from repository" is checked, then create the project.
4. Set the visibility of your board to public: More options (three dots) -> Settings -> Danger Zone -> Visibility.

### Step 3: Start Working

Clone the repository (Node.js 22.22 or newer is required) and install the dependencies of both parts:

```bash
cd backend && npm i
cd ../frontend && npm i
```

Then follow issue 1. Before you write your first prompt, set up your security baseline as described in Recap Project 6.
