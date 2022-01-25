# Quick docs

Quickly deploy a full-featured docs setup to Cloudflare Pages.

This is an opinionated setup: I have chosen to enable and configure features I usually want, such as navigation tabs and admonitions.

## Features

- MkDocs with the Material theme
- Vale GitHub Action
- Support for [Plausible](https://plausible.io/) analytics

## Quickstart

1. Copy the contents of this repo to your own repo.
2. Follow the instructions on [how to deploy MkDocs to Cloudflare Pages](https://starfallprojects.co.uk/projects/deploy-host-docs/deploy-mkdocs-material-cloudflare/). Note that this example repo uses the free version of Material. Once done, you have a live site!

## Work on the site

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



## Resources

The `mkdocs.yml` includes links to documentation on each theme feature that I'm using. The Material theme is the foundation of this project, and its [documentation](https://squidfunk.github.io/mkdocs-material/) is extensive and very helpful. You can also learn more about [MkDocs](https://www.mkdocs.org/), the static site generator underpinning the theme.
