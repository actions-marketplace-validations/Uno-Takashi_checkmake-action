# checkmake-action

[![Test](https://github.com/Uno-Takashi/checkmake-action/actions/workflows/run-my-self.yml/badge.svg?branch=main)](https://github.com/Uno-Takashi/checkmake-action/actions/workflows/run-my-self.yml)
[![Code Quality](https://github.com/Uno-Takashi/checkmake-action/actions/workflows/code-quality.yml/badge.svg?branch=main)](https://github.com/Uno-Takashi/checkmake-action/actions/workflows/code-quality.yml)

checkmake-action is a third-party OSS Github Action for easy execution of [checkmake](https://github.com/mrtazz/checkmake).This action uses [cytopia/docker-checkmake](https://github.com/cytopia/docker-checkmake).

- **Rapid Container**
  - The checkmake-action employs a lightweight container based on [Alpile](https://hub.docker.com/r/cytopia/checkmake). In most cases, preparation to begin analysis takes less than 30 seconds in github-hosted runner.
- **Easy-to-use variable specification**
  - Wrapping command line arguments allows for more intuitive execution.
- **Can be embedded in CI**
  - You can Keep beautiful your Makefile every time.

## 🗞️ Introduction

## 🛠️ Why We Built It

## 📚 Usage

The following code is the minimum code to make checkmake-action work. In the following cases, checkmake is run with default settings.

```yaml
name: checkmake action
on:
  push:

jobs:
  checkmake:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: checkmake action
        uses: Uno-Takashi/checkmake-action@main
```

chackemake execution options can be passed as arguments. For example, to specify a file to be analyzed or to activate debug mode, do the following

```yaml
      - name: checkmake action
        uses: Uno-Takashi/checkmake-action@main
        with:
          makefile: "path/to/Makefile"
          debug: true
```

## 📥 Inputs

## 📤 Outputs

## 🛒 How to Get
