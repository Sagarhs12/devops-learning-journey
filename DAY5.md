🚀 Day 5 – GitHub Webhooks & Automated Jenkins Builds
📌 Objective

The objective of Day 5 was to automate Jenkins builds using GitHub Webhooks, so that every code push to GitHub automatically triggers a Jenkins build without manual intervention.

🔹 What is a GitHub Webhook?

A GitHub Webhook is a mechanism that allows GitHub to send real-time HTTP notifications to another service (Jenkins) whenever an event occurs, such as:

Code push

Pull request

Merge

This enables event-driven CI automation.

🔹 Why Use Webhooks in CI/CD?

Eliminates manual build triggers

Ensures instant feedback on code changes

Enables real-time Continuous Integration

Improves development speed and reliability

🔹 Jenkins & GitHub Integration Overview

Flow:

GitHub Push → Webhook → Jenkins → Build Triggered Automatically

🔹 Jenkins Job Configuration (CI Job)
Job Name:
devops-learning-journey-ci

SCM Configuration:

Source Code Management: Git

Repository URL:

https://github.com/Sagarhs12/devops-learning-journey.git


Branch: main

🔹 Enable GitHub Webhook Trigger in Jenkins
Steps:

Open Jenkins Job

Click Configure

Go to Build Triggers

Enable:

GitHub hook trigger for GITScm polling


Save configuration

🔹 GitHub Webhook Configuration
Steps in GitHub:

Open Repository → Settings

Click Webhooks

Click Add Webhook

Webhook Details:

Payload URL:

http://<EC2-PUBLIC-IP>:8080/github-webhook/


Content type: application/json

Events: Just the push event

Active: ✅ Enabled

🔹 Webhook Testing & Verification
GitHub Side:

Webhook delivery showed HTTP 200 OK

Push and ping events successfully delivered

Jenkins Side:

Build triggered automatically

Console output confirmed:

Started by GitHub push by Sagarhs12

🔹 Hands-On Test (Real Automation)
Command Executed:
echo "Day 5 webhook test" >> DAY5.md
git add DAY5.md
git commit -m "Day 5: webhook test"
git push

Result:

GitHub push event sent

Jenkins job triggered automatically

Build completed successfully

🔹 Jenkins Build Evidence

Build triggered without clicking Build Now

Console Output confirmed webhook trigger

Status: ✅ SUCCESS

🔹 Issues Faced & Solutions
❌ Jenkins Node Offline (Earlier)

Cause: Low /tmp disk space

Solution: Configured custom Jenkins temp directory

Jenkins restored successfully

❌ Webhook URL Error (Initial)

Cause: Jenkins service not fully ready

Solution: Restarted Jenkins and verified endpoint

✅ Key Learnings

GitHub Webhooks configuration

Jenkins webhook endpoint usage

Automated CI triggers

Event-driven CI/CD concepts

Real-world Jenkins + GitHub integration

🎯 Outcome

By the end of Day 5:

Jenkins builds were fully automated

GitHub push events triggered Jenkins jobs

Manual build triggering eliminated

CI pipeline became real-time and reliable
