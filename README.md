# Morpx-docs
Morpx Inc. documents

Website: https://morpx-docs.readthedocs.io/en/latest/index.html

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

- 3.Make file:

    ```bash
    $ cd {your_project_path}/Morpx-docs/
    $ make html
    ```

- 4.Open file `index.html` in path `{your_project_path}/Morpx-docs/_build/html/index.html`