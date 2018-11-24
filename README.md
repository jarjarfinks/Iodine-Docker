# iodined DNS Tunnel with SSH quick start
## DNS 
1. 	set two domain records
```
tunnel		IN	NS	ns1.mydomain.com.		; THIS IS the DOMAIN YOU NEED TO WRITE IN SETTING
ns1		IN	A	1.1.1.1		; POINT TO YOUR IP
  ```
## Server side
1. manage file setting dns password in `docker-compose.yml`
2. `docker-compose up -d`
3. enjoy it!
## Client 
1. install iodine  `apt isntall iodine`
2. run command with your password and domain name `iodine -f -P {PASSWORD} {DNS}`
3. get SSH Tunnel for a proxy  `ssh -D 8080 sshproxy@10.1.1.1` and password is `sshproxy`
4. set your proxy to 127.0.0.1:8080 with SOCK
