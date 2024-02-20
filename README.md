# Replace string in file

[![Test Actions on Ubunut, Macos and Windows](https://github.com/MathieuSoysal/replace-string-in-file/actions/workflows/test-actions.yml/badge.svg)](https://github.com/MathieuSoysal/replace-string-in-file/actions/workflows/test-actions.yml)

Replace string in file, works with *Ubuntu*, *Windows*, *Macos*.

## Usage

The workflow, usually declared in `.github/workflows/replace-string-in-file.yml`, looks like:
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
        uses: MathieuSoysal/replace-string-in-file@v1.1.0
        with:
          file: tests/test-file.txt
          old-string: WHAT
          new-string: World
```

### With regex

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
        uses: MathieuSoysal/replace-string-in-file@v1.1.0
        with:
          file: tests/test-file.txt
          old-string: 'W.*T$'
          new-string: World
```

## Contribute

### Setup development environment

- Add [Nektos/act](https://www.github.com/nektos/act) to test the workflow locally

-OR-

- Use the devcontainer inside this project with [GitHub Codespaces](https://docs.github.com/fr/codespaces/getting-started/quickstart) or any other IDE that supports devcontainers.

### Test

- Run `act` command to test the workflow locally

## License
The Dockerfile and associated scripts and documentation in this project are released under the [Apache 2.0 License](https://github.com/MathieuSoysal/Javadoc-publisher.yml/blob/main/LICENSE).
