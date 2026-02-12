# BTS Réseau — Maquette d’infrastructure

## Objectif
Mettre en place une maquette réseau niveau BTS avec des services d’infrastructure (ex: AD/DNS/DHCP), une segmentation simple et de la supervision.

## Périmètre (ce qui est fait)
- Domaine Active Directory (utilisateurs, groupes, OU si applicable).
- Services réseau : DNS / DHCP 
- Sécurité : pare-feu + règles principales.
- Supervision : outil de monitoring + alertes/dashboards de base.
- Documentation et tests de validation.

## Architecture
- Schéma réseau : [diagramme/schema-bts.png](./diagramme/schema-reseau.png)
- Plan d’adressage : [docs/plan-adressage.md](./docs/plan-adressa.md)
- 
## Technologies / Stack
- Virtualisation : Vmware / VirtualBox
- OS/Services : Windows Server (AD), Linux (debian,ubuntu,kali linux)
- Supervision : Zabbix
- Ticketing : OCS Inventory
- Serveur Web : Apache
- Pare-feu : Opnsense

## Validation (preuves)
- Tests réalisés : ping, résolution DNS, attribution DHCP, GPO, accès aux services, règles FireWall, alertes Zabbix, 

## Limites / À améliorer
Serveur de ticketing pas assez configuré / Aucune configuraton Pare-Feu (paramètre par défaut) / Aucun Vlan / Le serveur Zabbix pouvait être amélioré (alerting par téléphone, manque de monitoring)

## Contact
Email : noa.fiore [at] proton [dot] me

