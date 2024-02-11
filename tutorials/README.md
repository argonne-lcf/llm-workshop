# Large Language Models (LLMs): Tutorial Workshop -- Introduction

[Workshop Agenda](https://anl.app.box.com/file/1421615910690?s=woqtpw0o0tpnb6j9uljjme5wqmxsoz35)  
Argonne National Laboratory  
_February 12th and 13th, 2024_  
**Building 240**, **Room 1501** (in-person)

The workshop material rely on Python and Jupyter Notebooks which are targeted for running on [Google's Colaboratory Platform](https://colab.research.google.com).  

Creating an installation script for Jupyter Notebooks on a Mac involves using a terminal and a package manager like Homebrew, and possibly pip (Python's package installer). The following script assumes you have Homebrew installed on your Mac. If you don't have Homebrew installed, you can install it by following the instructions on the [Homebrew website](https://brew.sh).

This script will:

1. Install Python 3, if not already installed.
2. Use pip to install Jupyter Notebook.

Save the following content into a file with a `.sh` extension, for example, `install_jupyter.sh`. Make sure to give it execute permission using `chmod +x install_jupyter.sh` before running.

```bash
#!/bin/bash

# Install Python 3 using Homebrew
echo "Checking for Python 3 installation..."
if ! command -v python3 &> /dev/null
then
    echo "Python 3 could not be found, installing now..."
    brew install python
    echo "Python 3 installed successfully."
else
    echo "Python 3 is already installed."
fi

# Update pip (Python package installer) to its latest version
echo "Updating pip..."
pip3 install --upgrade pip

# Install Jupyter Notebook
echo "Installing Jupyter Notebook..."
pip3 install notebook

# Verify installation and provide user instructions
if command -v jupyter-notebook &> /dev/null
then
    echo "Jupyter Notebook installed successfully."
    echo "You can run Jupyter Notebook by typing 'jupyter-notebook' in your terminal."
else
    echo "Jupyter Notebook installation failed. Please check the output for errors."
fi
```

To run this script:

1. Open Terminal on your Mac.
2. Navigate to the directory where your script is located using `cd /path/to/directory`.
3. Make the script executable (if you haven't already) with `chmod +x install_jupyter.sh`.
4. Run the script with `./install_jupyter.sh`.

The script checks if Python 3 is installed, installs it if it's not, upgrades pip, installs Jupyter Notebook, and then checks if Jupyter Notebook is installed successfully.

```jupyter-notebook Introduction.ipynb```

Will run the example notebook.

<!--

## Contents

- 📂 [`tutorials/`](https://github.com/argonne-lcf/llm-workshop/tutorials/)
  `├──` [`01-llm-101`](https://github.com/argonne-lcf/llm-workshop/tutorials/01-llm101/)
    `└──` [`06-llm-from-scratch`](https://github.com/argonne-lcf/llm-workshop/tutorials/06-llm-from-scratch/)
    -->
    ~
