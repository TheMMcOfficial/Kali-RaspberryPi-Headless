# Kali-RaspberryPi-Headless

first things first change the default password
ssh to your pi vi this command:
ssh kali@IP_OF_YOUR_PI

the default password is "kali"

then type "passwd" to change it

To remove the default SSh key do this:
sudo dpkg-reconfigure openssh-server

Update your PI
sudo apt update
sudo apt upgrade -y
sudo apt full-upgrade
sudo apt autoremove

Install zsh completary 
sudo apt install zsh-syntax-highlighting autojump zsh-autosuggestions

Install if it's not there VNC
sudo apt install tightvncserver -y

vncserver
vncserver -kill :1
sudo chmod +x ~/.vnc/xstartup
vncserver

You can now connect to your PI trough VNC via your IP:5901


To make an AP from the internal wifi card: https://gist.github.com/Lewiscowles1986/fecd4de0b45b2029c390
I have made a mini modification to the script to make it work on kali 2020.4.
