# Sourcebrew

A simple package manager inspired by [Homebrew](https://brew.sh/) for building and installing packages from the source code on macOS.

*Note that, while sourcebrew is inspired by Homebrew's command syntax and functionality, it does not attempt to mimic its architecture or scale. I intend to add only a few package install scripts, though contributions are welcome.*

## Rationale

While installing software from pre-built packages is very convenient, there are times where installation from the source code is desired. Some people may want to modify the software before installing it, others may want to be sure of the built software's integrity. Sometimes a pre-built package isn't available, so building from source is the only option.

While Homebrew does have a `--build-from-source` flag for the `brew upgrade` command, I've found its implementation varies from package-to-package. Furthermore, this option is [intended as developer-only behavior](https://github.com/Homebrew/brew/issues/18226#issuecomment-2324882406), not as an option for persistent installation like Sourcebrew.

## Installing

*Instructions TBD.*

## Usage

### Installing a Package

```bash
sourcebrew install [recipe name]
```

### Updating the Package List

```bash
sourcebrew update
```

### Upgrading a Package

```bash
sourcebrew upgrade [recipe name]
```

*Note that, unlike Homebrew, to upgrade all packages you must explicitly supply the `--all` flag, since building from a recipe is a much bigger commitment than installing from a formula.*

### Uninstalling a Package

```bash
sourcebrew uninstall [application name]
```

## Defining Build Instructions

Instructions for building, installing, and managing a package are defined in a *recipe*, which is conceptually similar to a [formula](https://docs.brew.sh/Formula-Cookbook) in Homebrew. You can find more information about creating recipes in `Recipe Cookbook.md`
