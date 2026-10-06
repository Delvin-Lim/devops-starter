# DevOps Starter
## About
This project is a simple Python calculator created as part of a DevOps learning exercise.
## Features
The calculator supports:
- Addition
- Subtraction
- Multiplication
- Division
## Learning Points
- Github actions uses YAML files for configuration, YAML files are white-space sensitive and support lists (or sequences) and mappings (key-value pairs) that are dictated based on syntax. Mappings are created use semi-colon suffixed at the end (example:) and essentially are used to group key-value pairs together, this is different from a sequence in that this is unordered. Conversely, sequences do not need to be key-value pairs, and are ordered. This is important for Github Actions because a variety of its syntax varies from sequences to mappings to primitive scalars (e.g. string, number etc.)
- A Github Action workflow YAML file has the following components:
  - Events - dictate what triggers the workflow
  - Jobs - a set of related steps that will all run sequentially, multiple jobs can run in parallel on individual runners not shared with other jobs
  - Steps - a single action, has keywords like *use:* for using reusable actions (can find community ones from marketplace or written by yourself), *run:* for running shell commands and *with:* for providing a mapping of parameters to the action given in *use:*
  - Runner - a machine that provides the environment for the job to run in. Github provides a variety of runners such as for Windows, MacOS and Linux operating systems.

- The action marketplace is useful for finding commonly used actions and looking for documentation regarding what they do and how to use them, Github also has a variety of actions available for common actions such as checking out the code from the repository into the runner.
- When a workflow runs unsuccessfully, do not be hasty to try to rectify anything before actually consulting the error log that it outputs, as often times actions give a detailed output of what went wrong.
- Overall, Github Actions provides a bulit-in CI/CD solution right inside Github that allows for constructing pipelines such as for running tests whenever certain actions are performed in Github. Security can also be built into this step by incorporating utilities that scan for vulnerabilities such as running a SAST utility like SAST by Insomnia (vulnz/vulnerability), which allows for earlier detection of vulnerable code even before a push succeeds, to ensure code quality and minimize tech debt.

## Author
Delvin Lim
