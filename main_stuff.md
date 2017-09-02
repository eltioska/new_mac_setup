[home](index.md)

## Main Stuff
- [Update & New Admin](#update-new-admin)
- [Configure User Account](#configure-user-account)
- [Configure Security](#configure-security)
- [Backups](#backups)
- [Setting Up For Development](#setting-up-for-development)

### Update & New Admin
- Log in, run Software Update & restart again.
- Log in again & create a new admin account & use this one from now on.


### Configure User Account

#### Trackpad
- _System Preferences > Trackpad > Tap to click_
- _System Preferences > Accessibility > Mouse & Trackpad > Trackpad Options > Enable Dragging  & Three-finger Drag_

#### Keyboard
- _System Preferences > Keyboard > Keyboard > Use F1, F2 etc as standard function keys_
- _System Preferences > Keyboard > Keyboard > Modifier Keys > remap Caps to Ctrl_
- _System Preferences > Keyboard > Shortcuts > ..._

#### Safari Browser
- _Safari > Preferences > General_ & deselect _Open safe files after downloading_.
- _Safari > Preferences > Passwords_ & switch off password setting
- _Safari > View > Status Bar_

#### Dock
- Set auto-hide

#### Finder
- show the Library Folder: `chflags nohidden ~/Library`
- show hidden files: `defaults write com.apple.finder AppleShowAllFiles YES`
- show the path bar: `defaults write com.apple.finder ShowPathbar -bool true`
- show the status bar: `defaults write com.apple.finder ShowStatusBar -bool true`
- show full path in title bar: `defaults write com.apple.finder _FXShowPosixPathInTitle -bool true`
- disable creation of DS_Store files on network volumes and USB drives: 
  - `defaults write com.apple.desktopservices DSDontWriteNetworkStores -bool true`
  - `defaults write com.apple.desktopservices DSDontWriteUSBStores -bool true`
- Enable unsigned programs flag in Gatekeeper _(If open, quit System Preferences first)_:
  - `sudo spctl --master-disable`

#### Change Screenshots Folder
- `defaults write com.apple.screencapture location` _ADD A SPACE AFTER THIS_, open the file in Finder and drag the folder you want over to Terminal (which will insert the file path of the folder), or enter the location yourself.
- hit Enter on your keyboard, then type in `killall SystemUIServer`
- press Enter again and you're done.

### Configure Security
- _System Preferences > Security & Privacy > FileVault_ & turn FileVault on
- _#ToDO:_ Set up Anti-Virus (Sophos / Avira ?)

### Backups
- _#ToDO:_ Time Machine
- _#ToDO:_ SuperDuper! (consider Carbon Copy Cloner coz of recovery partition)
- Synology:
  - [Downloads Page](https://www.synology.com/en-global/support/download/DS214se#utilities)
  - CloudStation Drive
  - Hyper Backup Explorer (_#ToDo_)

### Other
- Disable auto-correct (e.g. it's annoying on skype)
  - `defaults write -g NSAutomaticSpellingCorrectionEnabled -bool false`


### Setting Up For Development

#### XCode & Command Line Tools
- AppStore > search for XCode & install
- Open terminal & run:
 `xcode-select --install`
 & accept the licence
 - Run XCode once (from the Launcher) and accept the licence
 

#### Homebrew
- set up [Homebrew](https://brew.sh)
- _no need to update the PATH since Homebrew now installs in /usr/local/_
- check that Homebrew is installed correctly: `brew doctor`
- update the index of available packages: `brew update`
- _Note re path order: can also insert `/usr/local/bin` to the first line of `/private/etc/paths` and reboot in order to change the global paths loading order. Admin password may be required if you modify the file._
- just in case: to set up Homebrew Cask: `brew cask` and then `brew cask list` (can do `brew tap cask` instead?)

