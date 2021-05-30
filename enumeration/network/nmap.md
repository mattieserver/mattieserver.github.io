# NMAP

## Basic scan

Start a scan of the IP/Host to get the open ports and services.

`sudo nmap -sC -sV -oA nmap_scan $IP`

| Parameter        | Description           |
| ------------- |:-------------:| 
| sC | Default scripts (--script=default) | 
| sV | Get version/service info | 
| oA  nmap_scan | Output all formats to nmap_scan file | 
| $IP | The IP of the host | 


## Scan all ports

By default nmap scans only the 1000 most common ports, so it can be usefull to scan all the ports.

`sudo nmap -p- -oA nmap_scan $IP`

| Parameter        | Description           |
| ------------- |:-------------:| 
| p- | Scan all ports (1 to 65535) | 
| oA  nmap_scan | Output all formats to nmap_scan file | 
| $IP | The IP of the host | 


## Dont open full TCP connection

It can be usefull to not open a full tcp connection, you can do this with the parameter below:

`-sS`

## Idle scan

Scan hoss with a extra zombie host, this can be used to hide your own machine.

`sudo nmap -Pn -sI $IDLE_HOST:$IDLE_PORT $IP`
| Parameter        | Description           |
| ------------- |:-------------:| 
| Pn | prevent using own host | 
| sI  $IDLE_HOST:IDLE_PORT | idle mode, where IDLE_HOST and IDLE_PORT are the IP/port from another hosts | 
| $IP | The IP of the host | 


The zombie host can be found with the following command:

`sudo  nmap -O $IP`

| Parameter        | Description           |
| ------------- |:-------------:| 
| O | os detection | 
| $IP | The IP of the host | 

If the "IP ID" is incremental we can use the host as a zombie