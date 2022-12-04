# replace-string-in-file
Replace string in file, works with ubuntu, windows, macos

## Usage

The workflow, usually declared in `.github/workflows/javadoc-publish.yml`, looks like:
```YAML
name: Replace string in file

on:
  push:
    branches:
      - master
      - main

jobs:
  publish:
    runs-on: ubuntu-latest
    steps:
      - name: Replace string in file
        uses: MathieuSoysal/replace-string-file@v1.0.0
        with:
          file: tests/test-file.txt
          old-string: WHAT
          new-string: World

```