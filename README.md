# `action-download-file` - **Github Action**

This action download a file from a URL and save it to the target path.

## Input

| Name          | Description |
| ------------- | ----------- |
| `url`         | URL to file |
| `target-path` | Target path |

## Example Usage

```yaml
name: Download a file

on:
  push:
    branches:
      - master
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v2
        - uses: valitydev/action-download-file@v1
          with:
            url: https://raw.githubusercontent.com/valitydev/action-download-file/master/README.md
            target-path: .
```

## TODO

- Add `replace` and `filename` options
