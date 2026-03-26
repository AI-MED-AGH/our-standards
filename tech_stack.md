# Technological stack

This document outlines the main technologies we use across our projects - along with the reasoning behind our choices.

## Python

Many modern AI-related projects are implemented in [Python](https://www.python.org/). It's powerful and easy to write language with countless packages for machine learning, data analysis, and automation.

We basically use python version `3.11`, as it provides the best compatibility with the packages we commonly use. This version is not mandatory - other versions may be used if required by the project.

## Python Virtual Environments & Packaging

We primarily use [`uv`](https://docs.astral.sh/uv/) for managing local Python packages and virtual environments, as it tends to cause fewer compatibility issues. Thanks to `uv.lock` we are able to reproduce environment with exactly same version of environment between users.

[`Pip`](https://pip.pypa.io/en/stable/) is used for managing computations environment  on HPC systems, where prepared modules with its optimized environments and performance benefits are particularly valuable.
## Python packages

- **numpy** - For CPU-based matrix operations.
- **PyTorch** - For GPU-based tensor operations.
- **Pandas** - For data importing and manipulations.
- **matplotlib** - for plotting
- **scikit-learn** - For Machine Learning and accuracy measurement
- **pydantic** - for validating JSONs, data structures (provides solid validation framework) - very useful for bigger projects
- **python-dotenv** - for importing `.env` file with secret/local parameters, required for project, but such we don't want to push to git.

## Configuration files and other

- **JSON** - for settings/configuration files.
- **.env** - for secret/local parameters, required to run a project, but such we don't want to push to git.
- **csv** - for data spreadsheets. Although, it may vary depending on the project. Good for model input/output.

## Github

For projects organization. We use issues and pull requests (PRs) for better in-project communication.

## React.js

For web-development (i.e. our website).
