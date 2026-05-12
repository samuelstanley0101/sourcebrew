# Sourcebrew

A simple package manager inspired by [Homebrew](https://brew.sh/) for building and installing applications from the source code on macOS.

*Note that, while sourcebrew is inspired by Homebrew's command syntax and functionality, it does not attempt to mimic its architecture or scale. I intend to add only a few application install scripts, though contributions are welcome.*

## Rationale

While installing software from pre-built packages is very convenient, there are times where installation from the source code is desired. Some people may want to modify the software before installing it, others may want to be sure of the built software's integrity. Sometimes a pre-built package isn't available, so building from source is the only option.

While Homebrew does have a `--build-from-source` flag for the `brew upgrade` command, I've found its implementation varies from application to application. Furthermore, this option is [intended as developer-only behavior](https://github.com/Homebrew/brew/issues/18226#issuecomment-2324882406), not as an option for persistent installation like Sourcebrew.

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
