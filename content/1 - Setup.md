# Setup

We will first need an installation of Python. Typically, we can download an installation of Python via its main [website](https://www.python.org/).

## Install by Operating System

### Windows

1. Download Python from the main [website](https://www.python.org/). Use the appropriate installer (usually `x64`) for 64-bit.
2. Make sure to select the option to setup Python in the environment variable `PATH`.
3. Run the following in a command prompt to verify:

```
python --version
```

### Mac OS X (via `Homebrew`)

1. Install `Homebrew` [https://brew.sh/](https://brew.sh/):

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Install Python via Homebrew:

```bash
brew install python
```

3. Verify the installation:

```bash
python --version
```

### Mac OS X (via [https://www.python.org/downloads/macos/](https://www.python.org/downloads/macos/))

1. Download the latest Python from the [website](https://www.python.org/downloads/macos/)

2. Open the `.pkg` file and follow instructions for installation.

3. Verify the installation (notice that it uses `python3` and not `python`:

```bash
python3 --version
```

### Linux

Linux distributions usually have python installed. Verify first that you have Python installed or refer to your distribution's official repositories.

```bash
python3 --version
```

or

```bash
python --version
```

## Python Environment Setup

In practice, we use a Python environment per project. Given a project name `project`, we first have to establish a virtual environment using the `venv` module available in Python 3. The succeeding steps will now be executed with your project's root directory.

### Creating an Environment

1. Creating an environment involves invoking `venv` to create a folder representing the Python environment which in itself includes the `python` executable. To create an environment:

```bash
python -m venv env
```

2. We then activate the environment by running a script found within the directory `env`:

#### Windows (CMD)

```
.\env\Scripts\Activate.bat
```

#### Windows (Powershell)

```
.\env\Scripts\Activate.ps1
```

#### Linux / Mac OS X

```bash
source env/bin/activate
```

This will create a prefix `(env)` in your command prompt to indicate that you are using the current environment.

### Installing Libraries

Installing libraries / packages / dependencies in Python involves the `pip` command. Make sure you are in your project's environment before running the `pip install` command in order to keep all dependencies within the environment. To verify that `pip` is callable:

```bash
pip --version
```

The syntax for installaing a package is as follows:

```bash
pip install [package-name]
```

You may also install multiple packages at a time:

```bash
pip install [package-1] [package-2] [package-3]
```

#### Example Set of Packages for Data Science

```bash
pip install pandas jupyter numpy scikit-learn
```

## Setting Up Jupyter Notebook

[Jupyter Notebook](https://jupyter.org/) is a convenient way to prototype your Python code and test things out via a web interface. This is done by first running a Jupyter server and accessing it via a browser. Make sure you have jupyter installed by running the following:

```bash
pip install jupyter
```

To start your Jupyter Notebook server, run the following:

```bash
jupyeter notebook .
```

This will start an instance of the server on port `8000` by default. You can then access it by visiting `http://localhost:8000` from your browser.
