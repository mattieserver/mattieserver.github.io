# mssqlclient.py

From the Impacket repo you can use the mssqlclient.py tool

## Connect to sql server

`mssqlclient.py -windows-auth $DOMAIN/$USER:$PASSWORD@$IP`

| Parameter        | Description           |
| ------------- |:-------------:| 
| $DOMAIN | The windows domain | 
| $USER | The username | 
| $PASSWORD | The password for the user | 
| $IP | The IP of the host | 

### Get the role for the current user

`select r.name as Role, m.name as Principal from  master.sys.server_role_members rm inner join master.sys.server_principals r on r.principal_id = rm.role_principal_id and r.type = 'R' inner join master.sys.server_principals m on m.principal_id = rm.member_principal_id where m.name = '$DOMAIN\$USER'` 

| Parameter        | Description           |
| ------------- |:-------------:| 
| $DOMAIN | The windows domain | 
| $USER | The username | 

