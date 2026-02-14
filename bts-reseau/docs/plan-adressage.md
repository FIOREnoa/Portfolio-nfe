# Plan d’adressage

## Résumé des réseaux
| Zone | Réseau       | Masque/CIDR |  Passerelle  |              DHCP               |      DNS      | 
|------|--------------|-------------|--------------|---------------------------------|---------------|
| LAN  | 192.168.10.0 | /24         | 192.168.10.1 | 192.168.10.100 - 192.168.10.150 | 192.168.10.10 |
| DMZ  | 10.0.0.0     | /24         | 10.0.0.1     | (statique)                      | 192.168.10.10 |
| WAN  | 172.31.0.0   | /16         | 172.31.30.254| (le wan était le lan de mon établissement)


## Équipements (IP statiques)
| Nom | Rôle | Zone | IP |
|-----|------|------|----|
| OPNsense-LAN          | Passerelle LAN       | LAN | 192.168.10.1   |
| OPNsense-DMZ          | Passerelle DMZ       | DMZ | 192.168.10.1   |
| OPNsense-WAN          | Passerelle WAN       | WAN | 172.31.30.254  |

| AD-01                 | AD DS / DNS / DHCP   | LAN | 192.168.X.10   |
| Zabbix-01             | Supervision          | LAN | 192.168.X.20   |
| WEB-01                | Serveur web (Apache) | DMZ | 10.0.0.10      |
| OCS-01                |OCS Inventory         | LAN | 192.168.X.40   |


## Postes clients
- Attribution : DHCP
- Plage DHCP : 192.168.X.100 - 192.168.X.200
- Passerelle : 192.168.X.1
- DNS : 192.168.X.10

