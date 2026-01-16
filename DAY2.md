🚀 Day 2 – Git & GitHub Fundamentals
📌 Objective

The goal of Day 2 was to understand version control using Git and learn how to collaborate and manage code using GitHub, which is essential in DevOps and CI/CD workflows.

🔹 What is Version Control?

Version control is a system that tracks changes made to files over time.
It allows developers to:

Work collaboratively

Track changes

Revert to previous versions

Manage multiple versions of code safely

🔹 What is Git?

Git is a distributed version control system used to track code changes locally and remotely.

Key Features of Git:

Distributed architecture

Fast and lightweight

Branching and merging

Full history tracking

Offline work support

🔹 What is GitHub?

GitHub is a cloud-based platform that hosts Git repositories and enables collaboration, code review, and CI/CD integrations.

Why GitHub is important for DevOps:

Centralized code hosting

Integration with CI/CD tools like Jenkins

Issue tracking and pull requests

Webhooks for automation

🔹 Git Architecture

Working Directory – Where you edit files

Staging Area – Files prepared for commit

Local Repository – Stored commits

Remote Repository – GitHub repository

🔹 Git Commands Practiced
🔧 Initial Setup
git --version
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list

📁 Repository Setup
git init                 # Initialize repository
git status               # Check status
git add file.txt         # Add file to staging
git add .                # Add all files
git commit -m "message"  # Commit changes

🔗 GitHub Integration
git branch -M main
git remote add origin https://github.com/username/repo-name.git
git remote -v
git push -u origin main

🔄 Updating Code
git pull origin main     # Fetch and merge changes
git log                  # View commit history

🔹 Git Workflow Used

Modify files

Stage changes (git add)

Commit changes (git commit)

Push to GitHub (git push)

Verify changes on GitHub

🔹 Hands-On Tasks Completed

Installed Git on local system and EC2

Configured Git username and email

Created a GitHub repository

Connected local repo to GitHub

Pushed code to remote repository

Verified commits on GitHub

🔹 Common Git Errors & Fixes

❌ Password authentication failed
✅ Use GitHub Personal Access Token (PAT)

❌ Branch mismatch
✅ Rename branch to main

❌ Remote already exists
✅ Check using git remote -v

✅ Key Learnings

Importance of version control in DevOps

Difference between Git and GitHub

Git command workflow

How GitHub integrates with CI/CD

Real-world collaboration practices

🎯 Outcome

By the end of Day 2, I was confident in using Git and GitHub to manage source code and collaborate efficiently—laying a strong foundation for CI/CD pipelines.
