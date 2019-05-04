# helpme
A repo for all the problems and solutions I have in Ubuntu, Mint or any other distro I have trouble with.


## No Network Adapter Found

**Distro:** Ubuntu 18.04 LTS

**Problem:** <br/>
When ubuntu was installed, my Intel 6265/8275 Wireless Network Adapter wasn't showing up
on the Wifi settings and on windows there is no troubleshooter. 

**Solution:** <br/>
Connect laptop to an ethernet cable (with internet access, idiot) <br/>
Open a terminal and run: <br/>
```
sudo apt install git dkms build-essential
cd /tmp
git clone https://github.com/jeremyb31/idea-laptop.git
sudo dkms add ./idea-laptop
sudo dkms install ideapad-laptop/*.*
sudo reboot
```
## Login Loop

**Distro:** Ubuntu 18.04 LTS

**Problem:** <br/>
Boot is fine and login screen looks fine. After a login is attempted, you will get a black screen for about 2 seconds or quicker. The it will revert back to the login screen. THIS SOLUTION WILL ONLY WORK WITH A DEDICATED AND INTEGRATED GPU

**Solution:** <br/>
This is probably a problem with Nvidida drivers. This can be easily solved by entering this in a terminal:
''''
prime-select intel
''''
Reboot and you should have access to the desktop

## Gnome Control Center Not Showing in I3WM

**Distro:** Any linux-based distro

**Problem:** <br>
Opening `gnome-control-center` in i3wm brings up a blank window.

**Solution:** <br>
`gnome-control-center` must be launched with this command from the terminal
```
env XDG_CURRENT_DESKTOP=GNOME gnome-control-center
```
