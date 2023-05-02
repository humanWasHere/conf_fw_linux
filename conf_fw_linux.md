# Configuration firewall Linux

## Comandes pour configurer simplement un firewall sur Linux

On veut fermer tout le traffic entrant et autoriser le traffic sortant
On veut aussi autoriser les protocoles ssh (port 22 en tcp), http/https (ports 80/443 en tcp), dns (port 53 en udp) et dhcp (port 68 en udp)

### Commande de démarrage de ufw
$ ```sudo ufw enable```

### Autorisation d'IPV6 si nécessaire
$ ```sudo nano /etc/default/ufw```
### Vérifier qu'il y a la ligne IPV6=yes

### Autorisations des entrées et sorties
$ ```sudo ufw default deny incoming```
$ ```sudo ufw default allow outgoing```

### Configuration des protocoles
$ ```sudo ufw allow 22/tcp```
$ ```sudo ufw allow 80/tcp```
$ ```sudo ufw allow 443/tcp```
$ ```sudo ufw allow 53/udp```
$ ```sudo ufw allow 68/udp```

Légende :
$ pour les commandes
