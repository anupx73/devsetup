# Dev Environment Setup
## Summary
My workstation set up for dev env

## Recipes
- Install homebrew
  ```
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```
- Install iterm2
  ```
  brew install --cask iterm2
  ```

- Config iterm2
  ```
  defaults write com.googlecode.iterm2 PrefsCustomFolder -string "$PWD/iterm"
  defaults write com.googlecode.iterm2 LoadPrefsFromCustomFolder -bool true
  cp $PWD/iterm/auto-dark-mode.py $HOME/Library/Application\ Support/iTerm2/Scripts/
  # To use the above script enable it from Menu > Scripts
  ```
[TODO]
