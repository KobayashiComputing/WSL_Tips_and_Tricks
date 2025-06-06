### Install Edge on Ubuntu using the terminal

Do you prefer to install software on Ubuntu using the command line? If so I’ve got you covered.

First step: set-up.

The following command will add the official Microsoft Edge Linux repo to your system and import the Microsoft GPG key that is required to authenticate packages (so Ubuntu can be sure they are what they say they are):

```
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/edge stable main" > /etc/apt/sources.list.d/microsoft-edge-dev.list'
sudo rm microsoft.gpg
```

If running this command shows an error that `curl` is not installed you must first install Curl in Ubuntu by running `sudo apt install curl` then re-run the command above.

Second step: paste this command in to the terminal to first refresh the list of packages your system can see is available, and then download and install the latest stable Microsoft Edge for Linux release:

```
sudo apt update && sudo apt install microsoft-edge-stable
```

Once done, launch the browser using your favourite [Linux app launcher](https://www.omgubuntu.co.uk/2019/08/best-app-launcher-for-ubuntu-linux), or run `microsoft-edge` .

And with the Edge Linux repo added you can also choose to install `microsoft-edge-beta` or `microsoft-edge-unstable` builds. Just keep in mind those aren’t stable so may contain bugs and unfinished features.

### How to Uninstall Microsoft Edge

If you install Edge, try it out, but decide it’s not for you or takes up too much space, you can uninstall the browser as easily as you added it.

Open a new *Terminal* window and run:

```
sudo apt remove microsoft-edge-stable
```

Simple!