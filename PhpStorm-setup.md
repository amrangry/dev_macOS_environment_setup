- [x] **🛠 PhpStorm CLI Setup on macOS** 
  >To open PhpStorm from the terminal using the phpstorm command:
  1. Add PhpStorm to Your PATH by edit your shell config file (.zshrc for zsh users):
   ```Terminal
     open -e ~/.zshrc
   ```
  2. Then add the following line at the end of the file:
    ```Terminal
     export PATH="/Applications/PhpStorm.app/Contents/MacOS:$PATH"
   ```
  3. Apply the Changes (In the terminal, reload the config):
    ```Terminal
     source ~/.zshrc
   ```
  4. Test the Command (Navigate to any project folder and run):
    ```Terminal
     phpstorm .
   ```
