---
title: 'MongoDB warns admins to patch severe RCE flaw immediately'
date: 2025-12-24
permalink: /posts/2025/12/24/mongodb-warns-admins-to-patch-severe-rce-flaw-immediately/
tags:
- veille-cyber
- bleepingcomp
---
**Urgence de Patch pour une Vulnérabilité Critique de MongoDB**

Une faille de sécurité majeure dans MongoDB, identifiée sous le code CVE-2025-14847, permet des attaques d'exécution de code à distance (RCE) exploitables par des acteurs malveillants non authentifiés avec une faible complexité. Cette vulnérabilité, causée par une mauvaise gestion d'un paramètre de longueur, peut autoriser l'exécution de code arbitraire et le contrôle des systèmes ciblés.

**Points Clés :**

*   **Nature de la Vulnérabilité :** Exécution de code à distance (RCE).
*   **Cause :** Mauvaise gestion d'une incohérence de paramètre de longueur dans l'implémentation zlib du serveur.
*   **Impact :** Permet aux attaquants d'exécuter du code arbitraire et de potentiellement prendre le contrôle des appareils ciblés.
*   **Exploitabilité :** Faible complexité, ne nécessite pas d'interaction utilisateur et peut être exploitée par des attaquants non authentifiés.
*   **Versions Affectées :** Une large gamme de versions de MongoDB, incluant toutes les versions de 8.2.0 à 8.2.3, 8.0.0 à 8.0.16, 7.0.0 à 7.0.26, 6.0.0 à 6.0.26, 5.0.0 à 5.0.31, 4.4.0 à 4.4.29, ainsi que toutes les versions 4.2, 4.0 et 3.6 de MongoDB Server.

**Vulnérabilités :**

*   **CVE-2025-14847 :** Vulnérabilité RCE critique due à une mauvaise gestion du paramètre de longueur dans l'implémentation zlib.
*   *Il est également fait mention d'une précédente vulnérabilité RCE (CVE-2019-101758) qui avait été ajoutée au catalogue de CISA des vulnérabilités connues et exploitées.*

**Recommandations :**

*   **Mise à Jour Immédiate :** Installer impérativement les versions corrigées de MongoDB, notamment : 8.2.3, 8.0.17, 7.0.28, 6.0.27, 5.0.32, ou 4.4.30.
*   **Contournement Temporaire (si la mise à jour n'est pas immédiate) :** Désactiver la compression zlib sur le serveur MongoDB en démarrant `mongod` ou `mongos` avec une option `networkMessageCompressors` ou `net.compression.compressors` qui exclut explicitement zlib.

---
[Source](https://www.bleepingcomputer.com/news/security/mongodb-warns-admins-to-patch-severe-rce-flaw-immediately/){:target="_blank"}
