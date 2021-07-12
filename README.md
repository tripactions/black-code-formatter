# Black Code Formatter GitHub Action

A GitHub action that runs [black code formatter](https://github.com/ambv/black) for Python.

## Example action

```
name: Build

on: [push]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v1
      with:
        lfs: false
    - name: Black Code Formatter
      uses: tripactions/black-code-formatter@21.4b1
      with:
        args: ". --check -l 100 -t py37"

```

For a full list of possible `args` checkout the [black docs](https://github.com/ambv/black#command-line-options).

Based on the original [lgeiger/black-action](https://github.com/lgeiger/black-action).