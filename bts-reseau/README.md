# BTS Réseau — Maquette d’infrastructure

## Objectif
Mettre en place une maquette réseau niveau BTS avec des services d’infrastructure (ex: AD/DNS/DHCP), une segmentation simple et de la supervision.

## Périmètre (ce qui est fait)
- Domaine Active Directory (utilisateurs, groupes, OU si applicable).
- Services réseau : DNS / DHCP (si tu l’as fait).
- Sécurité : pare-feu + règles principales (NAT/ACL si applicable).
- Supervision : outil de monitoring + alertes/dashboards de base.
- Documentation et tests de validation.

## Architecture
- Schéma réseau : [diagrammes/schema-bts.png](./diagrammes/schema-bts.png)
- Plan d’adressage : [docs/plan-adressage.md](./docs/plan-adressa
## Technologies / Stack
- Virtualisation : ...
- OS/Services : Windows Server (AD), Linux, ...
- Supervision : ...
- Pare-feu : ...

## Validation (preuves)
- Tests réalisés : ping, résolution DNS, attribution DHCP, accès aux services, règles FW.
- Captures / logs : dossier `preuves/` (optionnel).

## Limites / À améliorer
Ex: pas de haute dispo, pas de PRA, maquette mono-site, etc.

## Contact
Email : prenom.nom [at] domaine [dot] fr

