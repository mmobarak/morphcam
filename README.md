# Pi Camera Face Morpher

## Basic Pi Setup

After installing the Desktop version of Bookworm:

```bash
sudo apt update
sudo apt full-upgrade
```

```bash
sudo apt install \
    git \
    python3 \
    python3-pip 
```

## Set up Python

### Install Python3

```bash
sudo apt install \
    python3 \
    python3-pip 
```

### Create a Python Virtual Environment

Bookworm is strict about installing pakages in the global Python so we create a venv as our default python. This lets us `pip install` more tools like `Pipenv` to manage the virtual environments for our projects.

```bash
python -m venv --system-site-packages ~/env
```

In your `.profile` add the following to use your private python.

```bash
# set PATH so it includes user's default Python bin if it exists
if [ -d "$HOME/env/bin" ] ; then
    PATH="$HOME/env/bin:$PATH"
fi
```
