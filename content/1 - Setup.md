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

In practice, we use a Python environment per project. Given a project name `project`, we first have to establish a virtual environment using the `venv` module available in Python 3. The succeeding steps will now install

### Creating an Environment

Creating an environment involves invoking `venv` as a module (more on this later).
