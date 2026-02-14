# Architecture

## Objectif
Décrire la topologie de la maquette BTS, les zones réseau, les composants et les flux principaux.

## Schéma
[Schéma réseau](../diagramme/schema-reseau.png)

## Zones réseau
- LAN : (ex: 192.168.10.0/24) — postes + serveurs internes.
- WAN : accès Internet via OPNsense. (Etant dans un établissement scolaire, le wan de mon pare-feu etait le lan du pare-feu du lycée )
- DMZ : (ex: 10.0.0.0/24) — services exposés (serveur web)

## Composants (rôles)
- OPNsense : pare-feu, filtrage, routage entre interfaces.
- AD (Windows Server) : domaine, DNS, DHCP, GPO.
- Serveur Web (Apache) : hébergement du site/service web.
- Zabbix : supervision (disponibilité, services, alertes).
- OCS inventory :  inventaire et suivi du parc informatique (postes/serveurs, matériel/logiciels).
- Postes clients : postes du LAN (tests + utilisation des services).

## Flux principaux
- Clients LAN → AD/DNS/DHCP : authentification, résolution de noms, attribution d’IP.
- WAN → Serveur Web : autorisé uniquement en HTTP/HTTPS (80/443).
- Zabbix → serveurs/clients : collecte des métriques (ICMP/agent).

## Liens utiles
- Plan d’adressage : [plan-adressage.md](./plan-adressage.md)
- README projet : [../README.md](../README.md)

