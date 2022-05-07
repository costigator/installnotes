# Installation MacMini M1

My installation and setup notes for my MacMini M1. 

## System preferences

- Scroll direction (uncheck natural)
- Mouse tracking speed
- [YouTube Tutorial](https://www.youtube.com/watch?v=5eSaJGSGLs0&t=285s)

## Utilities

- [SwitchResX](https://www.madrau.com)
- [Sound Source](https://rogueamoeba.com/soundsource/) (Security changes and license needed)

## Install Homebrew

Don't forget to do the last steps that are described after the installation:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Install these apps:

```bash
brew install htop iterm2 rectangle pyenv git
brew install --cask docker
brew install --cask anydesk
brew install --cask visual-studio-code
brew install --cask ngrok
```

List packages

```bash
brew list
```

Pyenv additional config:

```bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```

## Customize the shell

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## App Store

- Twilio Authy
- Flycut

## Generate SSH key

The SSH key is generated on my Windows PC and used to access the Mac remotely.

```bash
ssh-keygen
```

## Update system

```bash
sudo softwareupdate -ia
brew upgrade --cask
```

## Start the getting started container

```bash
docker run -d -p 80:80 docker/getting-started
```
