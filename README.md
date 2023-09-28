# GHActions-Git-Brother
### GH Actions to check the branches
1. Slack notifications setup :
    - Getting a Webhook URL
        - Go to https://api.slack.com/apps and click Create New App.
        - Give your app a name and choose your Development Workspace from the dropdown.
        - Once you have created an app, you need to turn on the Incoming Webhook feature and create a new webhook URL.
        - Create a new webhook by clicking Add New Webhook to Workspace and choose the channel you want the notifications to be posted in.
        - Copy the webhook link
    - Add the webhook link to the Github Actions secrets with the name - ACTION_MONITORING_SLACK




To get useful and relevant slack notifications from the Git Brother, we would need the slack member ID.
To get this ID, we have couple choices:
- Easiest but requires actions from EVERY DEV :
  - In slack,write your GITHUB mail address
  - If you have a Github account different from your EP email address, you will have to create an account with the EP email address.
- Pain : 
  - Create a file with everybody 




Refs:
https://www.ravsam.in/blog/send-slack-notification-when-github-actions-fails/
