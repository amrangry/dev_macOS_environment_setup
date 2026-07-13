# CLI - Mac Development Environment Guide
**Platform:** macOS (Apple Silicon)  
**Purpose:** Standardized terminal configuration for React Native, PHP, WordPress, AI Development Tools, and IDE Launchers.

---

# Overview

This `.zshrc` configuration provides:

- PHP / Composer support
- Ruby & CocoaPods support
- Node.js version management (NVM)
- Android SDK support
- Java 17 support for React Native & Gradle
- IDE launchers (VS Code, Cursor, PhpStorm, Windsurf, Antigravity)
- Codex Desktop & CLI integration
- Developer productivity aliases

---

# Folder Structure

```text
.zshrc
├── Composer
├── Ruby
├── NVM
├── Android SDK
├── Java
├── IDE Launchers
├── Codex Function
├── Aliases
└── rbenv
```

---

# Composer

Provides access to globally installed Composer packages.

```bash
export PATH="$HOME/.composer/vendor/bin:$PATH"
```

### Verification

```bash
composer --version
```

---

# Ruby

Required for:

- CocoaPods
- Fastlane
- Ruby gems
- React Native iOS builds

```bash
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
```

### Verification

```bash
ruby -v
```

---

# Node Version Manager (NVM)

Allows switching between multiple Node.js versions.

```bash
export NVM_DIR="$HOME/.nvm"

[ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \
  . "/opt/homebrew/opt/nvm/nvm.sh"

[ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \
  . "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"
```

### Verification

```bash
nvm --version
node -v
npm -v
```

---

# Android SDK

Required for:

- Android Emulator
- adb
- React Native Android builds

```bash
export ANDROID_HOME="$HOME/Library/Android/sdk"

export PATH="$PATH:$ANDROID_HOME/emulator"
export PATH="$PATH:$ANDROID_HOME/platform-tools"
```

### Verification

```bash
adb version
emulator -version
```

---

# Java 17 for React Native / Gradle

Required by:

- Gradle
- Android Builds
- React Native

```bash
export JAVA_HOME="/opt/homebrew/opt/openjdk@17"
export PATH="$JAVA_HOME/bin:$PATH"
```

### Verification

```bash
java -version
javac -version
```

---

# Windsurf

AI-powered IDE from Codeium.

```bash
export PATH="/Users/amr.elghadban/.codeium/windsurf/bin:$PATH"
```

### Usage

```bash
surf .
```

or

```bash
windsurf .
```

---

# Antigravity

AI-powered development environment.

```bash
export PATH="/Users/amr.elghadban/.antigravity/antigravity/bin:$PATH"
```

### Usage

```bash
antigravity .
```

---

# Antigravity IDE

Standalone IDE launcher.

```bash
export PATH="/Users/amr.elghadban/.antigravity-ide/antigravity-ide/bin:$PATH"
```

### Usage

```bash
antigravity-ide .
```

---

# PhpStorm

JetBrains PHP IDE launcher.

```bash
export PATH="/Applications/PhpStorm.app/Contents/MacOS:$PATH"
```

### Usage

```bash
phpstorm .
```

---

# Codex Launcher

Custom launcher that supports both:

- Codex Desktop
- Codex CLI

---

## Desktop Mode

Open current folder in Codex Desktop.

```bash
codex
```

```bash
codex .
```

```bash
codex app .
```

---

## CLI Mode

Run Codex CLI.

```bash
codex cli
```

```bash
codex cli --help
```

```bash
codex cli generate
```

---

## Function Definition

```bash

# --------------------------------------------------
# Codex smart launcher (Desktop + CLI)
#
# Usage:
#   codex              → Open Codex Desktop (current dir)
#   codex .            → Open Codex Desktop (current dir)
#   codex app [path]   → Open Codex Desktop (optional path)
#
#   codex cli          → Run Codex CLI (current dir)
#   codex cli --help   → Codex CLI help
#   codex cli .        → Codex CLI scoped to dir
#
# Notes:
# - Defaults to Desktop when no mode is provided
# - Desktop and CLI are intentionally separated
# - Avoids conflicts with Codex CLI binary
# --------------------------------------------------

codex() {
  local mode="$1"
  local target

  if [[ "$mode" == "cli" || "$mode" == "app" ]]; then
    shift
  else
    mode="app"
  fi

  target="${1:-.}"

  case "$mode" in
    app)
      open -a "Codex" "$target"
      ;;
    cli)
      if command -v codex-cli >/dev/null 2>&1; then
        command codex-cli "$@"
      elif command -v codex >/dev/null 2>&1; then
        command codex "$@"
      else
        echo "Codex CLI not found in PATH"
        return 1
      fi
      ;;
  esac
}
```

---

# IDE Productivity Aliases

---

## Visual Studio Code

```bash
alias vs="code"
```

Usage:

```bash
vs .
```

---

## Cursor

```bash
alias cr="cursor"
```

Usage:

```bash
cr .
```

---

## PhpStorm

```bash
alias ps="phpstorm"
```

Usage:

```bash
ps .
```

---

## Windsurf

```bash
alias ws="surf"
alias windsurf="surf"
```

Usage:

```bash
ws .
```

or

```bash
windsurf .
```

---

## Antigravity

```bash
alias ag="antigravity"
```

Usage:

```bash
ag .
```

---

# Oh My Zsh Helpers

```bash
alias zshconfig="mate ~/.zshrc"
alias ohmyzsh="mate ~/.oh-my-zsh"
```

### Usage

Edit zsh configuration:

```bash
zshconfig
```

Open Oh My Zsh folder:

```bash
ohmyzsh
```

---

# rbenv

Used to manage Ruby versions.

```bash
eval "$(rbenv init - zsh)"
```

### Verification

```bash
rbenv versions
```

---

# Recommended Cleanup

Remove duplicate entries:

```bash
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
```

Keep only one copy.

---

```bash
export PATH="/Users/amr.elghadban/.antigravity-ide/antigravity-ide/bin:$PATH"
```

Keep only one copy.

---

# Frequently Used Commands

## Open Current Project

```bash
vs .
cr .
ps .
ws .
ag .
codex .
```

## Check Development Environment

```bash
node -v
npm -v
ruby -v
java -version
adb version
composer --version
```

## Reload Terminal Configuration

```bash
source ~/.zshrc
```

---

# Recommended Backup

Before making changes:

```bash
cp ~/.zshrc ~/.zshrc.backup
```

Restore if needed:

```bash
cp ~/.zshrc.backup ~/.zshrc
source ~/.zshrc
```

---


# backup snap for .zshrc

```bash


# User configuration

# export MANPATH="/usr/local/man:$MANPATH"

# You may need to manually set your language environment
# export LANG=en_US.UTF-8

# Preferred editor for local and remote sessions
# if [[ -n $SSH_CONNECTION ]]; then
#   export EDITOR='vim'
# else
#   export EDITOR='mvim'
# fi

# Compilation flags
# export ARCHFLAGS="-arch x86_64"

export PATH="$HOME/.composer/vendor/bin:$PATH"
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"

export NVM_DIR="$HOME/.nvm"
[ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"   # This loads nvm
[ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"   # This loads nvm bash_completion

export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/platform-tools

# Use Java 17 for React Native / Gradle
export JAVA_HOME="/opt/homebrew/opt/openjdk@17"
export PATH="$JAVA_HOME/bin:$PATH"


# Added by Windsurf
export PATH="/Users/amr.elghadban/.codeium/windsurf/bin:$PATH"

# Added by Antigravity
export PATH="/Users/amr.elghadban/.antigravity/antigravity/bin:$PATH"

# Added for PhpStorm
export PATH="/Applications/PhpStorm.app/Contents/MacOS:$PATH"

# --------------------------------------------------
# Codex smart launcher (Desktop + CLI)
#
# Usage:
#   codex              → Open Codex Desktop (current dir)
#   codex .            → Open Codex Desktop (current dir)
#   codex app [path]   → Open Codex Desktop (optional path)
#
#   codex cli          → Run Codex CLI (current dir)
#   codex cli --help   → Codex CLI help
#   codex cli .        → Codex CLI scoped to dir
#
# Notes:
# - Defaults to Desktop when no mode is provided
# - Desktop and CLI are intentionally separated
# - Avoids conflicts with Codex CLI binary
# --------------------------------------------------
codex() {
  local mode="$1"
  local target

  # Explicit mode handling
  if [[ "$mode" == "cli" || "$mode" == "app" ]]; then
    shift
  else
    mode="app"
  fi

  target="${1:-.}"

  case "$mode" in
    app)
      open -a "Codex" "$target"
      ;;
    cli)
      if command -v codex-cli >/dev/null 2>&1; then
        command codex-cli "$@"
      elif command -v codex >/dev/null 2>&1; then
        # fallback if CLI binary is also named codex
        command codex "$@"
      else
        echo "❌ Codex CLI not found in PATH"
        echo "👉 Install with: npm install -g @openai/codex"
        return 1
      fi
      ;;
  esac
}

# Set personal aliases, overriding those provided by oh-my-zsh libs,
# plugins, and themes. Aliases can be placed here, though oh-my-zsh
# users are encouraged to define aliases within the ZSH_CUSTOM folder.
# For a full list of active aliases, run `alias`.
#
# Example aliases
alias zshconfig="mate ~/.zshrc"
alias ohmyzsh="mate ~/.oh-my-zsh"

# IDE Aliases
alias vs="code"
alias cr="cursor"
alias ps="phpstorm"
alias ws="surf"
alias windsurf="surf"
alias ag="antigravity"

#alias codex='open -a "Codex"' # <<<< example for open app via terminal command


eval "$(rbenv init - zsh)"
# Added by Antigravity IDE
export PATH="/Users/amr.elghadban/.antigravity-ide/antigravity-ide/bin:$PATH"

```

# Owner Notes

This configuration is optimized for:

- React Native Development
- PHP Development
- WordPress Projects
- Android Builds
- iOS Builds (CocoaPods)
- AI-Assisted Development
  - Codex
  - Windsurf
  - Antigravity
  - Cursor
- JetBrains PhpStorm Workflow

Maintained by: **Amr Ahmed Elghadban**
