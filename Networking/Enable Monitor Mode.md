# Enable Monitor Mode

Firstly, you want to kill any processes that can conflict with monitor mode

```
sudo airmon-ng check kill
```

Then follow one of the following methods to enable monitor mode for your wireless interface

## Method One

```
sudo ifconfig wlan0 down
```
```
sudo iwconfig wlan0 mode monitor
```
```
sudo ifconfig wlan0 up
```
Note: Change `wlan0` to your own interface

## Method Two

```
sudo airmon-ng start wlan0
```
Note: Change `wlan0` to your own interface