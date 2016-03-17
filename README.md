# Raspberry Pi Setup

## Burn Raspian to MicroSD card using Disk Utility

## Initial Configuration
``raspi-config``

## Reboot
```sudo reboot```

## Install Apps

### Transmission
```sudo apt-get install transmission-cli transmission-common transmission-daemon```

### VLC 
```sudo apt-get install vlc browser-plugin-vlc```

## Instalk Appletalk protocol on Pi
```sudo apt-get install netatalk```
To connect:  
```open afp://10.1.1.10  (replace this with your Raspberry Pi IP address)```

## Find IP address
```nmap -sn 192.168.1.1/24```

## Connecting
```ssh pi@10.1.10```
Default password is 'raspberry'

## VNC Protocol
```vncserver :1 -geometry 1920x1080 -depth 24 -dpi 96```
```vncserver -kill :1```  

Enable screen sharing on Mac from preferences and open a session using:

```open vnc://pi@192.168.1.15:5901```

## Assigning .local domain to Pi using Bonjour
[Instructions](http://www.howtogeek.com/167190/how-and-why-to-assign-the-.local-domain-to-your-raspberry-pi/)

## Setting wireless module
[From the command line](https://learn.adafruit.com/adafruits-raspberry-pi-lesson-3-network-setup/setting-up-wifi-with-occidentalis)

## Setting up X11
```sudo apt-get install x11vnc```
```x11vnc -storepasswd```
```x11vnc -forever -usepw -display :0 -ultrafilexfer```

## Setting up openFrameworks
[Guide](http://openframeworks.cc/setup/raspberrypi/)
[Cross-compiling](https://forum.openframeworks.cc/t/cross-compiler-for-of-0-9-0-jessie-arm6-rpi1/21336)
