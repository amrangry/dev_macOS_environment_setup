

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


## **Author**

<div align="center">
  <img src="https://avatars.githubusercontent.com/u/2900952?s=400&u=41c504ca200e2f92638fc630e8361da78296b35c&v=4" width="180" alt="Amr Ahmed Elghadban"/>

  **Amr Ahmed Elghadban (AmrAngry)**

[![Email](https://img.shields.io/badge/Email-Contact%20Me-red?logo=gmail)](mailto:amr.elghadban@gmail.com) [![WhatsApp](https://img.shields.io/badge/GitHub-Profile-blue?logo=whatsapp)](https://api.whatsapp.com/send/?phone=00971543233227&text=Hi%20&app_absent=0) [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/amrelghadban/)

[![GitHub](https://img.shields.io/badge/GitHub-Profile-blue?logo=github)](https://github.com/amrangry) [![StackOverflow](https://img.shields.io/badge/StackOverflow-Profile-orange?logo=stackoverflow)](https://stackoverflow.com/users/1316779/amrangry)

[![Twitter (formerly Twitter)](https://img.shields.io/badge/Twitter-Profile-blue?logo=twitter)](https://x.com/intent/follow?screen_name=amr_elghadban) [![Facebook](https://img.shields.io/badge/Facebook-Profile-blue?logo=facebook)](https://facebook.com/amr.elghadban) [![Website](https://img.shields.io/badge/Website-Visit%20Me-blue?logo=globe)](https://amrangry.github.io/)
       <div align="center" >
	       <a href = "https://www.buymeacoffee.com/amrangry">
		    <img src = "https://img.buymeacoffee.com/button-api/?text=Buy%20me%20a%20coffee&emoji=&slug=your-username&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff"/>
                </a>
       </div>
  <!--  [![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support%20Me-yellow?logo=buymeacoffee)](https://www.buymeacoffee.com/amrangry) -->
  <!--  [Email](mailto:amr.elghadban@gmail.com?subject=I%20checked%20your%20GitHub%20repo!): [amr.elghadban@gmail.com](mailto:amr.elghadban@gmail.com) -->
  <!-- [![Linkedin](https://img.shields.io/badge/Lets%20Connect%20via-LinkedIn-blue)](https://www.linkedin.com/in/amrelghadban/) -->
  <!-- [![X (formerly Twitter) Follow](https://img.shields.io/twitter/follow/amr_elghadban)](https://x.com/intent/follow?screen_name=amr_elghadban) -->
  
</div>

## **Contributing 🤘**

All your feedback and help to improve this project is very welcome. 
Please create issues for your bugs, ideas and enhancement requests, or better yet, contribute directly by creating a PR. 😎

When reporting an issue, please add a detailed instruction, and if possible a code snippet or test that can be used as a reproducer of your problem. 💥

When creating a pull request, please adhere to the current coding style where possible, and create tests with your code so it keeps providing an awesome test coverage level 💪


## **Code of Conduct**

I’m here to share my knowledge and findings as I work every day to improve our apps/demos for the community.

This is a space where we work together, openly and safely, as kind and considerate human beings.

We grow by giving and receiving positive, constructive feedback.
 
Let’s keep learning and building, one step at a time.


## **License**

<details>
<summary>MIT License.</summary>
Distributed under MIT License.
Copyright 2025 Amr Elghadban
</details>
