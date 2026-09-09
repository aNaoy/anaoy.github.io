---
title: 'Hackers breach F5 BIG-IP APM devices to deploy Linux rootkit'
date: 2026-09-09
permalink: /posts/2026/09/09/hackers-breach-f5-big-ip-apm-devices-to-deploy-linux-rootkit/
tags:
- veille-cyber
- bleepingcomp
---
### Rootkit « PoisonedRefresh » : Menace persistante sur les équipements F5 BIG-IP

Des attaquants exploitent les systèmes F5 BIG-IP APM pour déployer un rootkit Linux sophistiqué, identifié sous le nom de « PoisonedRefresh ». Ce malware agit comme une charge utile de second niveau, injectant un web shell directement en mémoire sans modifier les fichiers sur le disque, rendant la détection extrêmement difficile.

**Points clés :**
*   **Infiltration en mémoire :** Le rootkit intercepte le chargement des modules PHP (via l'accrochage d'`apr_dso_load`) pour injecter un web shell dans des scripts légitimes (`apm_css.php3`, `full_wt.php3`, etc.).
*   **Techniques furtives :** Le malware manipule les configurations SELinux, assure sa persistance à travers les mises à jour du système et dissimule son activité en utilisant des réponses HTTP 201 déguisées en contenu CSS.
*   **Communication locale :** Un socket UNIX local, protégé par mot de passe, permet de lancer un shell Bash interactif sans ouvrir de port TCP externe, limitant l'exposition réseau.
*   **Furtivité temporelle :** L'implant retarde son exécution au démarrage d'Apache pour s'aligner sur les processus normaux et éviter de déclencher des alertes de sécurité.

**Vulnérabilité exploitée :**
*   **CVE-2025-53521 :** Une vulnérabilité critique d'exécution de code à distance (RCE) sur les dispositifs F5 BIG-IP APM, initialement classée comme un problème de DoS, qui sert de vecteur d'accès initial.

**Recommandations :**
*   **Correction immédiate :** Appliquer les correctifs de sécurité fournis par F5 pour remédier à la faille CVE-2025-53521.
*   **Surveillance des anomalies :** Rechercher des comportements suspects, notamment :
    *   Processus Apache accédant à `/proc/self/maps` ou modifiant les protections mémoire de `libphp`.
    *   Création de fichiers anormaux comme `/run/bigtlog.pipe`.
    *   Lancement inattendu de `/bin/bash` par les processus du serveur web.
*   **Analyse du trafic :** Inspecter les requêtes POST vers les terminaux `.php3` et identifier les réponses PHP renvoyant un code HTTP 201 avec un type de contenu `text/css`.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-breach-f5-big-ip-apm-devices-to-deploy-linux-rootkit/){:target="_blank"}
