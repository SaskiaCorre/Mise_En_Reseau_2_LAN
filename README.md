# Cisco Packet Tracer – Interconnexion de deux LAN (IP statiques)

# Contexte
Ce projet s’inscrit dans le cadre d’un test technique pour un poste de **Technicien Supérieur Systèmes et Réseaux (TSSR)**.
L' objectif est de concevoir et configurer une infrastructure réseau simple permettant la communication entre deux réseaux locaux distincts à l’aide d’un routeur.

# Objectifs pédagogiques
- Concevoir une topologie réseau simple sur Cisco Packet Tracer
- Configurer un adressage IPv4 statique
- Mettre en œuvre le routage entre deux sous-réseaux
- Vérifier la connectivité réseau

# Topologie réseau

- Site A
  - Réseau : 192.168.1.0/24
  - 1 switch Cisco 2960
  - 2 postes clients

- Site B
  - Réseau : 192.168.2.0/24
  - 1 switch Cisco 2960
  - 2 postes clients

- Interconnexion
  - 1 routeur Cisco ISR 4331

Chaque site est physiquement séparé et connecté au routeur via un commutateur de niveau 2.

# Configuration réalisée

# Routeur
- Interface vers Site A : 192.168.1.1/24
- Interface vers Site B : 192.168.2.1/24
- Routage inter-réseaux activé par défaut

# Postes clients
- Configuration IP **statique**
- Passerelle définie vers l’interface du routeur correspondante

# Switchs
- Utilisation du VLAN par défaut (VLAN 1)
- Aucun VLAN supplémentaire configuré (non nécessaire dans ce scénario)

# Vérifications
- Ping entre postes d’un même LAN
- Ping entre postes du Site A et du Site B

Les tests confirment le bon fonctionnement du routage et de la communication inter-sites.
