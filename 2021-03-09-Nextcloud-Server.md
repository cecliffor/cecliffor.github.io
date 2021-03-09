Nextcloud install

#duckdns install

#Setup HTTPS
##Install snapd
sudo apt update
sudo apt install snapd

##Install core
sudo snap install core; sudo snap refresh core

##Install certbot
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot

##Run certbot
sudo ./certbot --apache
