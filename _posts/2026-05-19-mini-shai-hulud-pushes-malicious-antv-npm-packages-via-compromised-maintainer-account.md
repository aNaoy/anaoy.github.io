---
title: 'Mini Shai-Hulud Pushes Malicious AntV npm Packages via Compromised Maintainer Account'
date: 2026-05-19
permalink: /posts/2026/05/19/mini-shai-hulud-pushes-malicious-antv-npm-packages-via-compromised-maintainer-account/
tags:
- veille-cyber
- hackernews
---
### Propagation massive de logiciels malveillants via l'écosystème @antv sur npm

Une campagne d'attaque par empoisonnement de la chaîne d'approvisionnement logicielle, orchestrée par le groupe « Mini Shai-Hulud », a compromis des centaines de paquets npm, principalement ceux de l'écosystème `@antv` et des bibliothèques populaires comme `echarts-for-react`.

**Points clés :**
* **Méthodologie :** Compromission d'un compte de maintenance permettant la publication automatisée et rapide de versions vérolées.
* **Volume :** 323 paquets uniques infectés via 639 versions malveillantes en un laps de temps très court (environ 22 minutes).
* **Charge utile :** Un « stealer » sophistiqué capable de dérober plus de 20 types d'identifiants (AWS, GCP, Azure, GitHub, Kubernetes, etc.) et de tenter des évasions de conteneurs Docker.
* **Complexité accrue :** L'utilisation de jetons volés pour falsifier des attestations Sigstore (SLSA), rendant les paquets malveillants indiscernables des versions légitimes.
* **Source ouverte :** Le groupe TeamPCP a rendu public le code source de l'outil, facilitant l'émergence de clones et compliquant l'attribution.

**Vulnérabilités :**
* Aucune CVE spécifique n'est attribuée, car l'attaque repose sur l'abus de privilèges légitimes (accès au compte npm et jetons CI/CD volés).
* **Vecteurs :** Utilisation de hooks `preinstall` et de dépendances optionnelles pour injecter et exécuter le code malveillant.

**Recommandations :**
* **Rotation immédiate :** Changer tous les identifiants et secrets potentiellement exposés dans les environnements de CI/CD et les services cloud.
* **Audit de sécurité :** Rechercher sur GitHub la chaîne de caractères `niaga og ew ereh :duluh-iahs` (associée à la création de dépôts par les jetons volés).
* **Protection des comptes :** Activer systématiquement l'authentification à deux facteurs (2FA) sur npm et GitHub pour tous les comptes de maintenance.
* **Gestion des dépendances :** Auditer les dépendances pour identifier les versions compromises et migrer vers des versions saines et vérifiées.
* **Vigilance CI/CD :** Restreindre les privilèges des jetons utilisés dans les pipelines d'automatisation (principe du moindre privilège).

---
[Source](https://thehackernews.com/2026/05/mini-shai-hulud-pushes-malicious-antv.html){:target="_blank"}
