# ansible-role-nginx-acmesh


```
- install acme.sh
- ensure azuredns is setup 
- sudo groupadd certs
- sudo mkdir /etc/certs
- sudo chown 
- acme.sh --issue --dns dns_azure -d kartan.no -d *.kartan.no -d *.app.kartan.no -d *.api.kartan.no --cert-home /etc/certs
- acme.sh --issue --dns dns_azure -d kartan.no -d *.kartan.no -d *.app.kartan.no -d *.api.kartan.no --install-cronjob --cert-home /etc/certs
- make all apps user this setup

- acme.sh --install-cert -d kartan.no -d *.kartan.no -d *.app.kartan.no -d *.api.kartan.no \
--key-file       /etc/certs/kartan.no/key.pem  \
--fullchain-file /etc/certs/kartan.no/cert.pem \
--reloadcmd     "service nginx force-reload" --install-cronjob

zHNSFER7AYIl8iQjwVferUQTg

```

## NGINX 

use the --install-cert flag to install for apache or nginx. Nothing more needed

acme.sh --install-cert -d kartan.no -d *.kartan.no -d *.app.kartan.no -d *.api.kartan.no --key-file       /etc/certs/kartan.no/key.pem  --fullchain-file /etc/certs/kartan.no/cert.pem --reloadcmd     "service nginx force-reload" --install-cronjob
