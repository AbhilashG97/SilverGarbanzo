# Using Environment variables and Secrets

## Introduction to Environment variables

Environment variables can be defined at the workflow level or the job level. The `env` context can be used to define environment variables. 

Here is an example -

```yaml
name: Deployment
on:
  push:
    branches:
      - main
      - dev
env:
  key1: value1
  key2: value2

jobs:
  newJob:
    env:
      key1: value1
      key2: value2
    runs-on: ubuntu-latest
    steps:
      - ...
```
:warning: Job level envs cannot be visible outside of the job in which the envs are defined.

> GitHub Actions also provides a couple of default environment variables that are set automatically: https://docs.github.com/en/actions/learn-github-actions/environment-variables#default-environment-variables

> These environment variable can, for example, give you quick access to the repository to which the workflow belongs, the name of the event that triggered the workflow and many other things.

## Environment variables vs Secrets

<p align="center"><img src ="images/envs-vs-secrets.png" /></p>

Secrets can be stored at organisation level or repository level

Repository secrets can be referred in a workflow by using the `secrets` context.
