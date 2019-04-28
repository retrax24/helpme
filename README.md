# helpme
A repo for all the problems and solutions I have in Ubuntu, Mint or any other distro I have trouble with.


### No Network Adapter Found

Distro: Ubuntu 18.04 LTS

Problem: When ubuntu was installed, my Intel 6265/8275 Wireless Network Adapter wasn't showing up
on the Wifi settings and on windows there is no troubleshooter. 

Solution: 
Connect laptop to an ethernet cable (with internet access, idiot)
Open a terminal and run:
    sudo apt install git dkms build-essential
    git clone https://github.com/jeremyb31/idea-laptop.git
    sudo dkms add ./idea-laptop
    sudo dkms install ideapad-laptop/*.*

Reboot \n
Boom ((internets)) \n
