# Projet Infrastructure DevOps - Automatisation CI/CD & IaC 

  ## Attention : Projet en cours de dévéloppement 


##  Contexte

Encadrement partiel : l’objectif est de concevoir et mettre en œuvre une démarche DevOps de bout en bout, incluant le déploiement d’une application. Dans notre cas, il s’agit d’une application de réservation de mototaxi.

Le projet est réalisé en autonomie : il n’y a pas forcément de composants imposés (outils, stack, architecture), et les choix techniques nous reviennent. Les enseignants interviennent surtout à la demande : si nous rencontrons un blocage ou avons besoin de validation d’orientation, ils nous aiguillent et proposent des pistes, sans fournir une solution complète

---

##  Objectif

Mettre en place une infrastructure DevOps complète avec :
- Provisioning automatisé (Terraform)
- Configuration centralisée (Ansible)
- Pipeline CI/CD (GitLab/Jenkins)
- Orchestration de conteneurs (Kubernetes et docker)
- Segmentation réseau sécurisée (LAN, LAN pré-prod, DMZ)
- Monitoring temps réel (Prometheus/Grafana)

---

##  Architecture

### Vue d'ensemble

Le projet déploie une infrastructure réseau complète avec 3 zones segmentées :

- **LAN (192.168.1.0/24)** : Environnement interne
  - Serveur AD (Active Directory avec le domaine mototaxi.llm
  - Prometheus / Grafana (_A préciser_)
  - Gitlab / Jenkins (_A préciser_)
  - Terraform / Ansible (_A préciser_)
  - Cluster Kubernetes (_A préciser_)
  - Elasticsearch (_A préciser_)
  - PCs clients (192.168.1.20 - 192.168.1.40)
  
- **LAN Pré-prod (10.10.0.0)** : Environnement de validation avant production (Miroir de la DMZ)
  - Docker (conteneurs applicatifs)
  - Serveur Web

- **DMZ (10.0.0.0/24)** : 
  - Docker (conteneurs applicatifs)
  - Serveur Web

### Outils DevOps (Infrastructure LAN)

- **Terraform / Ansible** : Provisioning et configuration (_A préciser_)
- **GitLab / Jenkins** : Pipeline CI/CD
- **Kubernetes / Docker** : Orchestration de conteneurs (cluster production)
- **Prometheus / Grafana** : Monitoring et visualisation (_A préciser_)

### Sécurité & Routage

- **Pare-feu du lycée** : Filtrage entrant (adresse IP publique)
- **Routage WAN/LAN/DMZ** : Analyse de logs et segmentation réseau
- **NAT 192.168 → 10.0.0** : Isolation DMZ

![Architecture réseau (en cours)](docs/architecture.png)
[Schéma réseau](diagramme/schéma-DEVOPS.drawio.png)

---

##  Technologies

| Catégorie | Outils |
|-----------|--------|
| **IaC** | Terraform, Ansible |
| **CI/CD** | GitLab CI / Jenkins |
| **Conteneurs** | Docker, Kubernetes |
| **Serveurs** | Windows Server (AD DS), Linux (Apache, Docker) |
| **Monitoring** | Prometheus, Grafana,|
|**Analyse de logs**| Elasticsearch, |
| **Réseau** | Segmentation VLAN, pare-feu multi-zones, NAT |
| **Versioning** | Git, GitLab |

---

## Prérequis

- En cours de définition.
- Objectif : documenter progressivement les versions/outils nécessaires (Jenkins, Terraform, Ansible, Docker/Kubernetes, monitoring).


