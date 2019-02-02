# MyMacSetup

## [Homebrew](https://brew.sh/)

### Setup

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```  
### Usages

```
# update homebrew
brew update
# update packages
brew upgrade
# update package (e.g. node)
brew upgrade node
```

## [iTerm](https://www.iterm2.com)

### Setup

```
brew cask install iterm2
```  
## ZSH

### Setup

```
brew install zsh
```

## [Oh-my-zsh](https://ohmyz.sh/)

### Setup

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

#### Setup theme

[Powerlevel9k](https://github.com/bhilburn/powerlevel9k)
```
git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
vi ~/.zshrc
# select theme and customize prompt by editing/adding
# ZSH_THEME="powerlevel9k/powerlevel9k"
# POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(vcs dir rbenv)
# POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(root_indicator background_jobs status load)
# reload .zshrc
source ~/.zshrc
```

#### Setup font for theme

Download Font [Source Code Pro for Powerline](https://github.com/powerline/fonts/blob/master/SourceCodePro/Source%20Code%20Pro%20for%20Powerline.otf)

Open the downloaded font and press "Install Font".

Set font in iTerm2 with 14px size (iTerm → Preferences → Profiles → Text → Change Font).

Restart iTerm2.

#### Set default terminal directory

Preferences → Profiles → General → Working Directory

#### Activate plugins

Plugin wiki page: https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins
```
vi ~/.zshrc
```
Type "/plugin" (without quotes)

| plugin | comment |
| --- | --- |
| **brew** | autocomplete, alias "brews" |
| **docker** | autocomplete |
| **git** | autocomplete, [aliases](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugin:git#aliases) |
| git-flow |  |
| jira | https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins#jira |
| ng | https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins/ng |
| npm | autocomplete |
| osx | [aliases](https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins/osx#commands) |
| phing | autocomplete |
| yarn | autocomplete |

# Archive

## Apps

Chrome

https://www.google.de/chrome

Git

https://git-scm.com/downloads

CleanMyDrive

http://macpaw.com/cleanmydrive

Dropbox

https://www.dropbox.com/install

Google Drive

https://www.google.com/intl/de_ALL/drive/download/

iTerm2

https://www.iterm2.com/downloads.html

Oh My Zsh

http://ohmyz.sh/

Textmate

http://macromates.com/download

Docker
https://www.docker.com/

FileZilla

https://filezilla-project.org/download.php?type=client

PhpStorm

https://www.jetbrains.com/phpstorm/download/

Creative Cloud

https://www.adobe.com/de/creativecloud/catalog/desktop.html

Source Tree

https://www.sourcetreeapp.com/

Sequel Pro

https://sequelpro.com/download

Vlc
http://www.videolan.org/vlc/download-macosx.html

JDownloader

http://jdownloader.org/download/index

Skype

https://www.skype.com/de/download-skype/skype-for-mac/

XnView MP

http://www.xnview.com/de/xnviewmp/

Firefox

https://www.mozilla.org/de/firefox/new/

Ukelele
http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=ukelele

Droplr

https://droplr.com/apps

Max! Smart Home
http://www.eq-3.de/service/downloads.html

Sweet Home 3D

http://www.sweethome3d.com/de/download.jsp

iSyncer

http://www.isyncer.de/de

## Tipps

OSX Essentials

Open App Store, search "essentials" and install Numbers, Pages, Keynote, etc. if needed. 

Show Hidden Files

In any Open or Save dialog in OS X, simply press Shift-Command-Period to display hidden files and folders.
