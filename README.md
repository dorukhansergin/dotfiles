# dotfiles
## Goal
I started this as dotfiles but it rather became an instructions list to restart an entire working OS if I ever have to. I hope you find something useful for your own system.
### MacOs
At the very least, a fresh MacOs should be equipped with the following (checkmark shows that an installing procedure is already implemented)
- [x] __Homebrew__ to easily install stuff
- [x] A decent, modern, minimalist __Shell__
  - [x] `zsh` as the shell (installed with brew)
  - [x] [prezto](https://github.com/sorin-ionescu/prezto) as the configuration framework for `zsh`
  - [x] [prezto-contrib](https://github.com/belak/prezto-contrib) to enhance prezto
  - [x] [Powerline fonts](https://github.com/powerline/fonts)
  - [x] [spaceship](https://denysdovhan.com/spaceship-prompt/) as prompt
  - [x] [iTerm2](https://www.iterm2.com/) as terminal replacement with a dynamic profile imported
- [x] `conda`: miniconda3 (preferred) or anaconda3
  - [x] conda base should be the default python executable
  - [x] conda completion
- [x] `Visual Studio Code` as general-purpose, extensible, free editor
  - [x] Plugins
- [x] `docker`
- [x] Brave Browser. I like this browser because it's privacy oriented, open source and chromium os so that certain plugins work.
  - [ ] Load bookmarks
  - [ ] Load plugins
- [x] Alfred4
  - [ ] Workflows
    - [ ] Scientific Article Search and BibTex copy to clipboard
    - [ ] Stack Overflow
    - [ ] Brave Bookmarks [Acidham/chromium-hist-bookmarks](https://github.com/Acidham/chromium-hist-bookmarks)

## Prerequisites
### MacOS
1. Install XCode
2. Install XCode Command Line Tools

At this point, you should have git and ruby installed already. To check
```shell
git --version
ruby --version
```

## Installation Guide
### MacOS
- Install homebrew
```
./homebrew/install
```
- Install `zsh`
```
./shell/install_zsh
```
- Clone `prezto`. Note that this will install [my own fork of the repo](https://github.com/dorukhansergin/prezto). If you decide to go with the original, you need to figure out your own configuration of `.zpreztorc` for the next two steps.
```
./shell/clone_prezto
```
- Clone `prezto-contrib`
```
./shell/clone_prezto_contrib
```
- Install `powerline fonts`. At this point, `spaceship` theme should already be working. You still need to adjust your terminal application fonts, though. I automate this process for myself with iTerm2 in the following step.
```
./shell/install_powerline_macos
```
- Install iTerm2
```
brew cask install iterm2
```
- (optional but recommended) Import `shell/Default.json` to iTerm2 by following `Profiles-> Open Profiles..-> Edit Profiles..-> Other Actions..-> Import JSON Profiles..`
- Install miniconda3 (optionally, you can execute the other installer in the same folder for anaconda3)
```
./conda/install_miniconda3_macos
```
- Go to [project webiste](https://code.visualstudio.com/) and download the latest stable version of VS Code
- Run `./vscode/install_extensions` to batch install the useful extensions
- Run the following to install Docker
```
brew cask install docker
```
- Install Brave Browser
```
brew cask install brave-browser
```
- Install Alfred4
```
brew cask install alfred
```

## TODOs
- [ ] Sync `vscode` settings via [Settings Sync] to a github gist
- [ ] Learn how to write your own Alfred workflows (heck even buy the powerpack)
- [ ] Find a way to automatically install favorite Brave Browser plugins
- [ ] Write aliases and functions for fast setup of `mltooling-workspace`

