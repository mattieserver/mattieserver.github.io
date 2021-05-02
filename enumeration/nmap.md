# NMAP

## Basic scan

Start a scan of the IP/Host to get the open ports and services

`sudo nmap -sC -sV -oA nmap_scan $IP`

| Parameter        | Description           |
| ------------- |:-------------:| 
| sC | Default scripts (--script=default) | 
| sV | Get version/service info | 
| oA  nmap_scan | Output all formats to nmap_scan file | 
| $IP| The IP of the host | 

## Scan all ports

`sudo nmap -p- -oA nmap_scan $IP`

| Parameter        | Description           |
| ------------- |:-------------:| 
| -p- | Scan all ports (1 to 65535) | 
| oA  nmap_scan | Output all formats to nmap_scan file | 
| $IP| The IP of the host | 
