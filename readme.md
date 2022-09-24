# Kahroba language documentation.
This documentation is built with the MkDocs Material, and if you need to read [documents](https://squidfunk.github.io/mkdocs-material/) before making any change.

## How to contribute?
* Clone the project using `git` or simple download.
* Install `mkdocs-material`.
* Edit .md files exists in docs folder.

Do not change the directories structure of `docs` folder without changing the `mkdocs.yml` `nav settings`, also do not touch mkdocs.yml unless you know what you are doing!



### Starting Live server:
* Navigate to project directory.
* Run `mkdocs serve` command
* Open `localhost:8000` url to check what's going on.

## How to publish | depending on version.
It's very simple and you need to know witch version you want to publish.
We use **Mike** library to build out package in different versions.

Steps:
* First determine witch version you want to make a change.
* Pull `gh-pages` branch
* run `mike deploy --push --update-aliases <version> latest`

Usage example:
```
# Will be accessable from https://kahroba-lang.github.io/docs/latest
# or https://kahroba-lang.github.io/docs/0.1
mike deploy --push --update-aliases 0.1 latest
```
