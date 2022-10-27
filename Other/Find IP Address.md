# Finding a public IP address using the linux terminal

## IPv4 Address
```
dig +short txt ch whoami.cloudflare @1.0.0.1
```

## IPv6 Address
```
dig -6 TXT +short o-o.myaddr.l.google.com @ns1.google.com
```