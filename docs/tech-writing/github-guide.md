How to Create a GitHub Repository and Upload Files from a Linux Terminal.  


This is a guide to create a GitHub Repository and upload files from a Linux system. It involves using Git to configure your identity, create a remote repository, and pushing your files to GitHub.  

Prerequisites:

A GitHub account 
Linux terminal access
A project folder with files ready to upload. 



Step 1 — Install Git

Git is a system that tracks all changes in your files and uploads those files to GitHub. 

Open terminal and run this command:  sudo apt install git

To verify the installation was successful, run this command : git --version

A successful installation would show: git version 2.x.x

Step 2 — Configure Git

Fill in your name and email, so Git can label your commits correctly. 

To set your username and email, run this command:
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

Entering these details once is valid for as long as you use that particular system.

Step 3 — Create a Repository on GitHub

A repository stores your project on GitHub.

To create a repository, 
	•	Go to github.com and sign in
	•	Click the + icon in the top right
	•	Select New Repository
	•	Enter a repository name
	•	Set visibility to Public
	•	Do not add README or any files
	•	Click Create Repository

This creates a repository in your profile.

Step 4 — Initialize Your Local Project

This prepares your local folder for version control

Navigate to your project folder in terminal with this command: cd your-project-folder

Initialize Git: git init

Stage all files: git add .

Create your first commit: git commit -m "Initial commit"

A commit is a saved snapshot of your files at that point in time.

Step 5 — Connect to GitHub and Push

This links your local project to the remote repository and uploads your files into GitHub.

Run this command to add the remote repository:
git remote add origin https://github.com/yourusername/your-repo-name.git

Then, Rename branch to main: git branch -M main

Now, upload files to GitHub:  git push -u origin main

When prompted:

	•	Username: your GitHub username
	•	Password: your Personal Access Token (not your GitHub password)

To generate a Personal Access Token: go to github.com → Settings → Developer Settings → Personal Access Tokens → Tokens Classic → Generate New Token → select repo scope → copy the token immediately.

Step 6 — Verify
To verify if your Github page is live, 

Go to github.com/yourusername/your-repo-name and confirm your files are visible.
Your project is now live on Github and accessible from any device. 

If not, check the common errors mentioned below and how to fix them. 

Common Errors and Fixes:

Error: git: command not found
Git is not installed on your device or the terminal needs to be restarted.
Fix: Run: sudo apt install git, and open a new terminal window.

Error: src refspec main does not match any
The local branch is named master instead of main.
Fix: Run: git branch -M main, and then push again.

Error: remote origin already exists
You ran git remote add origin twice.
Fix: Run: git remote set-url origin https://github.com/yourusername/your-repo.git

Error: Authentication failed
You entered your GitHub password instead of a Personal Access Token.
Fix: Generate a token at github.com/settings/tokens and use that as your password.

Error: Permission denied
The token doesn’t have the correct permissions.
Fix: Regenerate the token and make sure the repo scope is checked.




