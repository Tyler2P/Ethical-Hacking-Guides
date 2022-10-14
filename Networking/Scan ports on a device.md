# Scanning for open ports on a device

## Scan for specific ports
```
sudo nmap -sT -p 80,443 198.168.0.1
```
### Explanation
* `-sT` - The TCP protocol (See [#protocols](#protocols) for a full list)
* `-p` - The ports you're scanning for
* `198.168.0.1/24` - The IP address of the target machine

## Scan for all ports
```
sudo nmap -sT -p- 198.168.0.1
```
### Explanation
* `-sT` - The TCP protocol (See [#protocols](#protocols) for a full list)
* `-p-` - Scan all ports
* `198.168.0.1/24` - The IP address of the target machine


# Protocols
Expression | Name      | Alias          | Explanation
---------- | --------- | -------------- | ---------
`-sT`      | TCP       | Full-open scan | Scan a network and ensure the port is completely open
`-sS`      | Stealthy  | Half-open scan | Scan a network for open ports bypassing *most* firewalls
`-sO`      | IP Protocol Scan | N/A     | Find which IP protocols are supported by target machines
`-sA`      | IP Protocol Scan | N/A     | Find which IP protocols are supported by target machines
`-A`       | Agressive Mode   | N/A     | Find information on a device (OS detection, version detection, script scanning & traceroute)

# Options
Expression | Name      | Example | Explanation
---------- | --------- | ------- | ---------
`-D`       | Decoy     | [#Decoy Example](#decoy-example) | Send traffic from a range of different IP addresses 

# Examples

## Decoy Example
```
sudo nmap -sS -D 192.168.0.2 192.168.0.1
```
### Explanation
* `-sS` - Run a half open scan (to avoid detection)
* `-D` - Decoy as another IP
* `192.168.0.2` - The decoy IP
* `192.168.0.1` - The target machine