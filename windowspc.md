# Installation Windows

This installation guide is intended for home and/or business Windows 10/11 PC.

# Installation

First of all update Windowsa and install the required drivers.

Then open a Powershell with elevated privileges and install chocolatey:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

Enable the installation for all users:

```powershell
choco feature enable -n allowGlobalConfirmation
```

Then install the desired apps:

```powershell
choco install 7zip.install
choco install anydesk
choco install authy-desktop
choco install brave
choco install cdburnerxp
choco install choco-cleaner
choco install choco-shortcuts-winconfig
choco install citrix-workspace
choco install corretto11jdk
choco install cpu-z
choco install cyg-get
choco install cygwin
choco install dbeaver
choco install discord
choco install docker-desktop
choco install drawio
choco install dropbox
choco install em-client
choco install filezilla
choco install firefox
choco install git.install
choco install googlechrome
choco install greenshot
choco install intellijidea-community
choco install keepass
choco install keepassxc
choco install kubelogin
choco install kubernetes-cli
choco install make
choco install maven
choco install mongodb-compass
choco install mremoteng
choco install nextcloud-client
choco install notepadplusplus.install
choco install pdf24
choco install powertoys
choco install putty
choco install python3
choco install signal
choco install sonos-controller
choco install steam
choco install sysinternals
choco install teamviewer
choco install telegram
choco install tortoisesvn
choco install vlc
choco install vmwareworkstation
choco install vscode
choco install WhatsApp
choco install winrar --ignore-checksums
choco install winscp

```

Optional:

```powershell
choco install lghub --ignore-checksums
```

Swisscom specific:

```powershell
\\sch4045\x$\Server\Server_Common_for_all\Server_Settings_Batch
```

## Update

choco upgrade all

## Blacklist updates

choco pin list
choco pin add -n vmwareworkstation
choco pin remove -n vmwareworkstation

## List all installed packages

clist -l