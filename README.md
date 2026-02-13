# 📂 Centralisation et Redirection de Dossiers (Active Directory & GPO)

![Version](https://img.shields.io/badge/Windows_Server-2022-blue)
![Platform](https://img.shields.io/badge/VirtualBox-7.0-orange)
![IaC](https://img.shields.io/badge/Infrastructure_as_Code-Vagrant-purple)

Ce dépôt contient l'intégralité des travaux réalisés pour la mise en œuvre d'une infrastructure de centralisation des données utilisateurs. Le projet repose sur un contrôleur de domaine Windows Server 2022 et une stratégie de groupe (GPO) de redirection de dossiers.

## 📄 Documentation Principale
Le rapport complet de 25 pages détaillant chaque étape de la configuration, les captures d'écran et les phases de test est disponible ici :
👉 **[Consulter le Rapport d'Étape (PDF)](./rapport_etape.pdf)**

---

## 🚀 Déploiement Automatisé (Vagrant)
Pour tester cette infrastructure sans configuration manuelle, j'ai inclus un `Vagrantfile`. Il permet de monter l'environnement réseau en une seule commande.

### Architecture déployée :
* **Serveur (SRVADVAR01)** : Windows Server 2022 | IP: `192.168.88.5`
* **Client (WIN01)** : Windows 10 Pro | IP: `192.168.88.10` (DNS: `192.168.88.5`)

### Instructions :
1. Installer [VirtualBox](https://www.virtualbox.org/) et [Vagrant](https://www.vagrantup.com/).
2. Ouvrir un terminal dans ce dossier et taper :
   ```bash
   vagrant up
