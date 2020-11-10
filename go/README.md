# CloudDefense Golang Action

A [GitHub Action](https://github.com/features/actions) for using [CloudDefense](https://clouddefense.ai)

You can use the Action as follows:

```yaml
name: Example workflow for Golang using CloudDefense 
on: push
jobs:
  security:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: Run CloudDefense to check for vulnerabilities
      uses: snyk/actions/go@main
      env:
        SNYK_TOKEN: ${{ secrets.SNYK_TOKEN }}
```

The CloudDefense Golang Action has properties which are passed to the underlying image. These are
passed to the action using `with`.

| Property | Default | Description |
| --- | --- | --- |
| project-name |   | Name if the project |
| api-key |   | API-Key to send the results to CloudDefense |

