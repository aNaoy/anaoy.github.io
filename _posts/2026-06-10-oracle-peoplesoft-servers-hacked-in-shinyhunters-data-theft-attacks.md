---
title: 'Oracle PeopleSoft servers hacked in ShinyHunters data theft attacks'
date: 2026-06-10
permalink: /posts/2026/06/10/oracle-peoplesoft-servers-hacked-in-shinyhunters-data-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'extorsion massive contre les serveurs Oracle PeopleSoft

Le groupe de cybercriminels ShinyHunters mène actuellement une campagne d'extorsion visant les serveurs Oracle PeopleSoft (cloud et sur site). Plus de 100 organisations, principalement dans le secteur de l'éducation, ont été touchées, avec environ 300 instances compromises. Les attaquants utilisent une chaîne d'exploitation combinant des vulnérabilités anciennes et potentielles "zero-day" pour s'introduire dans les réseaux, déployer des outils de gestion à distance (MeshCentral) et exiger des rançons.

**Points clés :**
*   **Objectif :** Vol de données et extorsion financière.
*   **Mode opératoire :** Utilisation de scripts d'automatisation pour scanner le réseau interne, effectuer du "credential spraying" (tentatives de connexion avec des comptes par défaut comme `psoft`, `oracle`, `linuxadm`) et déposer des notes de rançon.
*   **Preuves :** Des chercheurs ont identifié des répertoires exposés contenant les outils des attaquants, confirmant l'utilisation d'adresses IP spécifiques et de certificats TLS liés à ShinyHunters.

**Vulnérabilités :**
*   Bien que le groupe mentionne l'usage d'une chaîne de vulnérabilités ("gadget chain") incluant des failles zero-day, aucune CVE spécifique n'a été officiellement publiée ou confirmée par Oracle à ce stade. L'exploitation semble varier en fonction de la configuration de l'instance cible.

**Recommandations :**
*   **Analyse des logs :** Vérifier immédiatement les journaux de connexion à la recherche de toute activité provenant des adresses IP suivantes : 
    *   `142.11.200.186` à `190`
    *   `108.174.202.99`
    *   `176.120.22.24`
*   **Sécurisation immédiate :** En cas de détection d'activité suspecte ou de présence du fichier `README-IF-YOU-SEE-THIS-YOUVE-BEEN-HACKED.TXT`, isoler les serveurs affectés de l'accès public (Internet) sans délai.
*   **Audit de configuration :** Désactiver les comptes par défaut non utilisés et renforcer les méthodes d'authentification SSH pour limiter les tentatives de brute force.
*   **Réponse à incident :** Engager une procédure d'investigation approfondie pour déterminer l'étendue de la compromission si des indicateurs de compromission (IOC) sont identifiés.

---
[Source](https://www.bleepingcomputer.com/news/security/oracle-peoplesoft-servers-hacked-in-shinyhunters-data-theft-attacks/){:target="_blank"}
