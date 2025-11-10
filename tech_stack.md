# Technological stack

This document outlines the main technologies we use across our projects - along with the reasoning behind our choices.

## Python

All modern AI-related projects are implemented in Python. It's powerful and easy to write language with countless packages for machine learning, data analysis, and automation.

We usually use python version 3.11, as it provides the best compatibility with the packages we commonly use. This version is not mandatory - other versions may be used if required by the project.

## Python Packaging

We primarily use `pip` for managing Python packages and virtual environments, as it tends to cause fewer compatibility issues. `Conda` is used exclusively for computations on HPC systems, where its optimized environments and performance benefits are particularly valuable.

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
