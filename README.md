# Sortie

[![PyPI version](https://badge.fury.io/py/sortie.svg)](https://badge.fury.io/py/sortie)

An opinionated tool for formatting your `pyproject.toml` files. Built in Rust and based on
[taplo](https://github.com/tamasfe/taplo).

**Should you use this?**

Generally, using [taplo](https://github.com/tamasfe/taplo) would probably be more suitable for the typical
workflow. The primary purpose of this Python package is to facilitate easy integration with Python-based CI/CD pipelines
solely for formatting `pyproject.toml` files.

# Using Sortie

Sortie is available as [sortie](https://pypi.org/project/sortie/) on PyPI:

```sh
pip install sortie
```

To use sortie you can try the following:

```sh
sortie          # formats pyproject file
sortie --check  # checks if pyproject file needs to be formatted
```

To use Sortie (v0.1.0) via pre-commit, add the following to your `.pre-commit-config.yaml`:

```yaml
  - repo: https://github.com/8bit-pixies/sortie-pre-commit
    rev: v0.1.0
    hooks:
      - id: sortie
```

## Options

You can modify the behavior of the formatter by setting the configuration in your `pyproject.toml`
file. _Sortie_ utilizes the `[tool.sortie]` section of your file. For full options, refer to
[formatter options](https://taplo.tamasfe.dev/configuration/formatter-options.html). 

Here is an example `pyproject.toml` file:

```toml
[tool.sortie]
reorder_arrays = true
reorder_keys = true
```
