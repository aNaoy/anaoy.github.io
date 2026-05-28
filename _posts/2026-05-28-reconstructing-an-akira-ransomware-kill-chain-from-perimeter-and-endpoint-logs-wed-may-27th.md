---
title: 'Reconstructing an Akira Ransomware Kill Chain from Perimeter and Endpoint Logs, (Wed, May 27th)'
date: 2026-05-28
permalink: /posts/2026/05/28/reconstructing-an-akira-ransomware-kill-chain-from-perimeter-and-endpoint-logs-wed-may-27th/
tags:
- veille-cyber
- sans-isc
---
### Analyse et reconstruction de la chaîne d'attaque du ransomware Akira

Une intrusion récente attribuée au groupe Akira démontre que la compromission repose sur des techniques classiques exploitant des accès négligés. L'analyse, réalisée exclusivement à partir des logs pare-feu (VPN) et des journaux d'événements Windows (EVTX), met en évidence une chaîne d'attaque prévisible mais dévastatrice.

**Points clés de l'intrusion**
*   **Vecteur initial :** Brute-force sur un compte local VPN non désactivé, dépourvu de MFA, dont l'équivalent AD avait été supprimé.
*   **Découverte et énumération :** Utilisation de commandes standards (`nltest`, `net group`, `whoami`, `AdFind`) pour cartographier le domaine.
*   **Escalade et mouvement latéral :** Kerberoasting de comptes de service, suivi de connexions RDP (Logon Type 10) vers des serveurs critiques et contrôleurs de domaine.
*   **Impact :** Suppression des clichés instantanés (`vssadmin`) pour empêcher la restauration, effacement des logs (`EID 1102`) et déploiement du chiffrement.

**Vulnérabilités exploitées**
L'attaque ne repose pas sur des failles 0-day, mais sur des mauvaises configurations critiques :
*   **Comptes locaux orphelins :** Comptes VPN actifs non synchronisés avec l'annuaire Active Directory (déprovisionnement incomplet).
*   **Absence de MFA :** Accès distant sans authentification multi-facteurs.
*   **Kerberoasting :** Utilisation de chiffrements faibles (RC4) pour les comptes de service.
*   **Audit insuffisant :** Taille par défaut des logs Windows trop faible, entraînant la perte des preuves avant investigation.

**Recommandations de sécurité**
*   **Gestion des accès :** Inventorier et supprimer tous les comptes locaux inutilisés sur le pare-feu ; imposer le MFA sur tous les accès VPN.
*   **Surveillance proactive :** 
    *   Alerter sur plus de 50 échecs de connexion VPN en une heure par source.
    *   Détecter les requêtes de tickets Kerberos (EID 4769) utilisant RC4 pour plusieurs SPN.
    *   Monitorer l'exécution de `vssadmin` et `wmic` pour supprimer des clichés.
*   **Politique de logs :** Augmenter la taille des journaux de sécurité (1 Go minimum) et centraliser les logs (EID 1102, 4688) sur un serveur distant.
*   **Synchronisation temporelle :** Aligner tous les équipements (pare-feu et serveurs) sur une source NTP unique pour corréler efficacement les événements.
*   **Réponse à incident :** Créer une corrélation entre les logs périmétriques (VPN) et les journaux internes (Windows) en utilisant l'adresse IP source comme pivot.

---
[Source](https://isc.sans.edu/diary/rss/33024){:target="_blank"}
