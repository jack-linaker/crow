# CROW1

Here you will find more focused documentation for the tkinter-based desktop
variant of CROW, detailing installation, configuration, and usage instructions
specific to this application. You will also find some useful guidance and setup
documents in the `docs` folder.

- [Overview](#overview)
  - [Key Differences From Flask Version](#key-differences-from-flask-version)
- [User Guide](#user-guide)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Configuration](#configuration)
  - [Running CROW1](#running-crow1)
- [Utils](#utils)
  - [Cluster-to-pairwise](#cluster-to-pairwise)
- [Help](#help)

## Overview

CROW1 is the original desktop solution for clerical review of linked candidate
pairs (or clusters). Built with Python and tkinter, it offers a lightweight GUI
for:

- Loading pre-linked CSV datasets via file selection within the app.
- Side-by-side record comparison.
- Simple review buttons: "Match" and "Non-match".
- Automatically exports match/non-match decisions to CSV for later analysis.

### Key Differences From Flask Version

- **Desktop GUI**: Runs as a standalone `.py` script with no web server.
- **Local File I/O**: Uses native file selection dialogs; with no HDFS/S3
  integration.
- **Simplified styling**: Basic tkinter widgets, no HTML/CSS.

## User Guide

The following instructions include the use of the `python` command. This can
only be used if you have the Python interpreter (`python.exe`) added to your
[PATH environment variable][path], or if you are in a [Python virtual
environment][venv]. You can find more information on this topic in the [ASAP
Coding Getting Started Guide Python page][asap-python] (internal access only).
If Python has not been added to your PATH, you should replace the `python`
command with the path to your Python interpreter. That is, rather than running
the command:

```sh
python your_script.py
```

you would instead run:

```sh
c:\path\to\your\python\interpreter\python.exe your_script.py
```

### Prerequisites

Before installing CROW1, ensure your machine has:

- Python 3.9+
- tkinter (usual comes bundled with Python)

### Installation

1. **Clone the repository**:

   ```sh
   git clone https://github.com/Data-Linkage/Clerical_Resolution_Online_Widget.git
   ```

2. **Navigate into the CROW1 directory**:

   ```sh
   cd Clerical_Resolution_Online_Widget/version1_tkinter
   ```

3. **Create a virtual environment**:

   ```sh
   python -m venv .venv
   ```

   and activate it:

   ```sh
   .venv/Scripts/activate
   ```

4. **Install dependencies**

   First, ensure `pip` (package manager) is up-to-date:

   ```sh
   python -m pip install --upgrade pip
   ```

   then install the required packages listed in `requirements.txt`:

   ```sh
   pip install -r requirements.txt
   ```

### Configuration

#### Data Source Setup

CROW1 expects input data in CSV format. You can place one or more CSV files in a
local folder of your choice.

#### Configuration files

Edit the `Config_clusters.ini` or `Config_pairwise.ini` files (depending on the
format of your data) to set various options based your data and review
preferences. Instructions are embedded within each configuration file.

> [!WARNING]
>
> Make sure you do not change the name of the configuration file. If you do, the
> script will not be able to read it.

Save your changes before running the application.

### Running CROW1

With your virtual environment activated, dependencies installed, and
configuration file edited, launch CROW1:

> [!IMPORTANT]
>
> Make sure the configuration file is in the same directory as the script.
> Otherwise the script will not be able to read it.

```sh
python CROW_clusters.py
```

or

```sh
python CROW_pairwise.py
```

- A window will open, prompting you to choose a file to clerically review.
  Clicking the button will open a file-selection dialog where you should choose
  a CSV file.
- The file-selection prompt will close and the main window will open, displaying
  pairs (or clusters) in a table-like format.
- Use the "Match" and "Non-match" buttons to record your decisions.
- Decisions are appended as you record decisions, but only save either by
  clicking the "Save and close" button or according to the auto-save interval
  specified in the configuration file.

#### Integrated Development Environment (IDE)

CROW1 can also be launched in an IDE such as Spyder, Visual Studio (VS) Code, or
PyCharm.

1. Open the script in your chosen IDE.
2. Click the run button (or run it from an integrated terminal within the IDE if
   available) and CROW1 should start (VS Code may require extra setup such as
   installing the Python extension).

## Utils

The `utils` folder contains some scripts that may be useful when working with
CROW1. Each script will contain a module-level docstring at the top of the file
that will contain usage instructions.

### Cluster-to-pairwise

The `cluster_to_pairwise.py` script will convert data that works with the
cluster version of CROW1 into a format that works with the pairwise version. The
script will group the data by cluster and data source, and keep only the
unique information from each data source per cluster.

## Help

If you have additional questions or issues, please raise an issue or contact:
<linkage.hub@ons.gov.uk>

[asap-python]: https://gitlab-app-l-01/ASAP/coding-getting-started-guide/-/wikis/python#python-on-the-command-line
[path]: https://en.wikipedia.org/wiki/PATH_(variable)
[venv]: https://docs.python.org/3/library/venv.html
