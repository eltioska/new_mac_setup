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
 -- colour presets: start with "Solarized (Dark)" colour preset and reset foreground colour to #c7c7c7
 -- set font to Source Code Pro Light 18px
 -- set window blur & transparency


#### Dotfiles

- In the home directory '/Users/<username>' create a bash profile:

```
touch .bash_profile
``` 

_This will be empty except for a reference to load .bashrc. Contents of the file:_
```
# Load .bashrc if it exists
test -f ~/.bashrc && source ~/.bashrc
```

- Create a bashrc file:

```
touch .bashrc
``` 

_This will be empty except for references to load the environment variables, aliases, customised prompt, useful functions, and config for python virtualenvs. Contents of the file:_

```
# Load .env if it exists
test -f ~/dotfiles/.env && source ~/dotfiles/.env

# Load .aliases if it exists
test -f ~/dotfiles/.aliases && source ~/dotfiles/.aliases

# Load .prompt if it exists
test -f ~/dotfiles/.prompt && source ~/dotfiles/.prompt

# Load .functions if it exists
test -f ~/dotfiles/.functions && source ~/dotfiles/.functions

# Load .venvsconf if it exists
test -f ~/dotfiles/.venvsconf && source ~/dotfiles/.venvsconf

```

- dotfiles folder:
 -- Create the folder: `mkdir dotfiles`
 -- Create the files in this folder:
 
 ```
 touch .env
 touch .aliases
 touch .prompt
 touch .functions
 touch .venvsconf
 ```
 
 ### Install hombrew bash completion:
 
```
brew install bash-completion
```
And add the following to `/dotfiles/.env` file:
```
# Add tab completion for many Bash commands
[ -f /usr/local/etc/bash_completion ] && . /usr/local/etc/bash_completion
```

### Terminal Tools
 - tree: __tree__ is a recursive directory listing command that produces a depth indented listing of files. 
 ```
 brew install tree
 ```
