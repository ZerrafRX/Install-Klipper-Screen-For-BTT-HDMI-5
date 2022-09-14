


# Install-Klipper-Screen-For-BTT-HDMI-5



Download and Install KIAUH

![kiauh](https://user-images.githubusercontent.com/39313169/190039394-ad41a125-108e-47f9-a148-03001d4f53d2.png)


For downloading this script it is necessary to have git installed.
If you haven't, please run sudo apt-get install git -y to install git first.
After git is installed, use the following commands in the given order to download and execute the script:

```shell
cd ~

git clone https://github.com/th33xitus/kiauh.git

./kiauh/kiauh.sh
```

<img width="462" alt="kiauh-1" src="https://user-images.githubusercontent.com/39313169/190041543-41b79e28-c515-4c75-9fb5-89bc80af5064.png">



Once Klipper screen is installed you will have to edit your Moonraker.cfg on either mainsail or fluid 
add this to your trusted clients section
```shell
[authorization]
trusted_clients:
  127.0.0.1
  ```
  
  If you wish to use the update manager feature of moonraker for KlipperScreen, add the following block to the moonraker.conf:

```shell
[update_manager KlipperScreen]
type: git_repo
path: ~/KlipperScreen
origin: https://github.com/jordanruthe/KlipperScreen.git
env: ~/.KlipperScreen-env/bin/python
requirements: scripts/KlipperScreen-requirements.txt
install_script: scripts/KlipperScreen-install.sh
managed_services: KlipperScreen
```

SSH into your pi (e.x: ssh pi@mainsail.local or pi@IP OF PI)

you will now need to edit the config.txt file from your boot directory of your Raspberry pi 

```shell

sudo nano /boot/config.txt
```

add these lines to the very bottom
```shell
hdmi_group=2
hdmi_mode=87
hdmi_cvt=800 480 60 6 0 0 0
hdmi_drive=1
```
hit ^X (for mac) or ctrl-X(for windows) 

Y to save

hit enter (do not change the name of this file ever)

type

```shell
reboot 

```
into your terminal to see if screen size updated properly

You should be all set!
