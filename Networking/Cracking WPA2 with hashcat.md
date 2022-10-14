# Cracking WPA/WPA2 with hashcat

## Installation

hashcat (v6.0.0 or above)<br>
hcxdumptool (v6.2.5 or above)<br>
hcxtools
```
sudo apt install hcxdumptool
sudo apt install hashcat
sudo apt install hcxtools
```

---

## Scan for wireless networks

```
sudo hcxdumptool -i wlan0 -o <file name>.pcapng --active_beacon --enable-status=15
```

### Explanation

`wlan0` - Your wireless interface<br>
`file name` - Your output file name
`--active-beacon` - To only use networks that are in use
`--enable-status=15` - To provide a live feed in the terminal

### Notes

* Let the command run for a while as it captures information about the network
* May take a while to start up if wifi card does not natively support monitor mode

## Convert the output file into a format that can be read by hashcat

```
sudo hcxpcapngtool -o <output file name>.hc22000 -E <essid-list file name> <dump-file file name>
```

### Explanation
`output file name` - The new files name<br>
`essid-list file name` - (OPTIONAL) The name for the file to list the captured ESSIDs<br>
`dump-file file name` - The output from the last command

---

## Scan wireless networks

```
sudo hcxdumptool --do_rcascan -i wlan0
```

### Explanation
`--do_rcascan` - The name of the scan<br>
`wlan0` - Your wireless interface

### Notes
* May take a while to start up if wifi card does not natively support monitor mode

---

