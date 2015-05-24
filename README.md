# dotfiles

dotfiles of my configuration files in OS X/Linux.

## Architecture

Use soft symlink for per-user configuration files

```
ln -s dotfiles/configuration_files ~/.configuration_files
```

Private tokens or other secret strings should be ignored by .gitignore. You can put your private tokens in a separate file named `.env_private` and `source` it in your main configuration files. Do not forget `chmod 600 env_private`.

Take my Github API token as an example, first you may set `HOMEBREW_GITHUB_API_TOKEN=xxxxx` in file `env_private`, then source it in your .zshrc.

```
# Read Private Environment file if it is present
[ -r ~/.env_private ] && . ~/.env_private

# Homebrew
export HOMEBREW_GITHUB_API_TOKEN=$HOMEBREW_GITHUB_API_TOKEN
```

## dircolors

- [seebi/dircolors-solarized](https://github.com/seebi/dircolors-solarized)

## Git

## tmux

- [seebi/tmux-colors-solarized](https://github.com/seebi/tmux-colors-solarized) - palette
