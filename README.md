#Developer Workstation Toolset for Mac OS X

This repo is a set of tools to convert our Mac in a complete Developer Workstation. Complete list of software installed is inside MacOSX.yml playbook.

We are using ansible to manage installation of AppStore, Homebrew and Cask packages.

##Install homebrew, cask, git & ansible

First you MUST to have basic tools: homebrew, cask, git & ansible.

Open a terminal and execute these commands:

### Install command-line tools only not fully XCode
```
xcode-select —install
```

### Install homebrew
Homebrew is like apt for Ubuntu. A lot of terminal tools are ready to install.

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”

sudo chown -R $(whoami) /usr/local

brew doctor
```

### Install Cask
Cask is a Homebrew extension that allow us to install non-terminal software.

```
brew tap caskroom/cask
brew install brew-cask
```

### Install git
Git is a Control Version Software. We need it to be sure that we have last version of **Baldrick** repo.

```
brew install git
```

### Install ansible
Ansible is a continuous integration tools that allow us to install software packages in several hosts. For this project we use always **localhost**... by the moment ;)

```
brew install ansible
```

### Download Baldrick repo
Download last version of this repo.

```
git clone git@github.com:corretgecom/baldrick.git
```

## Enjoy it
Now you have all you need. Execute it with command:

``` 
ansible-playbook MacOSX.yml --ask-become-pass
````

Depending your connection bandwith and sudo caducity period, you will be asked again for your password.

