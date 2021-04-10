# Installation MacMini M1

Some installation notes for my MacMini M1. The SSH key is generated on my Windows PC and used to access the Mac remotely.

## Customize the shell

```bash
echo "alias ll='ls -lG'" >> ~/.zprofile
```

## Generate SSH key

```bash
ssh-keygen
```

## Update system

```bash
sudo softwareupdate -ia
brew upgrade --cask
```

## Install Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Install docker and some tools

```bash
brew install htop
brew install --cask anydesk
brew install --cask visual-studio-code
brew install --cask docker
brew install --cask ngrok
brew install --cask iterm2
```

## Start the getting started container

```bash
docker run -d -p 80:80 docker/getting-started
```
