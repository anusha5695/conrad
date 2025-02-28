# Contributor's Guide

If you're reading this, you're probably looking to contributing to conrad. *Time is the only real currency*, and the fact that you're considering spending some here is *very* generous of you. Thank you very much!

This document will help you get started with contributing code, testing (future) and filing issues. If you have any questions, feel free to reach out to [Vinayak Mehta](https://vinayak-mehta.github.io), the author and maintainer.

## Code Of Conduct

The following quote sums up the **Code Of Conduct**.

   > Be cordial or be on your way. --Kenneth Reitz

As the [Requests Code Of Conduct](https://github.com/psf/requests/blob/master/CODE_OF_CONDUCT.md) states, **all contributions are welcome**, as long as everyone involved is treated with respect.

## Your first contribution

A great way to start contributing to conrad is to pick an issue with the [good first issue](https://github.com/vinayak-mehta/conrad/labels/good%20first%20issue) label. If you're unable to find a good first issue, feel free to contact the maintainer.

## Setting up a development environment

To install the dependencies needed for development, you can use pip:

<pre>
$ pip install conference-radar[dev]
</pre>

Alternatively, you can clone the project repository, and install using pip:

<pre>
$ pip install ".[dev]"
</pre>

## Pull Requests

### Submit a pull request

The preferred workflow for contributing to conrad is to fork the [project repository](https://github.com/vinayak-mehta/conrad) on GitHub, clone, develop on a branch and then finally submit a pull request. Here are the steps:

1. Fork the project repository. Click on the ‘Fork’ button near the top of the page. This creates a copy of the code under your account on the GitHub.

2. Clone your fork of conrad from your GitHub account:

<pre>
$ git clone https://www.github.com/[username]/conrad
</pre>

3. Create a branch to hold your changes:

<pre>
$ git checkout -b my-feature
</pre>

Always branch out from `master` to work on your contribution. It's good practice to never work on the `master` branch!

**Protip: `git stash` is a great way to save the work that you haven't committed yet, to move between branches.**

4. Work on your contribution. Add changed files using `git add` and then `git commit` them:

<pre>
$ git add modified_files
$ git commit
</pre>

5. Finally, push them to your GitHub fork:

<pre>
$ git push -u origin my-feature
</pre>

Now it's time to go to the your fork of conrad and create a pull request! You can [follow these instructions](https://help.github.com/articles/creating-a-pull-request-from-a-fork/) to do this.

### Work on your pull request

It is recommended that your pull request complies with the following rules:

- Make sure your code follows [pep8](http://pep8.org). You should [blacken](https://github.com/psf/black) your code.

- Make sure your commit messages follow [the seven rules of a great git commit message](https://chris.beams.io/posts/git-commit/):
    - Separate subject from body with a blank line
    - Limit the subject line to 50 characters
    - Capitalize the subject line
    - Do not end the subject line with a period
    - Use the imperative mood in the subject line
    - Wrap the body at 72 characters
    - Use the body to explain what and why vs. how

- Please prefix the title of your pull request with [MRG] (Ready for Merge), if the contribution is complete and ready for a detailed review. An incomplete pull request's title should be prefixed with [WIP] (to indicate a work in progress), and changed to [MRG] when it's complete. A good [task list](https://blog.github.com/2013-01-09-task-lists-in-gfm-issues-pulls-comments/) in the PR description will ensure that other people get a better idea of what it proposes to do, which will also increase collaboration.

- If contributing new functionality, make sure that you add a unit test for it, while making sure that all previous tests pass. conrad uses [pytest](https://docs.pytest.org/en/latest/) for testing (future). Tests can be run using:

<pre>
$ python setup.py test
</pre>

## Filing Issues

[GitHub issues](https://github.com/vinayak-mehta/conrad/issues) are used to keep track of all issues and pull requests. Before opening an issue (which asks a question or reports a bug), please use GitHub search to look for existing issues (both open and closed) that may be similar.

### Bug Reports

In bug reports, make sure you include:

- Your operating system type and Python version:

<pre>
import platform; print(platform.platform())
import sys; print('Python', sys.version)
</pre>

- The complete traceback. Just adding the exception message or a part of the traceback won't help the maintainer fix your issue sooner.
