# GitHub Actions Workflow Testing
[![debug](https://github.com/devops-testbed/actions-test/actions/workflows/latest.yml/badge.svg)](https://github.com/devops-testbed/actions-test/actions/workflows/latest.yml)


This repository is set up to test GitHub Actions workflows using a Python script.

## Python Script

The Python script [test.py](test.py) generates messages of varying lengths and prints them along with the current timestamp. The lengths of the messages are defined in the `lens` list.

```python
lens = [10, 100, 6*1024, 8*1024, 100*1024]
for i in lens:
    print(f'{datetime.datetime.now()} - Message length: {i} - {"a"*i}')
for i in reversed(lens):
    print(f'{datetime.datetime.now()} - Message length: {i} - {"a"*i}')

```
Workflows
There are two workflows defined in this repository:

Test Workflow: This workflow runs on an Alpine container and executes the Python script.

Debug Workflow: This workflow runs on the latest Ubuntu and executes the Python script.

You can view the execution runs of these workflows in the Actions tab of the GitHub repository.

Please note that the links to the execution runs will only work if the workflows have been run at least once.