# dev_macOS_environment_setup

<p align="center">
  <img src ="https://github.com/amrangry/dev_macOS_environment_setup/blob/master/GFX_ASSETS/dev_tools.jpg?raw=true"/>
</p>

# 1. Setup xCode
 ## 1- enable spell-checking in Xcode
You can enable this feature by going to Edit menu > Format > Spelling and Grammar > Check Spelling While Typing.
Ref: https://sarunw.com/posts/spell-checking-in-xcode

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
  <img src ="https://github.com/amrangry/dev_macOS_environment_setup/blob/master/GFX_ASSETS/oh_my_zch.jpg?raw=true"/>
</p>

Plugins are also a huge part of the Oh My Zsh ecosystem. My must haves are:

git for displaying what branch I'm on + if there are any changes
wd - shorthand for warp directory allows you to set up warp points in your file system and then jump to them from anywhere!
If nothing else, this will prettify your Terminal — and who doesn’t want that?! Get Oh My Zsh now!
