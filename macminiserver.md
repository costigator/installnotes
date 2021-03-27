# Installation MacMini M1

Some installation notes for my MacMini M1. The SSH key is generated on my Windows PC and used to access the Mac remotely.

# Generate SSH key
ssh-keygen

# Update system
sudo softwareupdate -ia

# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install docker and some tools
brew install htop
brew install --cask anydesk
brew install --cask visual-studio-code
brew install --cask docker
brew install --cask ngrok

# Start the getting started container
docker run -d -p 80:80 docker/getting-started