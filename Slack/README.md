# Slack notifications

## You have multiple options, depending on what you need is.
### Your need
#### Number of jobs
- If you have multiple jobs, and you don't want to wait for the end of all the jobs to be finished to notify, 
use the Simple Slack notification 
- If you have multiple jobs and need to notify only at the end of all the executions, use the Advanced Slack Notification
  - If you want personalized Slack notification title and/or job/steps status, check the 2.2 Advanced Slack Notification
  - Otherwise, check the 2.1 Advanced Slack Notification
  
#### Notification with personnal ping

To get useful and relevant Slack notifications from the Slack notification action, we would need the slack member ID.
To get this ID, the easiest but requires actions from EVERY DEV :

**Everybody puts their Slack ID in their GitHub Bio**

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

### 1. Simple Slack Notification

### 2. Advanced Slack notification
#### 2.1 Auto advanced Slack Notification

#### 2.2 Personalized advanced Slack Notification



Refs:
https://www.ravsam.in/blog/send-slack-notification-when-github-actions-fails/




