# Sourcebrew

A package manager inspired by [Homebrew](https://brew.sh/) for building and installing applications from the source code on macOS, since the `--build-from-source` flag in `brew install` only seems to work for some applications.

*Note that, while sourcebrew is inspired by Homebrew's command syntax and functionality, it does not attempt to mimic its architecture or scale. I intend to add only a few application install scripts, though contributions are welcome.*

## Installing

*Instructions TBD.*

## Usage

### Installing an Application

```bash
sourcebrew install [application name]
```

### Updating the Application List

```bash
sourcebrew update
```

### Upgrading an Application

```bash
sourcebrew upgrade [application name]
```

*Note that, unlike Homebrew, to upgrade all applications you must explicitly supply the `--all` flag, since building an application is a much bigger commitment than installing it from a package.*

### Uninstalling an Application

```bash
sourcebrew uninstall [application name]
```

## Defining Build Instructions

Instructions for building, installing, and managing an application are defined in a **Recipe**, which is conceptually similar to a [Formula](https://docs.brew.sh/Formula-Cookbook) in Homebrew. You can find more information about creating Recipes in `Recipe Cookbook.md`
