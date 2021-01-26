# Kali-RaspberryPi-Headless

You can find the image here: https://www.offensive-security.com/kali-linux-arm-images/

I suggest you to use Etcher to flash it since it is multi OS (Windows/Linux\MacOS): https://www.balena.io/etcher/

Flash the image to your SD card and boot up your Pi.


### first things first change the default password
ssh to your pi vi this command:

```ssh kali@IP_OF_YOUR_PI```

the default password is "kali"

then type ```passwd``` to change it

To remove the default SSH key do this:

```sudo dpkg-reconfigure openssh-server```

### Update your Pi
```
sudo apt update
sudo apt upgrade -y
sudo apt full-upgrade
sudo apt autoremove
```

### Install ZSH completary 
```sudo apt install zsh-syntax-highlighting autojump zsh-autosuggestions```

### Install if it's not there VNC
```
sudo apt install tightvncserver -y

vncserver
vncserver -kill :1
sudo chmod +x ~/.vnc/xstartup
vncserver
```

You can now connect to your PI trough VNC via your IP:5901


### To make an AP from the internal wifi card
You can take this script https://gist.github.com/Lewiscowles1986/fecd4de0b45b2029c390
I have made a mini modification to the script to make it work on kali 2020.4 the script is in this github repo.
