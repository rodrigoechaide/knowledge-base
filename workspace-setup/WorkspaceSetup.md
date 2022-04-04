# Workspace Customization

Improve this readme and put it in a repo together with .zshrc file plus Pipenv file with all needed python dependencies and also bash/zsh scripts to install all the necessary tools. The script should be idempotent and should work in mac, linux and wsl.

## Reference Documents

* https://www.bretfisher.com/shell/
* https://gist.github.com/kevin-smets/8568070
* https://github.com/agnoster/agnoster-zsh-theme/issues/123

## Terminal

### MAC

* Download and install iTerm2: https://iterm2.com/
  * Configure Profile
    * Enable setting "use built-in powerline glyphs"
    * Select "Solarized Dark" color preset
    * Configure Natural Text editing in the key configuration in the profile
* Other Configurations
  * Download and install brew: https://brew.sh/
  * Download and install ohmyzsh: https://ohmyz.sh/#install
    * Change prompt
    * Configure theme. I like to use agnoster theme. If it is is now showing properly, download and install powerline fonts and restart iTerm2.
      * Download agnoster latest version: https://github.com/agnoster/agnoster-zsh-theme
      * External themes are available here: https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes
    * Configure following plugins
      * aws
      * docker
      * git
      * go
      * kubernetes
      * python
      * vscode
  * Install Custom Fonts:
    * Download and install
      * [Powerline Fonts](https://github.com/powerline/fonts)
      * [Nerd Fonts](https://www.nerdfonts.com/font-downloads)
      * [Patched Fonts](https://github.com/ryanoasis/nerd-fonts#patched-fonts)
      * [Powerline Extra Symbols](https://github.com/ryanoasis/powerline-extra-symbols)
      * [Programming Fonts](https://www.programmingfonts.org/)
      * [How to install fonts with brew](https://github.com/Homebrew/homebrew-cask-fonts)
      * [How to install fonts on macos](https://support.apple.com/en-us/HT201749)
  * Download and install spaceVim
    * https://spacevim.org/quick-start-guide/
    * Customize configuration in ~/.SpaceVim.d/init.toml
    * Configure vimdevicons: https://github.com/ryanoasis/vim-devicons
    * Configure spacevim themes/colorschemes: https://spacevim.org/layers/colorscheme/
      * Try to get fire theme that bretfisher used
  * Download  following cli tools
    * bat (https://github.com/sharkdp/bat) -> Add zsh alias so when calling cat, bat is called instead.
    * tldr (https://tldr.sh/)
    * fd (https://github.com/sharkdp/fd)
    * exa (https://itsfoss.com/exa/)
    * duf (https://itsfoss.com/duf-disk-usage/)
    * tmux [tmux-wiki](https://github.com/tmux/tmux/wiki)
  * Install container images tools
    * dive (https://github.com/wagoodman/dive)
  * Configure pipenv environment (store this in a github repo) with useful python libraries and configure zsh to start that venv with each shell. Put in the prompt a very short text indicating that we are inside the venv. (https://github.com/pypa/pipenv/issues/1509)

Tools: https://itsfoss.com/legacy-linux-commands-alternatives/

Glyphs: https://glyphsapp.com/

Note: To enable icons/glyphs (https://www.nerdfonts.com/) on spacevim and on iTerm, I think that powerline or the font chosen on the iterm profile should be patched in order to add icons to it.

### Linux

### Windows

## Apps and Tools

* ansible: pip install ansible
* ansible-lint: pip install ansible-lint
* dbeaver
* discord
* docker
* envcahin: https://github.com/sorah/envchain
* filezilla
* gitter
* go
* jq: brew install jq
* kops (with brew the latest version and manually specific version)
* kubectl (with brew the latest version and manually specific version)
* kubectx
* kubens
* kubetail
* kubetcl krew (kubectl plugin manager)
* helm (with brew the latest version and manually specific version)
* filezilla
* flux (cli)
* nvm
  * node
  * npm
* python3
  * pip3
    * pipenv (with pip3)
* sdkman: https://sdkman.io/
  * Java
  * Maven
  * Gradle
* slack
* tfenv (brew install tfenv)
  * terraform
* vscode
