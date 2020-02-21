# jlab-script-button

A button that executes scripts in the frontend of JupyterLab.

## Usage

Adds a button into the notebook toolbar. Pushing the button starts a temporary python3 kernel named "tmp\_kernel\_for\_executing\_button\_code", which executes the following:

```bash
![ -z $BUTTON_EXTENSION_SCRIPT_PATH ] && /usr/local/bin/jlab_script_button.sh [notebook_path] \ 
                                      || eval $BUTTON_EXTENSION_SCRIPT_PATH [notebook_path]
```
So if ```$BUTTON_EXTENSION_SCRIPT_PATH``` is defined, the button runs the script at said path with the notebook's path as the argument. Otherwise the default script ```/usr/local/bin/jlab_script_button.sh``` is used.


### (AUTO-GENERATED BY COOKIECUTTER:)

# jlab-script-button

![Github Actions Status](https://github.com/my_name/myextension/workflows/Build/badge.svg)

A button that executes scripts in the frontend of JupyterLab.


## Requirements

* JupyterLab >= 1.0

## Install

```bash
jupyter labextension install @loncero/jlab-script-button
```

## Contributing

### Install

The `jlpm` command is JupyterLab's pinned version of
[yarn](https://yarnpkg.com/) that is installed with JupyterLab. You may use
`yarn` or `npm` in lieu of `jlpm` below.

```bash
# Clone the repo to your local environment
# Move to jlab-script-button directory
# Install dependencies
jlpm
# Build Typescript source
jlpm build
# Link your development version of the extension with JupyterLab
jupyter labextension link .
# Rebuild Typescript source after making changes
jlpm build
# Rebuild JupyterLab after making any changes
jupyter lab build
```

You can watch the source directory and run JupyterLab in watch mode to watch for changes in the extension's source and automatically rebuild the extension and application.

```bash
# Watch the source directory in another terminal tab
jlpm watch
# Run jupyterlab in watch mode in one terminal tab
jupyter lab --watch
```

### Uninstall

```bash
jupyter labextension uninstall @loncero/jlab-script-button
```

