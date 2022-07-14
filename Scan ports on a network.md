# Scanning for open ports on a network

## Scan for specific ports
```
sudo nmap -sT -p 80,443 198.168.0.1/24
```
### Explanation
* `-sT` - The TCP protocol (See [#protocols](#protocols) for a full list)
* `-p` - The ports you're scanning for
* `198.168.0.1/24` - The IP address of the router<br />
See [this list](#options) for other options

## Scan for all ports
```
sudo nmap -sT -p- 198.168.0.1/24
```
### Explanation
* `-sT` - The TCP protocol (See [#protocols](#protocols) for a full list)
* `-p-` - Scan all ports
* `198.168.0.1/24` - The IP address of the router<br />
See [this list](#options) for other options


# Protocols
Expression | Name      | Alias          | Explanation
---------- | --------- | -------------- | ---------
`-sT`      | TCP       | Full-open scan | Scan a network and ensure the port is completely open
`-sS`      | Stealthy  | Half-open scan | Scan a network for open ports bypassing *most* firewalls
`-sO`      | IP Protocol Scan | N/A     | Find which IP protocols are supported by target machines
`-sA`      | IP Protocol Scan | N/A     | Find which IP protocols are supported by target machines