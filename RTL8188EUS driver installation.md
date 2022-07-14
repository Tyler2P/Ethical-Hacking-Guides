# Install RTL8188EUS Chipset Drivers in Kali

## Update your system & ensure you're on the latest version of Kali Linux

```
sudo apt update -y && sudo apt upgrade -y
```

## Install required dependencies

```
sudo apt install bc
sudo apt-get install build-essential
sudo apt-get install libelf-dev
sudo apt install dkms
```

## Install the latest kernel Linux headers

```
sudo apt-get install linux-headers-5.16.0-kali6-amd64
```

## Remove old drivers

```
sudo rmmod r8188eu.ko
```

## Get the new drivers from github, then change directories into it

```
git clone https://github.com/aircrack-ng/rtl8188EUS
cd rtl8188eus
```

## Move to root and insert the new drivers

```
sudo -i
echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf"
exit
```

## Reboot the machine then check for any updates

```
sudo reboot
sudo apt update
```

## Move back to your driver installation

```
cd rtl8188eus
```

## Build the drivers

```
sudo make
sudo make install
```

## Insert the drivers into the operating system

```
sudo modprobe 8188eu
```

### Known Errors
* If an error occures, "option not permitted", disable secure boot on your device