# Kahroba language documentation.
This documentation is built with the MkDocs Material, and if you need to read [documents](https://squidfunk.github.io/mkdocs-material/) before making any change.

## How to publish | depending on version.
It's very simple and you need to know witch version you want to publish.
We use **Mike** library to build out package in different versions.

Steps:
* First determine witch version you want to make a change.
* Pull `gh-pages` branch
* run `mike deploy --push --update-aliases <version> latest`

Usage example:
```
mike deploy --push --update-aliases 0.1 latest
```