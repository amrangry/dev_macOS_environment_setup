# Table of content
- [x] [How to use macOS Recovery](How-to-use-macOS-Recovery!)
- [x] [The Quickest Way to Show/Hide Hidden Files](The-Quickest-Way-to-Show|Hide-Hidden-Files)
- [x] [Prevent Future .DS_Store Files (Optional)](Prevent-Future-.DS_Store-Files-(Optional))
- [x] [Modify text files via terminal](Modify-text-files-via-terminal)
- [x] [Modify text files via Nano](Modify-text-files-via-Nano)



## **How to use macOS Recovery!**

🔗 [Apple Support – macOS Recovery](https://support.apple.com/en-eg/HT204904) : 🛠 https://support.apple.com/en-eg/HT204904

| **Shortcut**                     | **Function** |
|-----------------------------------|-------------|
| **Command (⌘) + R**               | Install the latest macOS that was installed on your Mac (without upgrading). |
| **Option (⌥) + Command (⌘) + R**  | Upgrade to the latest macOS compatible with your Mac. |
| **Shift (⇧) + Option (⌥) + Command (⌘) + R** | (Requires macOS Sierra 10.12.4 or later) Install the macOS that came with your Mac, or the closest available version. |

## **The Quickest Way to Show|Hide Hidden Files**

👀 Since the release of macOS Sierra, when in Finder, it is now possible to use the shortcut:

```ruby
 CMD + SHIFT + .
```

## **Prevent Future .DS_Store Files (Optional)**
For macOS, run this command to stop creating .DS_Store files on network drives:

```bash
defaults write com.apple.desktopservices DSDontWriteNetworkStores true
```

## **Modify text files via terminal** 📝 

#### 1 - Open a File for Editing
```ruby
* Open File for edit
 $ vi filepath
```

#### 2 - Basic Modes in vi Editor
| **Mode**          | **Shortcut**                        |
|-------------------|-------------------------------------|
| **Insert Mode**   | Press i to enter insert mode.       |
| **Command Mode**  | Press Esc to return to command mode.|
	
	
#### 3 - Ex Mode (Command Line Mode)
To enter command mode, press Esc, then type : (colon).
> The cursor will go to the bottom of the screen at a colon prompt. to write your command

Common commands:
``` bash
:w      # Save file
:q      # Quit
:wq     # Save and quit
:wq!    # Force save and quit
:q!     # Quit without saving
ZZ      # Save and exit (shortcut)

```

## **Modify text files via Nano** 📝 
Press Ctrl + O to write (save) the file.
Nano will ask for a file name. Just press Enter to confirm (it will save to the same file).
After saving, press Ctrl + X to exit Nano.
