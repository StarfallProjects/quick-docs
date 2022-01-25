# Quick docs

A full-featured docs setup.

This is an opinionated setup: 

- Commonly-used theme features, such as navigation tabs and admonitions, are enabled and configured.
- The project setup assumes you use pip to install requirements, and deploy to Cloudflare Pages.
- The linting uses the Microsoft writing style guide, write-good, and alex. See [Using Vale](#using-vale) for more details.

## Features

- [MkDocs](https://www.mkdocs.org/) with the [Material](https://squidfunk.github.io/mkdocs-material/) theme.
- [Vale](https://docs.errata.ai/) linting: [GitHub Action](https://github.com/errata-ai/vale-action) set to run on pull request, and an opinionated style setup.
- Support for [Plausible](https://plausible.io/) analytics

## Quick deploy to Cloudflare Pages

1. Copy the contents of this repo to your own repo.
2. Follow the instructions on [how to deploy MkDocs to Cloudflare Pages](https://starfallprojects.co.uk/projects/deploy-host-docs/deploy-mkdocs-material-cloudflare/). Note that this example repo uses the free version of Material. Once done, you have a live site!

## Work on the site locally

1. Clone your repo.
2. Create a virtual environment:
    ```
    python -m venv venv
    ```
3. Activate your virtual environment:
    ```
    # PowerShell
    /venv/Scripts/activate.ps1
    ```
4. Install requirements:
    ```
    pip install -r requirements.txt
    ```
    > **Note:** there are several ways to install the Material theme, which is the cornerstone of this project. But you must install using pip in order to use some features. I strongly recommend using pip.
5. View locally with `mkdocs serve`.

## Configure the site

## Using Vale

Vale provides text linting, both locally and on pull request using a GitHub Action.

The setup in this repo includes the following styles:

- [Microsoft](https://github.com/errata-ai/Microsoft): a Vale-compatible implementation of the [Microsoft Writing Style Guide](https://docs.microsoft.com/en-us/style-guide/welcome/).
- [write-good](https://github.com/errata-ai/write-good)
- [alex](https://github.com/errata-ai/alex): a Vale-compatible implementation of the guidelines enforced by the alex, a linter designed to catch insensitive writing.

### Configure your styles

1. In `styles`, rename `your-company-styles` to your company name, and in `.vale.ini` change `your-company-styles` to the new directory name.
2. In `styles/Vocab/default`, add any terms you want Vale to accept or reject to the appropriate `.txt` file. This is useful for allowing company-specific terminology (such as brand names) to pass the spell checker. Learn more about [Vale vocabularies](https://docs.errata.ai/vale/vocab).

### To lint your local files, you can:

- [Install Vale CLI](https://docs.errata.ai/vale/install) and run it with `vale --glob='*.md' docs` (this lints all Markdown files in your `docs` directory)
- Install Vale CLI or Vale Server, and use with one of the integrations, such as the VS Code extension. There is a list of integrations in the [docs](https://docs.errata.ai/).

## Resources

The `mkdocs.yml` includes links to documentation on each theme feature that I'm using. The Material theme is the foundation of this project, and its [documentation](https://squidfunk.github.io/mkdocs-material/) is extensive and very helpful. You can also learn more about [MkDocs](https://www.mkdocs.org/), the static site generator underpinning the theme.

Vale is a complex linting tool. The [documentation](https://docs.errata.ai/) is a good starting point. You may also want to learn a little about [GitHub Actions](https://docs.github.com/en/actions/quickstart).
