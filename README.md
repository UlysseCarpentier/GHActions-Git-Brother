<div align="center" width="100%">
<!-- start branding -->
<!-- end branding -->
<!-- start title -->
# GitHub Action: GitHub Action's Readme Generator
<!-- end title -->
<!-- start badges -->
<!-- end badges -->

</div>
<!-- start description -->
📓 Keep your action's README.md up to date with the `title` and `description` from the `[action.yml](./action.yml)` file, while also automatically generating sections for the inputs, outputs, and a usage example for the action.

Additionally the Action's usage example is updated to match the Action's current release.

This is both a CLI tool and GitHub Action that will read the details from a GitHub Action's `[action.yml](./action.yml)` file. Configuration can be provided through a `.ghadocs.json` file stored in the root directory of the Action's repository, via the command line when using the CLI, or through the `with:` section of this Action.

**_📝 This tool uses markdown comments as delimiting tokens within the README.md file to determine where to place the generated content._**

**_🔗 You can find an example README template with all fields filled-in in the [`README.example.md`](README.example.md) file._**

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: UlysseCarpentier/GHActions-Git-Brother@main
  with:
    # The absolute or relative path to the `action.yml` file to read in from.
    # Default: action.yml
    action: ""

    # The absolute or relative path to the markdown output file that contains the
    # formatting tokens within it.
    # Default: README.md
    readme: ""

    # The GitHub Action repository owner.
    # example `bitflight-devops` or `your-gh-username`
    owner: ""

    # The GitHub Action repository name.
    # example - `github-action-readme-generator`
    repo: ""

    # Save the provided values in a `.ghadocs.json` file.
    # This will update any existing `.ghadocs.json` file that is in place.
    save: ""

    # Use `prettier` to pretty print the new README.md file
    pretty: ""

    # Enable the update of the usage version to match the latest version in the
    # `package.json` file
    versioning_enabled: ""

    # Set a specific version to display in the README.md
    version_override: ""

    # Prefix the version with this value, if it isn't already prefixed
    # Default: v
    version_prefix: ""

    # If versioning is disabled show this branch instead
    # Default: main
    versioning_default_branch: ""

    # Add a prefix to the README title.
    # The title template looks like this:
    # # {brand}{prefix}{title}
    # Default: GitHub Action:
    title_prefix: ""

    # Include additional badge showing latest tag
    # Default: true
    include_github_version_badge: ""

    # Create the branding svg image from the branding object in `action.yml`
    # then save it to this path.
    # Then update the `README.md` file to source the branding image from this path.
    # You can use a section template like this:
    # `\<!-- start branding --><!-- stop branding -->`
    # or use the action input:
    # `branding_as_title_prefix: true`
    # to prefix the 'title' section with the image.
    # The title template looks like this:
    # # {brand}{prefix}{title}
    # Default: .github/ghadocs/branding.svg
    branding_svg_path: ""

    # Prefix the title in the `\<!-- start title -->` section with the svg branding
    # image
    # The title template looks like this:
    # # {brand}{prefix}{title}
    # Default: true
    branding_as_title_prefix: ""
```

<!-- end usage -->
<!-- start inputs -->

| **Input**                                     | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | **Default**                               | **Required** |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- | ------------ |
| **<code>action</code>**                       | The absolute or relative path to the <code>action.yml</code> file to read in from.                                                                                                                                                                                                                                                                                                                                                                                                                      | <code>action.yml</code>                   | **false**    |
| **<code>readme</code>**                       | The absolute or relative path to the markdown output file that contains the formatting tokens within it.                                                                                                                                                                                                                                                                                                                                                                                                | <code>README.md</code>                    | **false**    |
| **<code>owner</code>**                        | The GitHub Action repository owner.<br />example <code>bitflight-devops</code> or <code>your-gh-username</code>                                                                                                                                                                                                                                                                                                                                                                                         |                                           | **false**    |
| **<code>repo</code>**                         | The GitHub Action repository name.<br />example - <code>github-action-readme-generator</code>                                                                                                                                                                                                                                                                                                                                                                                                           |                                           | **false**    |
| **<code>save</code>**                         | Save the provided values in a <code>.ghadocs.json</code> file.<br />This will update any existing <code>.ghadocs.json</code> file that is in place.                                                                                                                                                                                                                                                                                                                                                     |                                           | **false**    |
| **<code>pretty</code>**                       | Use <code>prettier</code> to pretty print the new README.md file                                                                                                                                                                                                                                                                                                                                                                                                                                        |                                           | **false**    |
| **<code>versioning_enabled</code>**           | Enable the update of the usage version to match the latest version in the <code>package.json</code> file                                                                                                                                                                                                                                                                                                                                                                                                |                                           | **false**    |
| **<code>version_override</code>**             | Set a specific version to display in the README.md                                                                                                                                                                                                                                                                                                                                                                                                                                                      |                                           | **false**    |
| **<code>version_prefix</code>**               | Prefix the version with this value, if it isn't already prefixed                                                                                                                                                                                                                                                                                                                                                                                                                                        | <code>v</code>                            | **false**    |
| **<code>versioning_default_branch</code>**    | If versioning is disabled show this branch instead                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <code>main</code>                         | **false**    |
| **<code>title_prefix</code>**                 | Add a prefix to the README title.<br />The title template looks like this:<br /># {brand}{prefix}{title}                                                                                                                                                                                                                                                                                                                                                                                                | <code>GitHub Action: </code>              | **false**    |
| **<code>include_github_version_badge</code>** | Include additional badge showing latest tag                                                                                                                                                                                                                                                                                                                                                                                                                                                             | <code>true</code>                         | **false**    |
| **<code>branding_svg_path</code>**            | Create the branding svg image from the branding object in `action.yml`<br />then save it to this path.<br />Then update the <code>README.md</code> file to source the branding image from this path.<br />You can use a section template like this:<br />`\<!-- start branding --><!-- stop branding -->`<br />or use the action input:<br />`branding_as_title_prefix: true`<br />to prefix the 'title' section with the image.<br />The title template looks like this:<br /># {brand}{prefix}{title} | <code>.github/ghadocs/branding.svg</code> | **false**    |
| **<code>branding_as_title_prefix</code>**     | Prefix the title in the <code>\<!-- start title --></code> section with the svg branding image<br />The title template looks like this:<br /># {brand}{prefix}{title}                                                                                                                                                                                                                                                                                                                                   | <code>true</code>                         | **false**    |

<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start [.github/ghadocs/examples/] -->
<!-- end [.github/ghadocs/examples/] -->

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
- Followed by 6 digit number and \_
- Ended with a short description

### Check-Commit-Message

Example of the start of a good commit message : GH-123456
**The commit message must start with the issue ID**

- Commit message must start with GH|RM and -
- Followed by 6 digits

Refs:
https://www.ravsam.in/blog/send-slack-notification-when-github-actions-fails/
