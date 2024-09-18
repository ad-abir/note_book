## Pushing Code to GitHub
1. Create a Repository on GitHub.

Go to your GitHub account and create a new repository. This will be the remote location where your code will be stored.

2. Set Up Git Locally (if not already done):

- Item 1 git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

These two lines configure Git with your name and email address for future commits.

3. Initialize a Git Repository in Your Project:

git init

Run this command in your terminal while navigating to the directory containing your code. This creates a local Git repository to track changes.

4. Add Files to Staging Area:

git add .    or     git add filename

This command tells Git which files you want to include in your next commit. The . symbol represents all files in the current directory.

5. Commit Your Changes:

git commit -m "Initial commit"

This command creates a snapshot of your current code with a descriptive message. Replace "Initial commit" with a more specific message about your changes.

6. Link Your Local Repository to GitHub:

git remote add origin URL

Replace "URL" with the actual URL of your remote repository on GitHub. You can find this URL on the main page of your repository.

7. Push Code to GitHub:

git push -u origin main

This command pushes your local changes (including the commit message) to the "main" branch of your remote repository on GitHub. The -u flag sets the "origin" remote as the default for future pushes.
