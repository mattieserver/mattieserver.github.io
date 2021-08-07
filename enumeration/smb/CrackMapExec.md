# CrackMapExec

## Get SMB info

To get the OS version or basic smb info.

`poetry run crackmapexec smb $IP`

| Parameter        | Description           |
| ------------- |:-------------:| 
| $IP | The IP of the host | 

## List Shares

To list the shares of a host/IP.

`poetry run crackmapexec smb $IP --shares`

| Parameter        | Description           |
| ------------- |:-------------:| 
| $IP | The IP of the host | 
| --shares | List the shares  | 

You may also add `-p ' ' -u ' '` to get more info with auth. 

| Parameter        | Description           |
| ------------- |:-------------:| 
| -p ' ' | Username (Blank) | 
| -u ' ' | Password (Blank)  | 

## List all files from readable shares

To list all files you can access you can use the spider_plus module

`poetry run crackmapexec smb $IP -M spider_plus -p '' -u ''`

| Parameter        | Description           |
| ------------- |:-------------:| 
| -p '' | Username (Blank) | 
| -u '' | Password (Blank)  | 
| -M spider_plus | Module spider_plus  | 
