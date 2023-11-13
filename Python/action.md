# Your Action title here

## Others infos

<!-- start branding -->
<!-- end branding -->
<!-- start title -->

# GitHub Action: slack notification

<!-- end title -->
<!-- start badges -->

## <!-- end badges -->

</div>
<!-- start description -->
Slack notification to your channel or person if you have his slack ID

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: UlysseCarpentier/GHActions-Git-Brother@main
  with:
    # Slack username to send to
    # Default: test_bot
    slack_username: ""

    # The message to send, formatted etc...
    # Default: README.md
    slack_message: ""
```

<!-- end usage -->
<!-- start inputs -->

| **Input**                       | **Description**                       | **Default**            | **Required** |
| ------------------------------- | ------------------------------------- | ---------------------- | ------------ |
| **<code>slack_username</code>** | Slack username to send to             | <code>test_bot</code>  | **true**     |
| **<code>slack_message</code>**  | The message to send, formatted etc... | <code>README.md</code> | **true**     |

<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start [.github/ghadocs/examples/] -->
<!-- end [.github/ghadocs/examples/] -->
