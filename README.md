# oem_discourse

**OpenEnergyMonitor forum Discourse config **

Running discourse docker container

  cd /var/discourse

Start / stop container

  /var/discourse/./launcher start app
  /var/discourse/./launcher stop app

Edit config

  nano /var/discourse/containers/app.yml

Rebuild after editing

  /var/discourse/./launcher rebuild app

SSH into docker container

  /var/discourse/./launcher ssh app

SSH into docker

  sudo /var/discourse/./launcher enter app

Backup Location
  
  /var/discourse/shared/standalone/backups/default


## CURRENT SETUP

Nginx on port 80 & 443, use virtual hosts to reverse proxy all other site traffic to Apache on port 8080 and Discourse traffic to Discourse HTTP socket.  SSL gets terminated at Nginx for apache and SSL gets passed to discourse via https web socket


Run with another server bind to different port
https://meta.discourse.org/t/running-other-websites-on-the-same-machine-as-discourse/17247
