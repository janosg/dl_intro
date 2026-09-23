# Installation

This page describes how to set up a Python environment with all packages we use in the
course and how to run notebooks in it. Please read it before approaching us with
questions.

We use [uv](https://docs.astral.sh/uv/) to manage Python versions, virtual environments
and packages. You do not need conda, pip or a separate Python installation. The
environment is defined by two files: `pyproject.toml` lists the packages, `uv.lock` pins
their exact versions. Both files are the same for macOS, Linux and Windows, so everyone
in the course works in an identical environment.

**The short version** if you know your way around uv: clone
[dl_intro](https://github.com/janosg/dl_intro), run `uv sync` inside it and start
notebooks with `uv run jupyter lab`.

## Install uv

::::{tab-set}

:::{tab-item} macOS and Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```
:::

:::{tab-item} Windows
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```
:::

::::

Restart your terminal afterwards and check that `uv --version` prints a version number.
The [uv installation guide](https://docs.astral.sh/uv/getting-started/installation/)
lists alternatives such as Homebrew, winget or pipx.

You only need to do this once for the entire course.

## Get the course environment

The environment files live in the repository behind this web page. The easiest way to
get them is to clone the repository. You then also have all exercise notebooks on your
computer.

```bash
git clone https://github.com/janosg/dl_intro.git
cd dl_intro
```

If you do not want to clone the repository, download
[pyproject.toml](https://raw.githubusercontent.com/janosg/dl_intro/main/pyproject.toml)
and [uv.lock](https://raw.githubusercontent.com/janosg/dl_intro/main/uv.lock) into an
empty folder of your choice and open a terminal in that folder.

## Create the environment

In the folder that contains the two files, run

```bash
uv sync
```

This downloads a suitable Python version if necessary, creates a virtual environment in
the hidden folder `.venv` and installs all packages in exactly the versions from
`uv.lock`. It downloads roughly 1-2 GB (pytorch is large), so do this once at home and
not in the lecture. On Linux and Windows a CPU-only version of pytorch is installed.

If we update the environment during the course, you pull the new files (or download
them again) and run `uv sync` again. Only the changes are installed.

## Run notebooks

In the same folder, run

```bash
uv run jupyter lab
```

`uv run` executes a command inside the environment. You never have to activate anything.
Jupyter opens in your browser and lets you open notebooks or create new ones. Notebooks
you download from this web page should be saved inside the `dl_intro` folder or a
subfolder of it. The terminal has to stay open while you work.

Some alternatives:

- If you use [VS Code](https://code.visualstudio.com/) with the Jupyter extension,
  open the folder and select the Python interpreter from `.venv` as the kernel.
- To run a script, use `uv run python my_script.py`.
- If you prefer an activated environment, run `source .venv/bin/activate` (macOS and
  Linux) or `.venv\Scripts\activate` (Windows). Afterwards, `jupyter lab` and `python`
  work without the `uv run` prefix.

## Add packages

To add a package to the environment, run `uv add some-package` in the folder. This
updates `pyproject.toml` and `uv.lock` and installs the package. For your final
project you create your own environment the same way: `uv init` in the project folder,
then `uv add` for each package you need. See the
[uv documentation](https://docs.astral.sh/uv/guides/projects/) for details.

## Google Colab

[Google Colab](https://colab.research.google.com/) runs notebooks in the cloud and
provides free GPUs. Using it is optional. We use it in lecture 7, where fine-tuning a
model on a CPU would take too long. Log into your Google account, upload a notebook via
`File -> Upload notebook` and select a GPU under `Runtime -> Change runtime type`.

Most packages we need are pre-installed on Colab, but the huggingface libraries are
not. Add the following cell at the top of every notebook you run on Colab:

```ipython
import os

IS_ON_COLAB = bool(os.getenv("COLAB_RELEASE_TAG"))

if IS_ON_COLAB:
    !pip install transformers tokenizers datasets sentencepiece huggingface_hub accelerate
```

The condition makes the cell harmless when you run the notebook locally.
