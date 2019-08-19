[![doc-build](https://img.shields.io/readthedocs/morpx-docs)](https://readthedocs.org/projects/morpx-docs/builds/)

# Morpx-docs
Morpx Inc. documents

Website: https://morpx-docs.readthedocs.io/

## Local edit

refer to [Read-the-Docs Getting Started with Sphinx](https://read-the-docs.readthedocs.io/en/latest/intro/getting-started-with-sphinx.html#)

- 1.Assuming you have Python already, install Sphinx:

    ```bash
    $ sudo pip install sphinx
    ```

- 2.Install `recommonmark` for markdown files(.md):

    ```bash
    $ sudo pip install recommonmark
    ```

- 3.Install theme `sphinx_rtd_theme`:
    ```bash
    $ sudo pip install sphinx_rtd_theme
    ```

- 4.Make file:

    ```bash
    $ cd {your_project_path}/Morpx-docs/
    $ make html
    ```

- 5.Open file `index.html` in path `{your_project_path}/Morpx-docs/_build/html/index.html`
