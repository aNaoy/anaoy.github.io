---
title: 'Chinese Hackers Abused Google Workspace Rules to Steal Research and Defense Emails'
date: 2026-06-16
permalink: /posts/2026/06/16/chinese-hackers-abused-google-workspace-rules-to-steal-research-and-defense-emails/
tags:
- veille-cyber
- hackernews
---
### Espionnage via REDCap et détournement des règles Google Workspace

Le groupe de cyberespionnage **UNC6508**, lié à la Chine, a infiltré pendant plus d'un an des réseaux académiques, médicaux et militaires en Amérique du Nord. L'attaque a permis l'exfiltration massive de données sensibles, notamment sur la stratégie militaire, l'IA et la recherche médicale, en exploitant les fonctionnalités natives des infrastructures ciblées.

**Points clés :**
* **Vecteur d'entrée :** Compromission de serveurs REDCap (Research Electronic Data Capture) exposés sur Internet.
* **Malware INFINITERED :** Un logiciel malveillant personnalisé qui infecte les fichiers système de REDCap, capture les identifiants de connexion et crée une porte dérobée persistante résistante aux mises à jour.
* **Exfiltration furtive :** Une fois les privilèges d'administrateur obtenus, les attaquants ont détourné les règles de « conformité de contenu » (content compliance rules) de Google Workspace pour copier automatiquement et discrètement les emails contenant des mots-clés spécifiques vers un compte externe.
* **Portée :** Les cibles incluaient des institutions de santé, des centres de recherche, des organismes militaires et des régulateurs de santé.

**Vulnérabilités :**
* Aucune CVE spécifique n'a été publiée à ce jour. L'attaque repose sur l'exploitation de **versions obsolètes de REDCap** laissées actives sur les serveurs, facilitant des attaques par rétrogradation (downgrade attacks).

**Recommandations :**
* **Sécurisation REDCap :** Supprimer les anciennes versions de REDCap plutôt que de les maintenir côte à côte avec les versions actuelles, et maintenir les serveurs exposés à jour.
* **Audit des configurations mail :** Vérifier régulièrement les règles de transfert, de routage et de conformité de contenu dans Google Workspace (ou solutions équivalentes) pour détecter tout transfert anormal vers des domaines externes.
* **Surveillance administrative :** Analyser les journaux d'audit (Audit Logs) pour identifier toute modification suspecte des règles de messagerie.
* **Renforcement des accès :** Implémenter une authentification multifacteur (MFA) résistante au phishing pour tous les comptes disposant de privilèges d'administration.

---
[Source](https://thehackernews.com/2026/06/chinese-hackers-abused-google-workspace.html){:target="_blank"}
