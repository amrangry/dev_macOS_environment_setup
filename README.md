

<p align="center">
  <img src ="https://github.com/amrangry/dev_macOS_environment_setup/blob/main/GFX_ASSETS/dev_tools.jpg?raw=true"/>
</p>



-  Package manager for macOS
  - [x] [Homebrew](https://brew.sh/)
  - [ ] [macports](https://www.macports.org/install.php)
  - [x] Ruby version manager [rbenv](https://github.com/rbenv/rbenv)
-  Terminal Enhancements
  - [x] [Z Shell](https://ohmyz.sh/)
-  Command Line
  - [x] [xCode Command Line ]() ``` x code-select --install ```` 
-  Package Managers for Programming Languages
  - [x][cocoapods](https://guides.cocoapods.org/using/getting-started.html)
-  Text Editors
  - [x] [Sublime Download](https://www.sublimetext.com/download_thanks?target=mac)
- [x] [SSH Setup for Business GitHub vs Personal Account](https://github.com/amrangry/dev_macOS_environment_setup/blob/main/SSH%20Setup%20for%20Business%20GitHub%20vs%20Personal%20Account.md)
  


# 0. Mac OS
   Upgrade Your Unsupported Mac To macOS Ventura https://www.youtube.com/watch?v=SSjkLO8BA2o
# 1. Setup Xcode
 ## 1-1 Enable spell-checking in Xcode
You can enable this feature by going to Edit menu > Format > Spelling and Grammar > Check Spelling While Typing.
Ref: https://sarunw.com/posts/spell-checking-in-xcode
## 1-2 Adding files for unsupported iOS Devices 
https://github.com/filsv/iOSDeviceSupport?

# 2. Xcode-Behaviors
1. Download the Supported Scripts. https://github.com/amrangry/dev_macOS_environment_setup/tree/master/xCode%20Behavior%20Scripts
3. Open Xcode.
4. Open the Xcode preferences. Shortcuts: cmd,
5. Select the behaviors tab.
6. Press the + button on the bottom left.
7. Create a name for the behavior. (ex. open terminal)
8. Activate the Run check box.
9. Click choose script.
10. Right-click the name of the behavior you just created to specify the shortcut. (ex. cmd + shift + 5)

Note: 
```ruby
- how to create bash executable file  
  $ echo '#!/bin/bash\nopen -a Terminal "`pwd`"' > ~/terminal.sh && chmod +x ~/terminal.sh
```

# 3. Oh My Zsh
Supercharge your terminal with styles, plugins and features! Since Apple replaced Bash with Zsh in 2019 and it installs with a single shell command, this is a no-brainer. You can pick from a boatload of themes — or just use the default one like me, it’s plenty good!

Basically if you ever saw someone using a fancy terminal, chances are that he was using Oh My Zsh.

<p align="center">
  <img src ="https://github.com/amrangry/dev_macOS_environment_setup/blob/main/GFX_ASSETS/oh_my_zch.jpg?raw=true"/>
</p>

Plugins are also a huge part of the Oh My Zsh ecosystem. My must haves are:

git for displaying what branch I'm on + if there are any changes
wd - shorthand for warp directory allows you to set up warp points in your file system and then jump to them from anywhere!
If nothing else, this will prettify your Terminal — and who doesn’t want that?! Get Oh My Zsh now!



#### How to use macOS Recovery
https://support.apple.com/en-eg/HT204904


Command (⌘)-R
Install the latest macOS that was installed on your Mac, without upgrading to a later version.*
Option-Command-R
Upgrade to the latest macOS that is compatible with your Mac.**
Shift-Option-Command-R
Requires macOS Sierra 10.12.4 or later	Install the macOS that came with your Mac, or the version closest to it that is still available. 

# The Quickest Way to Show/Hide Hidden Files
Since the release of macOS Sierra, when in Finder, it is now possible to use the shortcut:
```ruby
 CMD + SHIFT + .
```
# Terminal
```ruby
  pwd to print the current path
```

# Xcode Command-line Tools
```ruby
$ xcode-select --install
```

# Modify text files in Terminal
```ruby
* Open File for edit
 $ vi filepath
 
* Input mode

 press i to enter the insert mode 
 press q coomand 
 
* Ex mode
To get into it, press Esc and then : (the colon).
 The cursor will go to the bottom of the screen at a colon prompt.
 Write your file by entering :w 
 and quit by entering :q
 You can combine these to save and exit by entering :wq
 However, if you're finished with your file, it's generally more convenient to type Shift-z-z from command mode
 write 
 :wq!   --> write and quite 
 :q!   quite without saving 
```

#Repo clone from GitHup [Stackoverflow](https://stackoverflow.com/questions/68775869/message-support-for-password-authentication-was-removed)
## Just simply follow these steps:
- Create Personal Access Token on GitHub
  - [x] Go to this [link](https://github.com/settings/tokens) or From your GitHub account, go to Settings → Developer Settings → Personal Access Token → Tokens (classic) → Generate New Token (Give your password) → click Generate token → Copy the generated Token, it will be something like [ghp_sFhFsSHhTzMDreGRLjmks4Tzuzgthdvfsrta]
   [(don't go to repository setting; it's your profile setting)]
  - [x] Generate a new token and copy-paste it somewhere safely.
  - [x] Now search for an app in your Mac, named Keychain Access.
  - [x] Search for github.com (if there are multiple GitHub logins then choose Kind: Internet password), double-click it.
  - [x] Click on show password, then enter your Mac's password and hit Enter.
  - [x] Past the token you generated in step 2 and click Save changes
Or 
  - [ ] Set Global config
 ```ruby
$ git config --global user.name "your_github_username"
$ git config --global user.email "your_github_email"
$ git config -l
 ```
  - [ ] Now cache the given record in your computer to remembers the token:
 ```ruby
$ git config --global credential.helper cache
 ```
  - [ ] If needed, anytime you can delete the cache record by:
 ```ruby
$ git config --global --unset credential.helper
$ git config --system --unset credential.helper
 ```

