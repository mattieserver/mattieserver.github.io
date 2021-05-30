# NMAP

## Basic port check

Check if a port replys on SYN packets

`hping3 -S $IP -p $PORT -c $COUNT`

| Parameter        | Description           |
| ------------- |:-------------:| 
| S $IP | set SYN flag | 
| p $PORT | remote port | 
| c $COUNT | number of packets to send| 