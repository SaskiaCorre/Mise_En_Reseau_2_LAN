# Cisco Packet Tracer – DHCP centralisé multi-sites

# Contexte
Ce projet est la suite directe de la Partie 1.  
L’entreprise souhaite faciliter l’ajout de nouveaux équipements sur le réseau en automatisant l’attribution des adresses IP.

Un serveur DHCP centralisé est mis en place afin de desservir deux sous-réseaux distincts.

# Objectifs 
- Mettre en place un serveur DHCP
- Créer plusieurs pools d’adresses DHCP
- Comprendre et configurer le DHCP Relay (IP Helper)
- Simplifier l’administration réseau
- Valider le fonctionnement sur plusieurs LAN

# Topologie réseau

- Site A
  - Réseau : 192.168.1.0/24
  - Serveur DHCP
  - Switch Cisco 2960
  - Postes clients

- Site B
  - Réseau : 192.168.2.0/24
  - Switch Cisco 2960
  - Postes clients

- Routeur Cisco ISR 4331
  - Assure le routage inter-sites
  - Joue le rôle de DHCP Relay

# Configuration réalisée

# Serveur DHCP (Site A)
- Adresse IP statique : 192.168.1.10/24
- Passerelle : 192.168.1.1

# Pools DHCP
- Pool Site A
  - Réseau : 192.168.1.0/24
  - Passerelle : 192.168.1.1
  - Plage dynamique à partir de 192.168.1.100

- Pool Site B
  - Réseau : 192.168.2.0/24
  - Passerelle : 192.168.2.1
  - Plage dynamique à partir de 192.168.2.100

# Routeur – DHCP Relay
- Configuration de la commande :

sur l’interface connectée au Site B.

Cette configuration permet au routeur de relayer les requêtes DHCP vers le serveur situé sur un autre réseau.

# Postes clients
- Configuration en DHCP
- Attribution automatique :
  - Adresse IP
  - Masque de sous-réseau
  - Passerelle
  - DNS

# Vérifications
- Attribution correcte des adresses IP sur les deux sites
- Ping entre postes des deux LAN
- Fonctionnement validé du DHCP centralisé et du relay

# Conclusion
Cette seconde partie démontre la mise en place d’une solution DHCP centralisée adaptée à une PME, améliorant la flexibilité et la maintenabilité du réseau tout en restant simple et robuste.
