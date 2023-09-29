# GHActions-Git-Brother



### Personnal slack notification solutions: 
To get useful and relevant slack notifications from the Git Brother, we would need the slack member ID.
To get this ID, we have couple choices:
- Easiest but requires actions from EVERY DEV (already implemented):
    - Everybody puts their Slack ID in their Github Bio
- Also requires actions from EVERY DEV and must be kept up to date :
    - Create a file where everybody puts their Github ID and Slack ID
    - Keep it up to date, add it to the Onboarding



### Get started
1. Slack notifications setup :
    - Getting a Webhook URL
        - Go to https://api.slack.com/apps and click Create New App.
        - Give your app a name and choose your Development Workspace from the dropdown.
        - Once you have created an app, you need to turn on the Incoming Webhook feature and create a new webhook URL.
        - Create a new webhook by clicking Add New Webhook to Workspace and choose the channel you want the notifications to be posted in.
        - Copy the webhook link
    - Add the webhook link to the Github Actions secrets with the name - ACTION_MONITORING_SLACK
2. Slack ID setup :
   - Get your Slack ID by clicking on your picture/profile, click the "...", click on "copy member ID"
   - Set your Github bio to your Slack ID, click on your GH profile, your profile, edit profile, put your Slack ID in the bio, and save






### Check-Branch-Name
Example of a good named branch : fix/microgrid/GH-123456_petite-description

- Branch name must start with chore|feat|fix|hotfix
- Followed by a directory (can contains numbers)
- Followed by RM|GH and -
- Followed by 6 digit number and _
- Ended with a short description

### Check-Commit-Message
Example of the start of a good commit message : GH-123456
**The commit message must start with the issue ID**

- Commit message must start with GH|RM and -
- Followed by 6 digits 

Refs:
https://www.ravsam.in/blog/send-slack-notification-when-github-actions-fails/
