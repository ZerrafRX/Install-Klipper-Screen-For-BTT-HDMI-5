

# Install-Klipper-Screen-For-BTT-HDMI-5



Download and Install KIAUH

![kiauh](https://user-images.githubusercontent.com/39313169/190039394-ad41a125-108e-47f9-a148-03001d4f53d2.png)


For downloading this script it is necessary to have git installed.
If you haven't, please run sudo apt-get install git -y to install git first.
After git is installed, use the following commands in the given order to download and execute the script:

cd ~

git clone https://github.com/th33xitus/kiauh.git

./kiauh/kiauh.sh



Once Klipper screen is installed you will have to edit your config.txt from the boot folder

SSH into you pi (e.x: ssh pi@<hostname.here>)

type sudo nano /boot/config.txt

add these lines to the very bottom

hdmi_group=2
hdmi_mode=87
hdmi_cvt=800 480 60 6 0 0 0
hdmi_drive=1

hit ^X (for mac) 

Y to save

hit enter (do not change the name of this file ever)

type "reboot" into your terminal to see if screen size updated properly

You should be all set!
