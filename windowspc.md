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
choco install choco-cleaner
choco install choco-shortcuts-winconfig
choco install googlechrome
choco install firefox
choco install powertoys
choco install cpu-z
choco install vscode
choco install notepadplusplus.install
choco install git.install
choco install 7zip.install
choco install python3
choco install mremoteng
choco install docker-desktop
choco install greenshot
choco install filezilla
choco install citrix-workspace
choco install WhatsApp
choco install telegram
choco install keepassx
choco install authy-desktop
choco install dropbox
choco install dbeaver
choco install intellijidea-community
choco install kubernetes-cli
choco install kubelogin
choco install tortoisesvn
choco install corretto11jdk
choco install keepass
choco install vmwareworkstation (requires reboot)
choco install drawio
choco install make
choco install cygwin
choco install cyg-get
choco install vlc
choco install maven
choco install winscp
choco install putty
choco install steam
choco install sonos-controller
choco install vlc
choco install anydesk
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