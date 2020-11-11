# CloudDefense GitHub Actions

A set of [GitHub Actions](https://github.com/features/actions) for using [CloudDefense](https://clouddefense.ai) to check for
vulnerabilities in your GitHub projects. A different action is required depending on which language or build tool
you are using. We currently support:

* [Java-Maven](java)
* [Node.js](node)
* [PHP](php)
* [Python](python)
* [DotNet](dotnet)
* [Golang](go)

An example of using one of the Actions, in this case to test a Node.js project:

```yaml
name: Example workflow using CloudDefense
on: push
jobs:
  security:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: Run Cloud Defense to check for vulnerabilities
      uses: cdefense/actions/node@master
      with:
        project-name: <Name of your project>
        api-key: <Your CD API-KEY>
```

See the individual Actions linked above for per-language instructions.
