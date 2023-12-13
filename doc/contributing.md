# How to participate in GHA Shared
## How to join the team

We are glad to count on new members to review and participate in this repository!!!

Ask to become a team member in the Slack channel #gha_shared!

We can provide some useful trainings/time to spend with you to best help you take part of the team!
## How to make a reusable workflow
### First off
- You can find an example of a rightfully made reusable workflow here : @ULYSSE CHANGE THIS
- The auto documentation will create a .md from only your reusable workflow "R_".
- Once your workflow is merged into the repository, it will create the .md file with the same name as your action.
  You will then be able to update this documentation if it's missing any important information.
  For example if you have 2 examples for your reusable workflow, you will be able to change the documentation to add context to those, if the description inside the workflow is not enough.

**Make your changes outside the brackets in the file, otherwise it will be overwritten**


### PR Convention

Please use the PR Template to create your PR.


### Reusable Workflow syntax

The file name pattern should be :
- "R_" to mark them as reusable
- "Directory_SubDir_Description"

**Everything with * is mandatory**
- Name* : `name:` , it should be close to the directory structure
- Description* : `description: |+`
- Author* : `author: [your name] [your email]`
- Inputs
  - Name*
    - Description* : `description: |`
    - Required* : `required: true or false`
    - Default : `default:`
    - Type* : `type: string or bool or number`
- Outputs
  - Name*
    - Description* : `description: |`

### Use example of reusable Workflow syntax

The file name pattern should be :
- "V_" to mark them as example
- "Directory_SubDir_Description"

**Everything with  * is mandatory**
- Name* : `name:` , Same as the reusable name beginning with Example and more description if needed
- Author* : `author:[your name] [your email]`
- Inputs
  - Name
    - Description : `description: |+`
    - Required : `required: true or false`
    - Default : `default:`
- Outputs
  - Name
    - Description : `description: |`

### Runners

⚠️ Use only provided private runners in your workflow using `runs-on` parameter [Runners](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idruns-on). Currently, you can use :



- `gha-private-runners`
- `gha-private-runners-java-11`

### Steps to provide a reusable workflow
- Reusable workflow file with emoji "R_" and syntax.
- Example of use of that workflow with emoji "V_" and syntax.
- Update the sync.yml in .GitHub to sync your reusable workflow to the .GitHub/workflow directory.
- Optional: Update the .md file with more data if needed.


### Update/rename workflow
If you modify the top description of your reusable workflow, the changes won't be applied to the list of actions in the README.md
- You need to update the description in the action list in README.md
- You also need to update the sync.yml file to reflect the new name

### Delete workflow
If you delete your reusable workflow, the changes won't be applied to the list of actions in the README.md
- You need to update the description in the action list in README.md
- You also need to update the sync.yml file to reflect remove the corresponding line
