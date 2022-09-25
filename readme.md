# Kahroba language documentation.
This documentation is built with the MkDocs Material, and if you need to read [documents](https://squidfunk.github.io/mkdocs-material/) before making any change.

## How to contribute?
* Clone the project using `git`.
* Install dependencies ([MKDocs Material](https://squidfunk.github.io/mkdocs-material/getting-started/) - [Mike](https://github.com/jimporter/mike)).
* Edit .md files exists in docs folder.

Do not change the directories structure of `docs` folder without changing the `mkdocs.yml` `nav settings`, also do not touch mkdocs.yml unless you know what you are doing!


### Starting Live server:
* Navigate to project directory.
* Run `mkdocs serve` command
* Open `localhost:8000` url to check what's going on.

## How to publish version based.
It's very simple, You need to know witch version you want to publish.
We use **Mike** library to build out package in different versions. For more help checkout [example](#publish-example).

Steps:
* Determine witch version you want to make a change.
* Make sure you installed dependencies (mike, MKDocs-Material) [from here](#how-to-contribute).
* Pull `gh-pages` branch to merge any change before yours.
* run `mike deploy --push --update-aliases <version> latest`

### Publish example:
Below command will be accessible from:
* `https://kahroba-lang.github.io/docs/latest`
* https://kahroba-lang.github.io/docs/0.1


```
mike deploy --push --update-aliases 0.1 latest

```
