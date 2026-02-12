# BTS Réseau — Maquette d’infrastructure

## Contexte
“Encadrement léger : objectifs et composants imposés (ex. AD/DNS/DHCP, supervision, pare-feu), mais choix d’implémentation et réalisation en autonomie. J’ai conçu l’architecture, installé/configuré les services, validé le fonctionnement et documenté une partie des solutions.”

## Objectif
Mettre en place une maquette réseau niveau BTS avec des services d’infrastructure (ex: AD/DNS/DHCP), une segmentation simple et de la supervision.

## Périmètre (réalisé)
- Active Directory :
  - Mise en place d’un domaine AD.
  - Création/gestion d’utilisateurs, groupes (OU si applicable).
  - GPO (si applicable).
- Services réseau :
  - DNS (résolution interne).
  - DHCP (attribution d’adresses IP).
- Sécurité :
  - Pare-feu OPNsense.
  - Règle WAN permettant uniquement HTTP/HTTPS (ports 80/443) pour l’accès au service web.
- Supervision :
  - Zabbix (monitoring de base, dashboards et alertes simples).
- Services :
  - Serveur web Apache.
- Documentation :
  - Schéma, plan d’adressage, et tests de validation

## Architecture
- Schéma réseau : [diagramme/schema-bts.png](./diagramme/schema-reseau.png)
- Plan d’adressage : [docs/plan-adressage.md](./docs/plan-adressa.md)
  
## Technologies / Stack
- Virtualisation : VMware / VirtualBox
- OS/Services :
  - Windows Server (Active Directory)
  - Linux (Debian, Ubuntu, Kali)
- Supervision : Zabbix
- Inventaire : OCS Inventory
- Serveur Web : Apache
- Pare-feu : OPNsense

## Validation (preuves)
Tests réalisés (avec captures/logs si disponibles) :
- Connectivité : ping entre postes/serveurs.
- DNS : résolution de noms.
- DHCP : attribution d’IP et renouvellement de bail.
- Active Directory :
  - Jonction d’un poste au domaine.
  - Connexion avec un compte du domaine.
  - Application des GPO.
- Pare-feu / WAN :
  - Accès OK en HTTP/HTTPS (80/443) vers le serveur web.
  - Vérification que les autres ports ne sont pas accessibles depuis le WAN.
- Zabbix :
  - Hôtes ajoutés, disponibilité, quelques métriques.
  - Alerte testée (ex : service down / hôte unreachable).

## Limites / À améliorer
- Réseau :
  - Pas de VLAN pour l’instant (à ajouter : segmentation par zones, routage inter-VLAN, ACL).
- Pare-feu :
  - Règles limitées au besoin web (80/443) ; durcissement à compléter (règles plus fines, journalisation, etc.).
- Supervision :
  - Zabbix améliorable : plus de métriques, meilleurs triggers, meilleure couverture, éventuellement escalade/notifications avancées.
- OCS Inventory :
  - Périmètre/paramétrage à approfondir selon l’objectif (inventaire complet, reporting, etc.).


## Contact
Email : noa.fiore [at] proton [dot] me

