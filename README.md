# iodine DNS Tunnel with SSH quick start
## DNS 
1. 	set two domain records
```
tunnel		IN	NS	ns1.mydomain.com.		; THIS IS the DOMAIN YOU NEED TO WRITE IN SETTING
ns1		IN	A	1.1.1.1				; POINT TO YOUR IP
  ```
## Server
1. git clone this project 
2. manage file setting dns password in `docker-compose.yml`
3. `docker-compose up -d`

## Client 
1. install iodine  `apt isntall iodine`
2. run command with your password and domain name `iodine -f -P {PASSWORD} {DNS}` 
    - ex. `iodine -f -P "aaaa" "tunnel.mydomain.com"`
3. get SSH Tunnel for a proxy  `ssh -D 8080  sshproxy@10.1.1.1` and password is `sshproxy`
4. set your proxy to 127.0.0.1:8080 with SOCK
5. enjoy it!
