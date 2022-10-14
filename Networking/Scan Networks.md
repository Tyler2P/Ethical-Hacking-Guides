# Scan Networks

## Installation

```
sudo apt install aircrack-ng
```

---

## Scan for nearby networks

Base Command:
```
sudo airodump-ng wlan0
```
Note: Change `wlan0` to your own interface

### Filter by BSSID
```
sudo airodump-ng --bssid <AP BSSID> wlan0
```
Explanation:
* `AP Name` - The AP's BSSID<br>
* `wlan0` - Your wireless interface

### Filter by ESSID
```
sudo airodump-ng --essid <AP Name> wlan0
```
Explanation:
* `AP Name` - The AP's Name/ESSID<br>
* `wlan0` - Your wireless interface

### Filter by ESSID (regex)
```
sudo airodump-ng --essid-regex <AP Name Regex> wlan0
```
Explanation:
* `AP Name Regex` - Filter AP's using a regular expression<br>
* `wlan0` - Your wireless interface