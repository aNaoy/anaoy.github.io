---
title: 'New CIFSwitch Linux flaw gives root on multiple distributions'
date: 2026-05-30
permalink: /posts/2026/05/30/new-cifswitch-linux-flaw-gives-root-on-multiple-distributions/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité CIFSwitch : Élévation de privilèges dans le noyau Linux

Une faille de sécurité critique, baptisée **CIFSwitch**, a été identifiée dans le sous-système CIFS du noyau Linux. Cette vulnérabilité permet à un utilisateur local non privilégié d'usurper des requêtes d'authentification Kerberos (`cifs.spnego`) et d'obtenir les droits `root` en manipulant le processus `cifs.upcall`.

**Points clés :**
*   **Origine :** Le noyau Linux ne vérifie pas correctement si les requêtes `cifs.spnego` proviennent légitimement du client CIFS du noyau.
*   **Mécanisme :** Un attaquant peut forcer un changement d'espace de noms (namespace switch) et déclencher une recherche NSS (Name Service Switch) pour charger un module malveillant avant l'abandon des privilèges.
*   **Historique :** La vulnérabilité est présente depuis 2007, bien que son exploitabilité dépende de la configuration système (version du noyau, `cifs-utils`, espaces de noms utilisateur et politiques SELinux/AppArmor).

**Vulnérabilités :**
*   **CVE :** Aucune CVE n'a été explicitement mentionnée dans le texte, mais le correctif est associé au commit amont du noyau Linux `3da1fdf`.

**Distributions impactées (configurations par défaut) :**
*   Linux Mint 21.3 / 22.3, CentOS Stream 9, Rocky Linux 9, AlmaLinux 9, Kali Linux (versions 2021.4 à 2026.1) et SLES 15 SP7. 
*   D'autres distributions (Ubuntu, Debian, etc.) sont vulnérables si le paquet `cifs-utils` est installé.

**Recommandations :**
*   **Mise à jour :** Appliquer les correctifs du noyau fournis par les mainteneurs de la distribution.
*   **Durcissement :** 
    *   Désactiver ou mettre sur liste noire (blacklist) le module `cifs` s'il n'est pas utilisé.
    *   Désinstaller le paquet `cifs-utils` si nécessaire.
    *   Désactiver les espaces de noms utilisateur (user namespaces) si les besoins métier le permettent.
*   **Validation :** Utiliser le PoC (Proof-of-Concept) publié par le chercheur Asim Viladi Oglu Manizada pour vérifier l'exposition du système.

---
[Source](https://www.bleepingcomputer.com/news/security/new-cifswitch-linux-flaw-gives-root-on-multiple-distributions/){:target="_blank"}
