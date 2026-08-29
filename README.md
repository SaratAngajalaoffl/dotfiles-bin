# dotfiles-bin

Personal utility scripts, symlinked into `~/.local/bin`.

Part of the [dotfiles-arch](https://github.com/SaratAngajalaoffl/dotfiles-arch) multi-repo dotfiles system.

## Layout

- `bin/*` → `~/.local/bin/` (one symlink per file, see `.links`)

## Setup

Not used standalone — applied by the parent repo's `install.sh`, which reads `.links` and symlinks each script into place.
