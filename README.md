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
  
  mkdir $HOME/Library/Application\ Support/iTerm2/Scripts/AutoLaunch
  
  cp $PWD/iterm/DarkLightSwitcher.py $HOME/Library/Application\ Support/iTerm2/Scripts/AutoLaunch
  ```
  - To stop restoring iTerm last run window content change macOS settings > Desktop & Dock > Enable `Close windows when quitting an application`
  - Enable Automatic saving of preference changes of iTerms from  Settings > General > Preference > Save changes

- Install Oh-My-Zsh
  ```
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```

- Install Powerlevel10K
  ```
  git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
  sed -i .bak 's/robbyrussell/powerlevel10k\/powerlevel10k/1' ~/.zshrc
  source ~/.zshrc
  ```

- Install Extra ZSH Plugins
  ```
  git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
  git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
  ```
    - Update plugins section of ~/.zshrc with zsh-autosuggestions zsh-autocomplete zsh-syntax-highlighting
    - Need to verify the zsh-autocomplete usage with work laptop
    - Need to verify zsh-syntax-highlighting usage in work laptop with kubectl, gcloud if it works

- Install VS Code
  ```
  brew install --cask visual-studio-code
  ```

- Install Maccy
  ```
  brew install --cask maccy
  ```


