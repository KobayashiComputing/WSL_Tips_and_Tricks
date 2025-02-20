# Installation and Initial Setup
## Ubuntu 24.04 LTS
The following command issued in an Administrator shell will install Ubuntu 24.04 LTS and make it the default.
```
wsl --install -d ubuntu-24.04
```
## Kali (Rolling)
The following command issued in an Administrator shell will install Kali (Rolling).
```
wsl --install kali-Linux
```
You will almost certainly want to install all (or at least almost all) of the available Kali tools, with the following command.
```
sudo apt install -y kali-linux-large
```
I then remove the OSS VS-Code version that gets installed with the above. I prefer to use VS Code on Windows and connect to the WSL distros via the WSL extension from Microsoft (which is part of the Remote Development extension - which I highly recommend). 
```
sudo apt remove code-oss
```
Then run VS-Code on Windows and connect to the WSL session for Kali-Linux (sweet!)
## Setting the Prompt
I like the prompt that is created by the following; your mileage may vary, as they say. Note that I backup the original .bashrc file first.
```
cp .bashrc .bashrc.bak
echo 'export PS1="-[\[$(tput sgr0)\]\[\033[38;5;10m\]\d\[$(tput sgr0)\]-\[$(tput sgr0)\]\[\033[38;5;10m\]\t\[$(tput sgr0)\]]-[\[$(tput sgr0)\]\[\033[38;5;214m\]\u\[$(tput sgr0)\]@\[$(tput sgr0)\]\[\033[38;5;196m\]\h\[$(tput sgr0)\]]-\n-[\[$(tput sgr0)\]\[\033[38;5;33m\]\w\[$(tput sgr0)\]]\\$ \[$(tput sgr0)\]"' >> .bashrc
```
## Update(s)
Start each distro in turn, and install updates (on a regular basis).
```
sudo apt update
sudo apt full-upgrade -y
```
