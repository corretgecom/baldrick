#Install homebrew &cask, git & ansible

Open a terminal and execute these commands:


- [ ] xcode-select —install
- [ ] ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”
- [ ] sudo chown -R $(whoami) /usr/local
- [ ] brew doctor
- [ ] brew tap caskroom/cask
- [ ] brew install brew-cask
- [ ] brew install git
- [ ] brew install ansible

Download Baldrick repo
```
git clone baldrick
```

Then, execute the playbook

``` 
ansible-playbook MacOSX.yml --ask-become-pass
````


