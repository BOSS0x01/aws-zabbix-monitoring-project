# AWS Zabbix Monitoring Project

## Présentation

Ce projet met en œuvre une infrastructure de supervision centralisée sur AWS, utilisant Zabbix (via Docker) pour monitorer un parc hybride Linux & Windows. Il inclut la configuration réseau, le déploiement des instances, l'installation de Zabbix et des agents, et la visualisation des métriques.

---

## Architecture

![Schéma d'architecture](screenshots/architecture.png)

---

## Étapes principales

### 1. Accès AWS & Création du VPC

![AWS Console](screenshots/AWS%20Console%20dashboard.png)

Création d'un VPC dédié pour isoler l'environnement de supervision.

![VPC créé](screenshots/vpc%20created.png)

### 2. Sous-réseau, Passerelle Internet & Routage

![Subnet créé](screenshots/subnet%20created.png)

![Internet Gateway](screenshots/internet%20gatway%20created.png)

![Table de routage](screenshots/route%20table%20created.png)

![Route modifiée](screenshots/route%20edited.png)

![Association subnet-route table](screenshots/subnet%20associated%20with%20route%20table.png)

### 3. Groupes de sécurité

![SG Zabbix](screenshots/zabbix%20server%20security%20groupe%20.png)

![SG Linux](screenshots/linux%20security%20groupe%20.png)

![SG Windows](screenshots/windows%20security%20groupe%20.png)

![Association SG-VPC](screenshots/associating%20all%20security%20grooups%20with%20vpc.png)

### 4. Déploiement des instances EC2

![Zabbix Instance](screenshots/zabbix%20instance.png)

![Linux Instance](screenshots/linux%20instance.png)

![Windows Instance](screenshots/windows%20instance%20.png)

![Toutes les instances running](screenshots/all%20instances%20running%20.png)

### 5. Installation & Configuration du serveur Zabbix

Connexion SSH :

![SSH Zabbix](screenshots/connect%20to%20ssh%20zabix%20server.png)

![SSH Established](screenshots/connected%20to%20ssh%20zabix%20server.png)

Installation Docker & Compose :

![Docker installé](screenshots/docker%20has%20been%20installed.png)

![Docker Compose installé](screenshots/docker%20compose%20has%20been%20installed.png)

Déploiement Zabbix via Docker Compose :

![docker-compose.yml](screenshots/docker%20compose%20file.png)

![Conteneurs running](screenshots/contrainers%20running.png)

### 6. Accès à l'interface Zabbix

![Login Zabbix](screenshots/zabbix%20interface%20login%20accessible.png)

![Première vue Zabbix](screenshots/first%20look%20into%20zabbix%20interface.png)

### 7. Configuration des clients

#### Linux

![SSH Linux](screenshots/connected%20to%20linux%20ssh.png)

![Agent configuré](screenshots/configured%20zabbix%20agent.png)

![Agent actif](screenshots/zabbix%20agent%20working.png)

#### Windows

![RDP Windows](screenshots/connected%20to%20windows%20instance%20via%20rdp%20.png)

![Zabbix installé Windows](screenshots/installed%20zabbix%20in%20windows%20.png)

![Agent configuré Windows](screenshots/configured%20zabbix%20agent.png)

### 8. Ajout des hôtes dans Zabbix

![Ajout agents](screenshots/ADDED%20AGENTS%20TO%20ZABBIX%20INTERFACE.png)

![Agent opérationnel](screenshots/zabbix%20agent%20working.png)

### 9. Supervision & Tableaux de bord

![Dashboard Zabbix](screenshots/dashboard.png)

![Monitoring Ubuntu](screenshots/client_ubunto_monitoring.png)

![Monitoring Windows](screenshots/client_windows_monitoring.jpg)

---

## Conclusion

Ce projet démontre la mise en place d'une supervision efficace sur AWS avec Zabbix, couvrant la configuration réseau, le déploiement automatisé, l'intégration d'agents et la visualisation graphique des métriques. Toutes les étapes sont illustrées par des captures d'écran pour faciliter la reproduction.

---

## Auteur & Remerciements

Encadrant : Prof. Azeddine KHIAT  
Année universitaire : 2025/2026

---

## Liens utiles

- [Documentation Zabbix](https://www.zabbix.com/documentation/current/manual/)
- [AWS Academy](https://aws.amazon.com/training/awsacademy/)
- [Dépôt GitHub du projet](https://github.com/yourusername/aws-zabbix-monitoring-project)
