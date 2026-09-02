---
title: 'GeoNetwork Fixes Unauthenticated RCE Chain Affecting Government Geoportal Backends'
date: 2026-09-02
permalink: /posts/2026/09/02/geonetwork-fixes-unauthenticated-rce-chain-affecting-government-geoportal-backends/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans GeoNetwork : RCE par chaînage d'exploits

Une chaîne d'exploitation permet l'exécution de code à distance (RCE) non authentifiée sur GeoNetwork, une plateforme open-source utilisée par de nombreux portails géographiques gouvernementaux et institutionnels.

**Points clés :**
* La vulnérabilité affecte les versions 4.4.x jusqu'à 4.4.11 et 4.2.x jusqu'à 4.2.16.
* L'attaque combine le contournement de l'authentification et une mauvaise configuration du moteur de transformation XSLT.
* Plus d'une centaine d'instances exposées ont été identifiées, dont une large majorité appartient à des organismes publics ou militaires.

**Vulnérabilités :**
* **CVE-2026-63219 (Score CVSS 8.6) :** Absence de contrôle d'accès sur le point de terminaison de chargement des formateurs (formatters). Un attaquant peut uploader des fichiers malveillants `.xsl` ou `.zip`.
* **CVE-2026-58400 (Score CVSS 9.1) :** Configuration non sécurisée du processeur Saxon XSLT. Le moteur permet d'exécuter des commandes système via des fonctions Java (`java.lang.Runtime.exec()`) lors du rendu d'un fichier malveillant chargé via la première faille.

**Recommandations :**
* **Mise à jour immédiate :** Passer aux versions **4.4.12** ou **4.2.17** publiées par le projet.
* **Mesures d'atténuation (en attendant la mise à jour) :** Restreindre l'accès au point de terminaison `/geonetwork/srv/api/formatters` via un reverse proxy :
    * **Apache httpd :** Bloquer les méthodes POST, PUT et PATCH.
    * **Nginx :** Restreindre l'accès aux seules méthodes GET, HEAD et OPTIONS.

---
[Source](https://thehackernews.com/2026/09/geonetwork-fixes-unauthenticated-rce.html){:target="_blank"}
