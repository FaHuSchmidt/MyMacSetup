# MyMacSetup

## Basics

### [Homebrew](https://brew.sh/)

Package manager for macOS.

#### Setup

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```  
#### Usages

```
# update homebrew
brew update
# update packages
brew upgrade
# update package (e.g. node)
brew upgrade node
# search
brew search docker
```

## Terminal

The default mac terminal app could be replaced by a way more powerful combination of [iTerm](https://www.iterm2.com), [ZSH](http://www.zsh.org/) and [Oh-my-zsh](https://ohmyz.sh/), with more features, plugins and themes.

https://www.howtogeek.com/362409/what-is-zsh-and-why-should-you-use-it-instead-of-bash/

### [iTerm](https://www.iterm2.com)

Replacement for default terminal app with more features.

#### Setup

```
brew cask install iterm2
```

#### Color Preset

Download color preset ("save as.." → *.itemcolors): [Solarized Dark - Patched](https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/Solarized%20Dark%20-%20Patched.itermcolors)

iTerm → Preferences → Profiles → Colors → Color Presets... → Import... → select downloaded file

Select imported Color Preset.

Every color preset from this page could be used: https://iterm2colorschemes.com/

### [ZSH](http://www.zsh.org/)

#### Setup

```
brew install zsh
```

### [Oh-my-zsh](https://ohmyz.sh/)

#### Setup

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Add some aliases to handle ZSH config

```
echo 'alias zshconfig="vi ~/.zshrc"' >> ~/.zshrc
echo 'alias zshrefresh="source ~/.zshrc"' >> ~/.zshrc
```

Reload ZSH config

```
source ~/.zshrc
```

Now "zshconfig" opens ZSH config file with vi and "zshrefresh" reloads ZSH config.
If you don't like vi for editing, replace it with your favourite editor. You could also shorten aliases, e.g. "zshc" and "zshr" if you want to.

###### Setup theme

[Powerlevel9k](https://github.com/bhilburn/powerlevel9k)
```
git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
zshconfig

# select theme and customize prompt by edit
# ZSH_THEME="powerlevel9k/powerlevel9k"

# ... and adding:
# POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(vcs dir rbenv)
# POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(root_indicator background_jobs status load)

# reload zsh config
zshrefresh
```

###### Setup font for theme

The theme [Powerlevel9k](https://github.com/bhilburn/powerlevel9k) uses icons whicht have to provided by a font. Otherwise there would be a lot of ugly question marks and so on.

Download Font [Source Code Pro for Powerline](https://github.com/powerline/fonts/blob/master/SourceCodePro/Source%20Code%20Pro%20for%20Powerline.otf)

Open the downloaded font and press "Install Font".

Set font in iTerm2 with 14px size (iTerm → Preferences → Profiles → Text → Change Font).

Restart iTerm2.

###### Set default terminal directory

Preferences → Profiles → General → Working Directory

###### Activate plugins

Plugin wiki page: https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins
```
zshconfig
```
Type "/plugin" (without quotes)

| plugin | comment |
| --- | --- |
| **brew** | alias "brews" |
| **docker** | autocomplete |
| **git** | autocomplete, [aliases](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugin:git#aliases) |
| git-flow |  |
| jira | https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins#jira |
| ng | https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins/ng |
| npm | autocomplete |
| osx | [aliases](https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins/osx#commands) |
| phing | autocomplete |
| yarn | autocomplete |

### How to use with PHPStorm

Preferences → Tools → Terminal → Shell Path → "/bin/zsh"

## Container

### [Lando](https://docs.devwithlando.io/) and [Docker](https://www.docker.com/)

#### Setup

For a fresh setup remove Lando and Docker by executing uninstall script from Lando:
https://docs.devwithlando.io/installation/uninstalling.html#macos

```
brew cask install lando
```

Installs Lando and Docker for Mac.

Verify Lando installation

```
lando version
```

Start Docker for Mac to finish setup.

Verify Docker installation

```
docker -v
docker-compose -v
```

### PHP

Install a base PHP for installers, phing, etc.

```
brew install php

# add php to zsh path variable
# replace "php@7.3" with your version
echo 'export PATH="/usr/local/opt/php@7.3/bin:$PATH"' >> ~/.zshrc
echo 'export PATH="/usr/local/opt/php@7.3/sbin:$PATH"' >> ~/.zshrc

# reload zsh config
zshrefresh

# verify php version
php -v

```

#### Composer

```
brew install composer

# add composer to zsh path variable
echo 'export PATH="/usr/local/opt/composer/bin:$PATH"' >> ~/.zshrc

# reload zsh config
zshrefresh

# verify composer version
composer -V

```

#### Extensions
```
pecl install memcached
```

[Search packages](https://pecl.php.net/package-search.php)
[Browse packages](https://pecl.php.net/packages.php)

## Apps

### [Google Chrome](https://www.google.de/chrome)

```
brew cask install google-chrome
```

### [Google Cloud SDK](https://cloud.google.com/sdk)

```
brew cask install google-cloud-sdk
```

### WIP

just a list of apps which may be useful

```
brew cask install whatsapp
brew cask install telegram
brew cask install visual-studio-code
brew cask install sourcetree
brew cask install phpstorm
```

FileZilla

https://filezilla-project.org/download.php?type=client

Creative Cloud

https://www.adobe.com/de/creativecloud/catalog/desktop.html

Sequel Pro

https://sequelpro.com/download
