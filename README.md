# CROW (Clerical Resolution Online Widget)

An open-source app designed to support manual ("clerical") review of linked
records in data linkage projects.

- [What is CROW?](#what-is-crow)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running CROW](#running-crow)
- [Documentation](#documentation)
- [Accessibility](#accessibility)
- [Contributing](#contributing)
- [License](#license)
- [Contact and Support](#contact-and-support)
- [Acknowledgments](#acknowledgments)

## What is CROW?

CROW is an app designed to speed up and simplify the clerical review of data
linkage results.

After automated linking produces candidate pairs or cluster,
CROW:

- Reads pre-linked data in CSV or parquet format.
- Presents one record pair (or cluster) at a time.
- Provides simple "Match" and "Non-match" controls, along with other
  functionality to aid the match/non-match decision.

There are currently two versions of the app:

- **CROW1**: A desktop app that utilises tkinter. Available in
  `version1_tkinter`.
- **CROW2**: A web app that utilises Flask. Available in `version2_flask`. CROW2
  currently only runs in Cloudera Data Platform (CDP).

## Key Features

- **Web- and desktop-based**: CROW1 uses tkinter, while CROW2 utilises Flask but
  only runs in Cloudera Data Platform (CDP).
- **HDFS/Hue/S3 integration**: While CROW1 only works locally with CSV files,
  CROW2 loads parquet files directly from S3 buckets within a CDP session.
- **Flexible review modes**: CROW1 comes with two separate scripts for pairwise
  or cluster record comparison. CROW2 has pairwise and cluster comparison
  consolidated into a single app.
- **Bulk operations**: CROW2 features a "Select all" button for faster clerical
  review.
- **Accessibility-aware**: While CROW1 does have some accessibility features,
  CROW2 was built with WCAG-inspired font-resizing, zoom support, hover
  tooltips, and screen reader compatibility.

## Getting Started

See the `README.md` files and `docs` or `instructions` folders in the
`version1_tkinter` and `version2_flask` directories for more detailed guides on
getting set up with each version of the app.

### Prerequisites

- Python 3.9+
- Specific requirements for CROW1 vs CROW2 are listed in the `requirements.txt`
  file within the corresponding app's directory.

### Installation

1. **Clone this repository**:

   ```sh
   git clone https://github.com/Data-Linkage/Clerical_Resolution_Online_Widget.git
   ```

   and navigate into directory of the app version you would like to use:

   ```sh
    cd Clerical_Resolution_Online_Widget/version1_tkinter
   ```

   or

   ```sh
   cd Clerical_Resolution_Online_Widget/version2_flask
   ```

2. **Create a virtual environment** (not necessary for CROW2):

   ```sh
   python -m venv .venv
   ```

   and activate it:

   ```sh
   .venv/Scripts/activate
   ```

3. **Install dependencies**:

   ```sh
   pip install -r requirements.txt
   ```

### Running CROW

1. Edit the configuration file (`Config_clusters.ini` or `Config_pairwise.ini`
   for CROW1, `config_flow.ini` for CROW2) in a text editor to suit your data.
   Instructions are embedded within the corresponding configuration file.

   > [!WARNING]
   >
   > Make sure you do not change the name of the configuration file, the script
   > wil not be able to read it if you do.

2. Run the script (`CROW_clusters.py` or `CROW_pairwise.py` for CROW1,
   `flask_new_flow.py` for CROW2):

   ```sh
   python your_script_name.py
   ```

## Documentation

Detailed setup and user guides can be found in the respective `README.md` and
`docs` or `instructions` folders for each version:

- **CROW1**: `version1_tkinter/docs/`
- **CROW2**: `version2_flask/instructions/`

## Accessibility

We follow [Web Content Accessibility Guidelines (WCAG) 2.0][wcag] where
possible. Current support includes:

- Adjustable font sizes (CROW1 and CROW2) and style (CROW2 only). Size can be
  adjusted with buttons in CROW1, or via browser zoom in CROW2.
- High contrast muted hover tooltips (CROW2 only).
- Screen-reader "read aloud" compatibility (CROW2 only). This only works if
  opened in Microsoft Edge.

Planned in future releases:

- Keyboard-tab navigation.
- Custom background/text colour themes.
- Grey-out of already-reviewed records.

## Contributing

We welcome community contributions, but please read the [contributing
guidelines][contributing] first. This will tell you:

- How to file bugs or feature requests.
- Branching and pull request guidelines.
- Coding standards.

## License

This project is released under the [MIT License][license].

## Contact and Support

If you have any feedback, questions, require more information, need help, or for
anything else please raise and issue or contact the CROW team directly:

- File an issue: [GitHub Issues][issues]
- Email: <linkage.hub@ons.gov.uk>

## Acknowledgments

We are grateful to colleagues within the Data Linkage Hub and wider Office for
National Statistics for providing support, expert advice, and peer
review of this work.

[contributing]: ./CONTRIBUTING.md
[issues]: https://github.com/Data-Linkage/Clerical_Resolution_Online_Widget/issues
[license]: ./LICENSE
[wcag]: https://www.w3.org/TR/2008/REC-WCAG20-20081211/
