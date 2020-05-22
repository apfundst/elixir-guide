---
title: Install Elixir with asdf
date: "2020-05-20T22:12:03.284Z"
description: "Getting started with local elixir development using asdf for version management"
---

Before you start working on elixir projects, you will need to have elixir installed. I recommend using `asdf` to install and manage elixir versions.  If you don't already have `asdf` setup on your machine, follow the [asdf installation guide](https://asdf-vm.com/#/core-manage-asdf-vm).  Once `asdf` is installed and working, you will need to install `elixir` and `erlang`

## Install Erlang

To install `erlang` run the following

```bash
# Adds erlang to asdf
asdf plugin-add erlang https://github.com/asdf-vm/asdf-erlang.git

# for OSX run (other systems, check here: https://github.com/asdf-vm/asdf-erlang#before-asdf-install)
brew install autoconf
brew install wxmac

# Install a specific erlang version
asdf install erlang <version>
```

Installing `erlang` typically takes a while, so now would be a good time to grab a coffee.

## Install Elixir

Then install elixir by running:

```bash
asdf plugin-add elixir https://github.com/asdf-vm/asdf-elixir.git
asdf install elixir <version>
```

## Start working

Once you have installed your desired `elixir` and `erlang` versions pop into your working directory and run the following

```bash
asdf local elixir <version>
asdf local erlang <version>
```

This will set the versions to use in this project and will likely create a `.tool-versions` file.  This is much like a `.node-version` or `.ruby-version` file. If there is a `.tool-versions` file already present in your project, you can simply run `asdf install` to set up all local project versions.