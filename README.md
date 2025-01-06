<!-- markdownlint-disable MD041 -->
<div style="text-align: center;" align="center">
  <img src="https://raw.githubusercontent.com/UCL-ARC/python-tooling/main/images/logo.svg" alt="UCL ARC Python tooling logo" width="120"/>
  <h1> Mecha Health Python Recommendations</h1>
</div>
<!-- markdownlint-restore -->

This repository collects the standard Mecha Health recommendations for a research software project in Python, derived from [UCL ARC]'s recommendation. It contains a template for new Python packages.

🍪 The template is a [cookiecutter] template which automatically creates new
Python packages with our recommended tooling set up and ready to go.


## Using the template

If you have [uv] installed, you can use our template with the following one-liner:

```sh
uvx cookiecutter gh:mecha-health/python-tooling
```

Alternatively you can [install cookiecutter] (following the recommended instructions).
Do this if you don't use [uv], or if you're likely to want to use cookiecutter again.

Then you'll need to run cookiecutter with our template:

```sh
cookiecutter gh:mecha-health/python-tooling
```

When [cookiecutter] runs, it will ask you a series of questions to configure your project.
Type the answer or hit return without typing anything to use the default option (shown in parenthesis).
At the end, it will print some more follow-up information in the terminal for things like creating a remote repository and making a website for your package.

It will have created a directory for your project.
You can see the structure with the `tree` command.
In our example we've called our project `example-research-software-project`:

```sh
ls -ltr | tail -n1 # Shows the last directory that was created
tree example-research-software-project
```

To work on your project, initialise a `git` repository and _install_ your new package editable mode.
You probably want to do this in a [virtual environment](./docs/pages/virtual.md).
The comments show how to do this in [uv] with `uv venv`:

```sh
cd example-research-software-project
git init
# uv venv
# source .venv/bin/activate
uv pip install -e ".[dev]"
```

<!-- links here -->

<!-- prettier-ignore-start -->
[UCL ARC]: https://ucl.ac.uk/arc
[cookiecutter]: https://cookiecutter.readthedocs.io/en/stable
[install cookiecutter]: https://cookiecutter.readthedocs.io/en/stable/README.html#installation
[uv]: https://docs.astral.sh/uv
<!-- prettier-ignore-end -->
