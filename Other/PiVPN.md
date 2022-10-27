# PiVPN Setup

## Adding a user

```
pivpn add
```
Then, fololow the prompts

## Removing a user
```
pivpn revoke
```
Then, follow the prompts

## Restarting PiVPN - OpenVPN
```
sudo service openvpn restart

pivpn -d
```

## Restarting PiVPN - Wireguard
```
sudo system wg-quick@wg0 restart

pivpn -d
```

Reference:
* https://docs.pivpn.io/faq/