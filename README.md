# My Dot files:

## Automate this
```sh
### Instalando Git e coisas básicas
xcode-select --install

### Oh My ZSH
sudo sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/lukechilds/zsh-nvm ~/.oh-my-zsh/custom/plugins/zsh-nvm 
rm -rf ~/.zshrc

### Setup dos dotfiles
git clone https://github.com/LuizModolo/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
ln -s ~/.dotfiles/.zshrc ~/.zshrc
ln -s ~/.dotfiles/.gitconfig ~/.gitconfig

### Instalando o Home brew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
## Configs for Macs M1 Chip:
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
brew bundle --file ~/.dotfiles/Brewfile

### Finalização
cd ~ && mkdir ./dev
```

## How to extract current installed files?
```sh
cd ~/.dotfiles && brew bundle dump --force && git add . && git commit -m "update" && git push 
```
