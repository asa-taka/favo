# favo - A directory name resolver for favorite locations

## Installation

```sh
PROFILE=~/.zshrc # or your profile
# Set FAVO_PATH for your favorite locations to search.
echo 'export FAVO_PATH=$HOME/src:$HOME/Documents' >> "${PROFILE}"
# Insert initializing script, currently, for `fago` utility command.
echo 'eval "$(favo init)"' >> "${PROFILE}"
```

## Usage

```sh
# Tell where the favorite directories denoted like $PATH style.
export FAVO_PATH=$HOME/src:$HOME/Documents

# Just find a directory by name.
favo resolve my-dir-in-favorite-path

# `favo resolve` and cd to it.
fago my-dir-in-favorite-path
```

Other commands and functions are below.

```
favo - A directory name resolver for favorite locations(FAVO_PATH)
Usage: favo <command> [<options> ...]
Commands:
  env               Print values of configurable variables.
  help              Print whole help.
  init              Print script to declare utilities to eval in profile.
  list [-1fl]       Show all directories that resolvable.
  open <dir-name>   Open a directory resolved by name.
  path              Show paths to search directories
  resolve <dir-name>
                    Resolve a directory name from paths.
Environment variables:
  FAVO_PATH         Search target locations separated by ':' (e.g. '~/src:~/.local/src/')
  FAVO_EDITOR       A command to open directory (default: code)
```

## Completion

Place `_favo` and `_fago` into the dir where your `fpath` indicates.
