# setup-yq-action

This GitHub Action installs the `yq` CLI tool, a lightweight and portable command-line YAML processor.

## Usage

To use this action in your GitHub workflows, add a step in your workflow YAML file as shown below:

```yaml
name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3
      
      - name: Install yq
        uses: Makepad-fr/setup-yq-action@main
        with:
          version: '4.6.0'

      # Add more steps here that require yq
