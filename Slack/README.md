# Slack notifications

## You have multiple options, depending on what you need.
### Your need :
#### Number of jobs
- If you have multiple jobs, and you don't want to wait for the end of all the jobs to be finished to notify, 
use the 1. Simple Slack notification 
- If you have multiple jobs and need to notify only at the end of all the executions, use the 2. Advanced Slack Notification
  - You can personalize Slack notification title and/or job/steps status
  - You can also notify the person who launched the workflow
  
#### Notification with personal ping

To get useful and relevant Slack notifications from the Slack notification action, we would need the slack member ID.
To get this ID, the easiest but requires actions from EVERY DEV :

**Everybody puts their Slack ID in their GitHub Bio**

Once set, to get this ID, you can use this action [Get Slack ID]() as an example. Only take the job "Get Slack ID".

### Get started

1. Slack notifications setup :
    - Getting a Webhook URL
        - Go to https://api.slack.com/apps and click Create New App.
        - Give your app a name and choose your Development Workspace from the dropdown.
        - Once you have created an app, you need to turn on the Incoming Webhook feature and create a new webhook URL.
        - Create a new webhook by clicking Add New Webhook to Workspace and choose the channel you want the notifications to be posted in.
        - Copy the webhook link
    - Add the webhook link to the GitHub Actions secrets with the name - ACTION_MONITORING_SLACK
2. Slack ID setup :
    - Get your Slack ID by clicking on your picture/profile, click the "...", click on "copy member ID"
    - Set your GitHub bio to your Slack ID, click on your GH profile, your profile, edit profile, put your Slack ID in the bio, and save

### 1. Simple Slack Notification

Just use ravsamhq/notify-slack-action@v2

Ref: [notify-slack-action](https://github.com/ravsamhq/notify-slack-action)

To notify the person who launched the workflow, you can use this action as an example [Slack Notification Simple]()

### 2. Advanced Slack notification

You can use the overwritten version of the Slack notification action, which will allow you to have a more advanced notification.
This is used to notify at the end of all the jobs, not after each job.

You can use this action [Slack Notification Auto]() as an example.
This workflow will automatically notify at the end of all the jobs, with the status of all the jobs merged and present in the title.

It is also possible to personalize the title and the status of the jobs.
It is also able to retrieve the Slack ID of the person who launched the workflow, and ping him in the notification.




Refs:
https://www.ravsam.in/blog/send-slack-notification-when-github-actions-fails/




