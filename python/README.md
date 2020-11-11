# CloudDefense Python Action

A [GitHub Action](https://github.com/features/actions) for using [CloudDefense](https://clouddefense.ai)

You can use the Action as follows:

```yaml
name: Example workflow for Python using CloudDefense 
on: push
jobs:
  security:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: Run CloudDefense to check for vulnerabilities
      uses: cdefense/actions/python@master
      with:
        project-name: <Name of the project>
        api-key: <Your API-KEY>
```

The CloudDefense Python Action has properties which are passed to the underlying image. These are
passed to the action using `with`.

| Property | Default | Description |
| --- | --- | --- |
| project-name |   | Name if the project |
| api-key |   | API-Key to send the results to CloudDefense |

