# Poetry export plugin

This package is a plugin that allows the export of locked packages to various formats.

**Note**: For now, only the `requirements.txt` format is available.

This plugin provides the same features as the existing `export` command of POetry which it will eventually replace.


## Installation

The easiest way to install the `export` plugin is via the `plugin add` command of Poetry.

```bash
poetry plugin add poetry-export-plugin
```

If you used `pipx` to install Poetry you can add the plugin via the `pipx inject` command.

```bash
pipx inject poetry poetry-export-plugin
```

Otherwise, if you used `pip` to install Poetry you can add the plugin packages via the `pip install` command.

```bash
pip install poetry-export-plugin
```


## Usage

The plugin provides an `export` command to export to the desired format.

```bash
poetry export -f requirements.txt --output requirements.txt
```

**Note**: Only the `requirements.txt` format is currently supported.

### Available options

* `--format (-f)`: The format to export to (default: `requirements.txt`). Currently, only `requirements.txt` is supported.
* `--output (-o)`: The name of the output file.  If omitted, print to standard output.
* `--dev`: Include development dependencies.
* `--only-dev`: Include only development dependencies.
* `--extras (-E)`: Extra sets of dependencies to include.
* `--without-hashes`: Exclude hashes from the exported file.
* `--with-credentials`: Include credentials for extra indices.
