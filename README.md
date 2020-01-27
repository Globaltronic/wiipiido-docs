# WiiPiiDo Documentation

This repository contains the source files used in the WiiPiiDo online documentation.

## Quick Start
This documentation uses [MkDocs](https://www.mkdocs.org/) to generate the online documentation. \
To use MkDocs you simply need to install it first, using pip:

```bash
pip install mkdocs
```

When installed, you can start the documentation build process by running:

```bash
cd wiipiido-docs
mkdocs serve
```

Then you can access the `localhost:8000` to check the site and make modifications at run time.

To deploy the documentation to GitHub Pages, simply run:

```bash
mkdocs gh-deploy
```
