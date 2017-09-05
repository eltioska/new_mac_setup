[home](index.md)

### Services

- Alfred
- Bartender
- BetterTouch Tool
- f.lux
- ~~Caffeine~~ Amphetamine
- Calendar 2
- Cheatsheet
- cdto
- [New File Menu](http://langui.net/new-file-menu/)

- Dropbox
- Insync
- VPN

- Mackup? (syncs settings to Dropbox)

#### Alfred:
 - set shortcut key
 - shortcut keys for snippets & clipboard
 - set theme
 - snippets
 - workflows:
   - VirtualBox
   - Shortcut keys(?)

### Utilities

- AppCleaner
- CCleaner
- DiskWave
- Media Info
- PDF Toolbox
- Fluid
- Desktop Utility
- Name Changer
- The Unarchiver
- Default Folder X


### Note-Taking Apps
- Evernote
- Simplenote / NV-Alt
- Mou / MacDown


### Using Homebrew:

#### List of all commands to install one by one:
```
brew cask install alfred
brew cask install bartender
brew cask install bettertouchtool
brew cask install flux
brew cask install cheatsheet
brew cask install cd-to

brew cask install dropbox
brew cask install insync
brew cask install windscribe
brew cask install tigervpn
 
brew cask install appcleaner
brew cask install ccleaner
brew cask install diskwave
brew cask install mediainfo
brew cask install pdf-toolbox
brew cask install fluid
brew cask install desktoputility
brew cask install namechanger
brew cask install the-unarchiver
brew cask install default-folder-x
 
brew cask install evernote 
brew cask install simplenote 
brew cask install nvalt 
brew cask install mou 
brew cask install macdown
```

#### Otherwise create a Brewfile with something like this:

```
tap 'caskroom/cask'

cask 'alfred'
cask 'bartender'
cask 'bettertouchtool'
cask 'flux'
cask 'cheatsheet'
cask 'cd-to'
cask 'dropbox'
cask 'insync'
cask 'windscribe'
cask 'tigervpn'
cask 'appcleaner'
cask 'ccleaner'
cask 'diskwave'
cask 'mediainfo'
cask 'pdf-toolbox'
cask 'desktoputility'
cask 'namechanger'
cask 'the-unarchiver'
cask 'default-folder-x'
cask 'evernote'
cask 'simplenote'
cask 'nvalt'
cask 'mou'
```

And then run: 

```
brew bundle install
```

to install them all at one go.
