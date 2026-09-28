# dotfiles-bin

Personal utility scripts, symlinked into `~/.local/bin`.

Part of the [dotfiles-arch](https://github.com/SaratAngajalaoffl/dotfiles-arch) multi-repo dotfiles system.

## Layout

- `bin/*` → `~/.local/bin/` (one symlink per file, see `.links`)

## Scripts

- `aic` — AI-generate a Conventional Commits message for the current repo's staged
  diff, with confirm/edit/abort. `--generate` prints only (used by lazygit's `C`);
  `--agent claude|pi` picks the backend. See ADR 0004.
- `aicp` — the multi-repo version: generates messages for every dirty submodule in
  parallel, reviews and commits/pushes them, then does the same for the parent repo.
  Bound to lazygit's `A`. Needs a TTY + `whiptail`. See ADR 0006.

## Setup

Not used standalone — applied by the parent repo's `install.sh`, which reads `.links` and symlinks each script into place.
