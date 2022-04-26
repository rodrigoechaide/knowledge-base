# MacOS

## Reference Documents

* [https://www.bretfisher.com/shell/](https://www.bretfisher.com/shell/)
* [https://gist.github.com/kevin-smets/8568070](https://gist.github.com/kevin-smets/8568070)
* [https://github.com/agnoster/agnoster-zsh-theme/issues/123](https://github.com/agnoster/agnoster-zsh-theme/issues/123)

## Install Homebrew

```text
# https://brew.sh/

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew tap Homebrew/bundle
```

## Install Tools with Homebrew

Brewfile example:

```ruby
# casks
cask 'dbeaver-community'
cask 'docker'
cask 'iterm2'
# cask 'google-chrome'
cask 'google-drive'
cask 'gpg-suite-no-mail'
cask 'macpass'
cask 'slack'
cask 'spotify'
cask 'visual-studio-code'
cask 'zoom'


# brew
brew 'bat'
brew 'dive'
brew 'duf'
brew 'envchain'
brew 'exa'
brew 'fd'
brew 'go'
brew 'helm'
brew 'jq'
# https://krew.sigs.k8s.io/docs/user-guide/setup/install/
brew 'krew'
brew 'kubernetes-cli'
brew 'kubectx' # kubens and kubectx
tap 'johanhaleby/kubetail'
brew 'kubetail'
brew 'mas'
brew 'skopeo'
brew 'terraform'
brew 'tfenv'
brew 'tldr'
# https://github.com/tmux/tmux/wiki
brew 'tmux'
```

Install programs:

```text
# Run in the same directory where Brewfile is
brew bundle
```

## Configure iterm2

```text
# import iterm2 profile
```

* Configure Profile
  * Enable setting "use built-in powerline glyphs"
  * Select "Solarized Dark" color preset
  * Configure Natural Text editing in the key configuration in the profile

## Install and configure oh-my-zsh

```text
# https://ohmyz.sh/#install

ZSH="$HOME/.oh-my-zsh" sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
```

* Change Prompt
* Configure [theme](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)
  * I like to use agnoster theme. If it is is now showing properly, download and install powerline fonts and restart iTerm2.
  * Download latest version of [agnoster](https://github.com/agnoster/agnoster-zsh-theme) theme
  * External themes are available [here](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes)
* Configure following plugins
  * aws
  * docker
  * git
  * go
  * kubernetes
  * python
  * vscode
* Import custom .zshrc from dotfiles repo
  * Add zsh alias so when calling cat, bat is called instead.

## Install Custom Fonts

```text
TBC
```

* Download and install
  * [Powerline Fonts](https://github.com/powerline/fonts)
  * [Nerd Fonts](https://www.nerdfonts.com/font-downloads)
  * [Patched Fonts](https://github.com/ryanoasis/nerd-fonts#patched-fonts)
  * [Powerline Extra Symbols](https://github.com/ryanoasis/powerline-extra-symbols)
  * [Programming Fonts](https://www.programmingfonts.org/)
  * [How to install fonts with brew](https://github.com/Homebrew/homebrew-cask-fonts)
  * [How to install fonts on macos](https://support.apple.com/en-us/HT201749)

**Note:** To enable [icons/glyphs](https://www.nerdfonts.com/) on spacevim and on iTerm, I think that powerline or the font chosen on the iterm profile should be patched in order to add icons to it.

## Install and configure spacevim

```text
# https://spacevim.org/quick-start-guide/#linux-and-macos

curl -sLf https://spacevim.org/install.sh | bash
```

* [quick-start-guide](https://spacevim.org/quick-start-guide/)
* Customize configuration in ~/.SpaceVim.d/init.toml
* Configure [vimdevicons](https://github.com/ryanoasis/vim-devicons)
* Configure spacevim [themes/colorschemes](https://spacevim.org/layers/colorscheme/)
  * Try to get fire theme that bretfisher used

## Other Configurations

* Configure pipenv environment (store this in a github repo) with useful python libraries and configure zsh to start that venv with each shell. Put in the prompt a very short text indicating that we are inside the venv. Check this [github issue](https://github.com/pypa/pipenv/issues/1509)
* [legacy-linux-commands-alternatives](https://itsfoss.com/legacy-linux-commands-alternatives/)
* [Glyphs](https://glyphsapp.com/)
