# TODO List - xCode Setup
- [ ] [Enable spell-checking in Xcode](Enable-spell-checking-in-Xcode)
- [ ] [Xcode Behaviors](Xcode-Behaviors)
- [x] [Xcode Command Line Tools](Xcode-Command-line-Tools)
- [x] [Upgrade Your Unsupported iOS Devices](Upgrade-Your-Unsupported-Mac)

## Enable Spell-checking in Xcode
You can enable this feature by going to the **Edit** menu > **Format** > **Spelling and Grammar** > **Check Spelling While Typing**.
[Reference](https://sarunw.com/posts/spell-checking-in-xcode)

## Xcode Behaviors
1. Download the Supported Scripts from [Here](https://github.com/amrangry/dev_macOS_environment_setup/tree/master/xCode%20Behavior%20Scripts).
2. Open Xcode.
3. Open the Xcode preferences (Shortcut: `cmd`).
4. Select the **Behaviors** tab.
5. Press the **+** button at the bottom left.
6. Create a name for the behavior (e.g., `Open Terminal`).
7. Activate the **Run** checkbox.
8. Click **Choose Script**.
9. Right-click the name of the behavior you just created to assign a shortcut (e.g., `cmd + shift + 5`).

**Note**:  
To create a bash executable file, run the following:
```bash
$ echo '#!/bin/bash\nopen -a Terminal "`pwd`"' > ~/terminal.sh && chmod +x ~/terminal.sh
```

## Xcode Command-line Tools
Install the tools using the following command:
```ruby
$ xcode-select --install
```

## Upgrade Your Unsupported Mac
1. Upgrade Your Unsupported Mac To macOS Ventura [Watch Video](https://www.youtube.com/watch?v=SSjkLO8BA2o)
2. Adding files for unsupported iOS Devices: [GitHub Repository](https://github.com/filsv/iOSDeviceSupport)
