# Your Action title here

## Others infos

<!-- start branding -->
<!-- end branding -->
<!-- start title -->

# GitHub Action: reusable-ci_python_pipenv_pytest

<!-- end title -->
<!-- start badges -->

## <!-- end badges -->

</div>
<!-- start description -->
Slack notification to your channel or person if you have his slack ID

CI test run for Python
Expects project

- to use pytest as the test engine
- to use Pipenv for managing python virtual environment

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: UlysseCarpentier/GHActions-Git-Brother@main
  with:
    # Slack username to send to
    # Path within the git repository on the python code
    # Expects to find Pipfile.lock in that path
    code-path: ""

    # Python version to
    python-version: ""

    runner: ""
```

<!-- end usage -->
<!-- start inputs -->

| **Input**                       | **Description**                                                                                                                 | **Default** | **Required** |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ----------- | ------------ |
| **<code>code-path</code>**      | Slack username to send to<br />Path within the git repository on the python code<br />Expects to find Pipfile.lock in that path |             | **true**     |
| **<code>python-version</code>** | Python version to                                                                                                               |             | **true**     |
| **<code>runner</code>**         |                                                                                                                                 |             | **true**     |

<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start [.github/ghadocs/examples/] -->
<!-- end [.github/ghadocs/examples/] -->
