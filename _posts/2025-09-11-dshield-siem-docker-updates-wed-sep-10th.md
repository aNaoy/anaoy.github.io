---
title: 'DShield SIEM Docker Updates, (Wed, Sep 10th)'
date: 2025-09-11
permalink: /posts/2025/09/11/dshield-siem-docker-updates-wed-sep-10th/
tags:
- veille-cyber
- sans-isc
---
**Mise à jour du SIEM DShield et de ses capteurs Honeypot**

Des améliorations ont été apportées à DShield SIEM et à la collection de données des capteurs webhoneypot. L'interface a été mise à jour pour faciliter l'analyse des données des capteurs DShield, avec un tableau de bord principal qui regroupe les outils d'analyse sur la gauche.

**Points Clés et Évolutions :**

*   **Mise à jour ELK (Elastic Stack) :**
    *   Le port TCP 5601 n'est plus utilisé, l'accès se fait désormais via `https://IP`.
    *   Tous les paquets Elastic ont été mis à jour vers la version 8.19.3.
    *   Le parser Logstash pour le webhoneypot a été mis à jour.
    *   La page d'analyse web DShield a été actualisée.
    *   La supervision ELK utilise Metricbeat.
    *   Intégration de 2 flux de renseignements sur les menaces (Threat Intel) exécutés via cronjob sur le serveur ELK.
    *   Inclusion de règles de détection d'activité web ISC.
    *   Les pages de dépannage pour Cowrie et Docker ont été mises à jour.
    *   Une liste de scripts d'anciens étudiants du programme BACS de SANS.edu a été ajoutée.

*   **Outils d'Analyse supplémentaires :**
    *   Deux nouvelles applications ont été ajoutées à la page d'activité principale de Kibana :
        *   CyberChef
        *   Mitre ATT&CK - Attack Navigator
    *   Ces outils sont installés via Docker lors de la mise à jour vers la version actuelle.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans cet article. L'accent est mis sur les mises à jour et les améliorations fonctionnelles.

**Recommandations :**

Pour mettre à jour vers la version actuelle, il est conseillé de suivre les étapes suivantes :
1.  Se déplacer dans le répertoire `DShield-SIEM`.
2.  Arrêter les conteneurs Docker avec `sudo docker compose stop`.
3.  Récupérer les dernières modifications avec `git pull --autostash`.
4.  Supprimer les anciens conteneurs avec `sudo docker compose rm -f -v`.
5.  Reconstruire et démarrer les conteneurs avec `sudo docker compose up --build -d`.

Après la mise à jour, il est nécessaire de charger les nouveaux modèles dans Kibana en exécutant :
1.  `sudo docker exec -ti filebeat bash`
2.  `./filebeat setup -e`

---
[Source](https://isc.sans.edu/diary/rss/32276){:target="_blank"}
