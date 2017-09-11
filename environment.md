[home](index.md)

### Environment & Terminal

#### Bash
_Install & activate updated bash_
- check bash version:
```
echo $BASH_VERSION
```
- Install via homebrew:
```
brew install bash
```
- homebrew installs the updated bash into `usr/local/bin/bash`

- add the new bash to the list of legit shells (but for the current user, not for root):
```
sudo bash -c "echo $(brew --prefix)/bin/bash >> /private/etc/shells"
```
`#(brew --prefix)` is usually `usr/local/bin` but using the variable is safer

- check:
```
cd /etc
cat shells

cd /private/etc
cat shells
```
the last line should read
```
/usr/local/bin/bash
```
- change the shell for the user
```
chsh -s /usr/local/bin/bash
```
- _If you go to System Preferences > Users & Groups > User > click the lock to make changes_
  _ right click on the user name & choose "Advanced", the login shell for the user should now read /usr/local/bin/bash_

- Restart terminal.app (new window works too) or iTerm

- Check for Bash 4 and /usr/local/bin/bash...
```
echo $BASH && echo $BASH_VERSION
```

#### Git


#### Terminal
 - iTerm2 
 
  `brew cask install iterm2`

 - Fonts 
 
  ```
  # enable "tap":
  brew tap caskroom/fonts
  
  # install the fonts
  brew cask install font-source-code-pro
  brew cask install font-anonymous-pro
  brew cask install font-hack
  ```

- Configure iTerm2

#### Dotfiles
