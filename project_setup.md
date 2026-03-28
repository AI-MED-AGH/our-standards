# Project setup

Most of our projects are developed in **Python**.  
We recommend using **Python 3.11**, as it provides the best compatibility with the packages we commonly use.  
This version is not mandatory - other versions may be used if required by the project.

## Virtual Environment

To prevent package conflicts, **always create a separate virtual environment** for each project.  
For supercomputing we use **`pip`** for dependency management and `uv` for private workstations.

Every project **must include** a `requirements.txt`/  `pyproject.toml` file listing all required packages.  
The Python version used in the project should also be specified - either in the project’s `README.md` or in a `.python-version` file (read more about `.python-version` file [here](https://pydevtools.com/handbook/explanation/what-is-a-python-version-file/)). Best practice is to use `uv lock` & `uv sync` for better reproducibility.

## First-Time setup instructions

Each project’s `README.md` should include a **“First Time Setup”** section.  
This helps new contributors quickly set up their environment and ensures a consistent installation process.

### Example:

```md
## First time setup

Use python 3.11.

To setup project, run following commands:

python3.11 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## .gitignore

It’s essential to **exclude the virtual environment** from git.
You can do this in one of two ways:

1. Add the virtual environment folder (e.g., `venv/`) to your project’s `.gitignore` file.
2. Or, create a `.gitignore` file inside the virtual environment folder with the following content:
    `*`
> [!CAUTION]
> Remember to add **.env** to .gitignore

### Example structure:
``` (folders structure)
venv/
	.gitignore (with content: "*")
	... (other venv files)
```

Additionally, some IDEs create their own configuration folders.
These should also be ignored. For example, PyCharm creates a `.idea/` folder that is **not** ignored by default - be sure to add it to `.gitignore`!

If the project contains `.env` file it also MUST be excluded from version control!

### Example .gitignore file

Example (can be used as a base when creating new repositories):

```.gitignore
# Python virtual environment
venv/
.venv/

# PyCharm
.idea/

# Project settings
.env
```

## Summary

Each Python project repository should include the following files at the root:

```
.gitignore
requirements.txt / pyproject.toml
README.md (with python version specified)

.python-version (optional)
```
