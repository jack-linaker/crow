# Contributing to CROW

Thank you for taking the time to contribute!

The following is a set of guidelines for contributing to CROW. These are mostly
guidelines, not rules. Use your best judgement, and feel free to propose changes
to this document in a pull request.

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Pull Requests](#pull-requests)
- [Style Guides](#style-guides)
  - [Git Commit Messages](#git-commit-messages)
  - [Documentation](#documentation)
  - [Python](#python)
  - [HTML](#html)
  - [CSS](#css)

## Code of Conduct

This project and everyone participating in it are governed by the Code of
Conduct.

> **Note:** The Code of Conduct has not been implemented yet. Please check back
> later for updates.

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
  out what exactly is the problem with that behaviour.
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

[back to the top](#contributing-to-crow)

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

[back to the top](#contributing-to-crow)

### Pull Requests

Please follow these steps to have your contribution considered by the
maintainers:

1. [Create a new branch][github-docs-branches] from the `main` branch. If you
   are implementing a feature, name it `feature/name_of_feature`. If you are
   implementing a bug fix, name it `bug/name_of_issue`.
2. Implement your changes, following the relevant [style guide](#style-guides)
   for the changes you are making.
3. Update the `README.md`, as well as any other documentation, with relevant
   details of changes made. This might include: new configuration file
   parameters, new features or changes to existing features, or changes to the
   user interface.
4. Once your changes are ready for review, please open a [pull
   request][github-docs-pull-requests] to the `main` branch.
5. You may merge the pull request once you have the sign-off of two maintainers.

[back to the top](#contributing-to-crow)

## Style Guides

### Git Commit Messages

- Use the present tense ("add feature" not "added feature").
- Use the imperative mood ("change cursor to..." not "changes cursor to...")
- Limit the first line (the subject) to 72 characters or less.
- Include references to relevant issues and pull requests.
- Consider starting the commit message with an applicable scope (e.g.
  contributing: add git commit message guidelines).
- Any useful information that does not fit on the subject line (e.g. references
  to relevant issues and pull requests) can be included in a new paragraph as
  follows:

  ```bash
  git commit -m "subject line" -m "A paragraph going into more detail."
  ```

### Documentation

- Use [Markdown][wikipedia-markdown].

> **Note:** The style guide for documentation has not been completed yet. Please
> check back later for updates.

### Python

- Follow [PEP 8][pep-0008] for code style.
- Follow [PEP 257][pep-0257] for docstring conventions. In particular, try to
  adhere to [the numpy format][numpydoc-format] when documenting modules,
  classes, and functions using docstrings.

You can automatically format and lint your Python code using packages such as
[Ruff][ruff], which is available [via PyPi][ruff-pypi].

### HTML

> **Note:** The style guide for HTML has not been implemented yet. Please check
> back later for updates. For now, you can refer to The GDS Way's
> [HTML][gds-way-html-style] coding style page.

### CSS

> **Note:** The style guide for CSS has not been implemented yet. Please check
> back later for updates. For now, you can refer to The GDS Way's
> [CSS][gds-way-css-style] coding style page.

[back to the top](#contributing-to-crow)

[crow-issues]: https://github.com/Data-Linkage/Clerical_Resolution_Online_Widget/issues?q=is%3Aissue
[gds-way-css-style]: https://gds-way.digital.cabinet-office.gov.uk/manuals/programming-languages/css.html
[gds-way-html-style]: https://gds-way.digital.cabinet-office.gov.uk/manuals/programming-languages/html.html
[github-docs-issues]: https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues
[github-docs-branches]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches
[github-docs-code-blocks]: https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks
[github-docs-pull-requests]: https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests
[numpydoc-format]: https://numpydoc.readthedocs.io/en/latest/format.html
[pep-0008]: https://peps.python.org/pep-0008/
[pep-0257]: https://peps.python.org/pep-0257/
[ruff]: https://docs.astral.sh/ruff/
[ruff-pypi]: https://pypi.org/project/ruff/
[wikipedia-markdown]: https://en.wikipedia.org/wiki/Markdown
