# Configuration firewall Linux

## Comandes pour configurer simplement un firewall sur Linux

On veut fermer tout le traffic entrant et autoriser le traffic sortant
On veut aussi autoriser les protocoles ssh (port 22 en tcp), http/https (ports 80/443 en tcp), dns (port 53 en udp) et dhcp (port 68 en udp)

### commande de démarrage de ufw
$ ```shell
sudo ufw enable```

### autorisation d'IPV6 si nécessaire
$ ```shell
sudo nano /etc/default/ufw```
### vérifier qu'il y a la ligne IPV6=yes

### auotrisations des entrées et sorties
$ ```shell
sudo ufw default deny incoming```
$ ```shell
sudo ufw default allow outgoing```

### configuration des protocoles
$ ```shell
sudo ufw allow 22/tcp```
$ ```shell
sudo ufw allow 80/tcp```
$ ```shell
sudo ufw allow 443/tcp```
$ ```shell
sudo ufw allow 53/udp```
$ ```shell
sudo ufw allow 68/udp```

Légende :
$ pour les commandes
