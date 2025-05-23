# Contributing to `Clerical_Resolution_Online_Widget`

Thank you for taking the time to contribute!

The following is a set of guidelines for contributing to CROW. These are mostly
guidelines, not rules. Use your best judgement, and feel free to propose changes
to this document in a pull request. If you still have questions, [please contact
us][email] and we would be happy to help!

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Development Environment](#development-environment)
  - [Pull Requests](#pull-requests)
- [Code Conventions](#code-conventions)
  - [Git](#git)
  - [Documentation](#documentation)
  - [Python](#python)
  - [HTML](#html)
  - [CSS](#css)

## Code of Conduct

This project and everyone participating in it are governed by the Code of
Conduct. Please read the [Code of Conduct][code-of-conduct] before contributing.

## How Can I Contribute?

### Reporting Bugs

This section guides you through submitting a bug report for CROW. Following
these guidelines helps maintainers and the community understand your report,
reproduce the behaviour, and find related reports.

Before creating bug reports, please perform a [cursory search][crow-issues] to
see if the problem has already been reported. If it has, **and the issue is
still open**, add a comment to the existing issue instead of opening a new one.
When you are creating a bug report, please [include as many details as
possible](#how-do-i-submit-a-good-bug-report).

> **Note:** If you find a **Closed** issue that seems like it is the same thing
> that you are experiencing, open a new issue and include a link to the original
> issue in the body of your new one.

#### How Do I Submit a (Good) Bug Report?

Bugs are tracked as [GitHub issues][github-docs-issues]. After you have
determined which version of CROW your bug is related to, create an issue and
provide the following information.

Explain the problem and include additional details to help maintainers reproduce
the problem:

- **Use a clear and descriptive title** for the issue to identify the problem.
- **Describe the exact steps which reproduce the problem** in as much detail as
  possible. For example, start by explaining how you started CROW, e.g. the
  exact command you used in the terminal, or how you started CROW otherwise.
  When listing steps, **do not just say what you did, but explain how you did
  it**.
- **Provide specific examples to demonstrate the steps.** If you are providing
  code snippets in the issue, use [Markdown code
  blocks][github-docs-code-blocks].
- **Describe the behaviour you observed after following the steps** and point
  out the exact problem with that behaviour.
- **Explain what behaviour you expected to see instead and why.**
- **Include screenshots** which show you following the described steps and
  clearly demonstrate the problem.
- **If the problem was not triggered by a specific action,** describe what you
  were doing before the problem happened and share more information using the
  guidelines below.

Provide more context by answering these questions:

- **Did the problem start happening recently** (e.g. after updating to a new
  version of CROW) or was this always a problem?
- **Can you reliably reproduce the issue?** If not, provide details about how
  often the problem happens and under what conditions it normally happens.
- If the problem is related to working with files (e.g. opening or saving
  files), **does the problem happen for all files and projects or only some?**
  Does the problem happen only when working with local or remote files, with
  files of a specific type (e.g. only CSV or parquet files), or with large
  files? Is there anything else special about the files you are using?

Include details about your configuration and environment:

- **What software versions are you using?** Include your Python version if your
  issue is with CROW1 and your Python and spark versions if your issue is with
  CROW2.
- **Which packages do you have installed?** You can get that list by running the
  command `pip list` in the terminal.

### Suggesting Enhancements

This section guides you through submitting an enhancement suggestion for CROW,
including completely new features and minor improvements to existing
functionality. Following these guidelines helps maintainers and the community
understand your suggestion and find related suggestions.

Before creating enhancement suggestions, please perform a [cursory
search][crow-issues] to see if the enhancement has already been suggested. If it
has, add a comment to the existing issue instead of opening a new one. When you
are creating an enhancement suggestion, please include as many details as
possible.

#### How Do I Submit a (Good) Enhancement Suggestion?

Enhancement suggestions are tracked as [GitHub
issues][github-docs-issues]. After you have determined which version of
CROW your enhancement suggestion is related to, create an issue and provide the
following information:

- **Use a clear and descriptive title** for the issue to identify the
  suggestion.
- **Provide a step-by-step description of the suggested enhancement** in as much
  detail as possible. Use [Markdown code blocks][github-docs-code-blocks] if you
  are providing code snippets.
- **Describe the current behaviour** and **explain what behaviour you expect to
  see instead** and why.
- **Explain why this enhancement would be useful** to most CROW users.

### Development Environment

The following steps should help you set up your development environment so you
can start contributing code to CROW.

#### CROW1

1. If you are a member of the `Data-Linkage` organisation, clone the CROW GitHub
   repository:

   ```shell
   git clone https://github.com/Data-Linkage/Clerical_Resolution_Online_Widget.git
   ```

   Otherwise, create a [fork][github-docs-forks] of the GitHub repository and
   clone your fork as above.

2. Set up a Python virtual environment - [there are many ways to set up a
   virtual environment][virtual-environments], so we will let you decide what is
   best for you!
3. Install the necessary packages using `pip`:

   ```shell
   pip install -r version1_tkinter/requirements.txt
   ```

#### CROW2

1. Access your project in Cloudera AI in the Cloudera Data Platform (CDP), and
   start a session.
2. Open a terminal by clicking `Terminal Access` within the session.
3. If you are a member of the `Data-Linkage` organisation, clone the CROW GitHub
   repository:

   ```shell
   git clone https://github.com/Data-Linkage/Clerical_Resolution_Online_Widget.git
   ```

   Otherwise, create a [fork][github-docs-forks] of the GitHub repository and
   clone your fork as above.

4. Install the necessary packages using `pip`:

   ```shell
   pip install -r version2_flask/requirements.txt
   ```

### Pull Requests

Please follow these steps to have your contribution considered by the
maintainers:

1. [Create a new branch][github-docs-branches] from the `main` branch. If you
   are implementing a feature, name it `feat/name_of_feature`. If you are
   implementing a bug fix, name it `bug/name_of_issue`.
2. Implement your changes, following the relevant [code
   conventions](#code-conventions) for the changes you are making.
3. Update the `README.md`, as well as any other documentation, with relevant
   details of changes made. This might include: new configuration file
   parameters, new features or changes to existing features, or changes to the
   user interface.
4. You can open a [pull request][github-docs-pull-requests] from your branch to
   the `main` branch after your first commit, but if it is not yet ready for
   review, be sure to make it a [_draft_ pull
   request][github-docs-draft-pull-request]. Once your changes are ready for
   review, please mark your pull request as ready for review.
5. The pull request will be merged once you have the sign-off of a maintainer.

## Code Conventions

We mainly follow the [GDS Way][gds-way] in our code conventions.

### Git

We use Git to version control the source code. Please read the [quality
assurance of code for analysis and research][version-control] for details on Git
best practice. This includes how to write good commit messages, how to branch
appropriately, and how to solve merge conflicts.

### Documentation

- Use [Markdown][markdown-guide].
- To keep the files uniform, all links should be referenced at the bottom of the
  markdown file. This also helps to keep the Markdown file organised.
- Try to wrap Markdown to a line length of 80 characters. This is not strictly
  enforced in all cases (e.g. with long hyperlinks).

### Python

You can refer to the GDS Way's [Python][gds-way-python-style] coding style page,
but you should at least try to:

- Follow [PEP 8][pep-0008] for code style.
- Follow [PEP 257][pep-0257] for docstring conventions. In particular, try to
  adhere to [the numpy format][numpydoc-format] when documenting modules,
  classes, and functions using docstrings.
- If possible, ensure every function you create/change comes with a suitable
  test suite. Refer to the [GDS Way's Test-driven development][gds-way-tdd] page
  for more information.

You can automatically format and lint your Python code using packages such as
[Ruff][ruff], which is available [via PyPi][ruff-pypi].

### HTML

Refer to the GDS Way's [HTML][gds-way-html-style] coding style page.

### CSS

Refer to the GDS Way's [CSS][gds-way-css-style] coding style page.

[code-of-conduct]: ./CODE_OF_CONDUCT.md
[crow-issues]: https://github.com/Data-Linkage/Clerical_Resolution_Online_Widget/issues?q=is%3Aissue
[email]: mailto:linkage.hub@ons.gov.uk
[gds-way]: https://gds-way.digital.cabinet-office.gov.uk/
[gds-way-css-style]: https://gds-way.digital.cabinet-office.gov.uk/manuals/programming-languages/css.html
[gds-way-html-style]: https://gds-way.digital.cabinet-office.gov.uk/manuals/programming-languages/html.html
[gds-way-python-style]: https://gds-way.digital.cabinet-office.gov.uk/manuals/programming-languages/python/python.html
[gds-way-tdd]: https://gds-way.digital.cabinet-office.gov.uk/standards/test-driven-development.html
[github-docs-issues]: https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues
[github-docs-branches]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches
[github-docs-code-blocks]: https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks
[github-docs-draft-pull-request]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests#draft-pull-requests
[github-docs-forks]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks
[github-docs-pull-requests]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests
[markdown-guide]: https://www.markdownguide.org/
[numpydoc-format]: https://numpydoc.readthedocs.io/en/latest/format.html
[pep-0008]: https://peps.python.org/pep-0008/
[pep-0257]: https://peps.python.org/pep-0257/
[ruff]: https://docs.astral.sh/ruff/
[ruff-pypi]: https://pypi.org/project/ruff/
[version-control]: https://best-practice-and-impact.github.io/qa-of-code-guidance/version_control.html
[virtual-environments]: https://www.pluralsight.com/tech-blog/managing-python-environments/
