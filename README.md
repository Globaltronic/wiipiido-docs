# WiiPiiDo Documentation

This repository contains the source files used in the WiiPiiDo online documentation.

## Quick Start
This documentation uses [MkDocs](https://www.mkdocs.org/) to generate the online documentation, as well as some plugins. \
To start using this projects, install the necessary requirements by running:

```bash
pip install -r requirements.txt
```

When installed, you can start the documentation build process by running:

```bash
mkdocs serve
```

Then you can access the `localhost:8000` to check the site and make modifications at run time.

To deploy the documentation to GitHub Pages, simply run:

```bash
mkdocs gh-deploy
```
