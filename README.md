# Linux_Resource_limits
On our Storage server in Stratos Datacenter we are having some issues where nfsuser user is holding hundred of processes, which is degrading the performance of the server. Therefore, we have a requirement to limit its maximum processes. Please set its maximum process limits as below:
### a. soft limit = 1025

### b. hard_limit = 2024


#### Login to Storage Server

`cat /etc/passwd`



`sudo vi /etc/security/limits.conf`

#### Add these command to add limits
`nfsuser soft nproc 1025`

`nfsuser hard nproc 2024`


#### To check limits

`ulimit -Sn`

`ulimit -Hn`
