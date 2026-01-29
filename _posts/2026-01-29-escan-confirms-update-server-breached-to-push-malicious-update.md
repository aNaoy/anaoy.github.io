---
title: 'eScan confirms update server breached to push malicious update'
date: 2026-01-29
permalink: /posts/2026/01/29/escan-confirms-update-server-breached-to-push-malicious-update/
tags:
- veille-cyber
- bleepingcomp
---
### Serveur de mise à jour d'eScan compromis

Un serveur de mise à jour régional de l'antivirus eScan a été compromis le 20 janvier 2026, permettant la distribution d'une mise à jour non autorisée à un petit nombre de clients. L'accès non autorisé à la configuration d'un serveur de mise à jour régional a conduit à l'insertion d'un fichier incorrect dans le chemin de distribution des mises à jour.

**Points Clés:**

*   **Nature de l'incident :** Compromission d'une infrastructure de mise à jour, pas d'une vulnérabilité du produit eScan lui-même.
*   **Période affectée :** Une fenêtre de deux heures le 20 janvier 2026 pour les clients téléchargeant des mises à jour depuis le serveur régional concerné.
*   **Détection et notification :** eScan affirme avoir détecté l'incident en interne le même jour, isolé l'infrastructure compromise et publié un avis de sécurité le 21 janvier. La société de sécurité Morphisec a également signalé une activité malveillante détectée le 20 janvier.
*   **Impact sur les clients :** Les clients ayant installé la mise à jour malveillante ont pu rencontrer des échecs de service de mise à jour, des modifications du fichier hosts, des problèmes de réception des définitions de sécurité et des notifications d'indisponibilité des mises à jour.
*   **Actions correctives :** L'infrastructure affectée a été isolée et reconstruite. Les identifiants d'authentification ont été réinitialisés. Une mise à jour de remédiation est disponible pour corriger les modifications incorrectes et rétablir la fonctionnalité de mise à jour.

**Vulnérabilités :**

*   L'article ne mentionne pas de CVE spécifique pour cette attaque. La vulnérabilité réside dans l'accès non autorisé à la configuration d'un serveur de mise à jour régional.

**Recommandations :**

*   Les clients concernés doivent exécuter la mise à jour de remédiation fournie par eScan pour identifier et corriger les modifications incorrectes, rétablir la fonctionnalité de mise à jour et vérifier la restauration du système.
*   Il est recommandé de bloquer les serveurs de commande et de contrôle identifiés :
    *   `hxxps[://]vhs[.]delrosal[.]net/i`
    *   `hxxps[://]tumama[.]hns[.]to`
    *   `hxxps[://]blackice[.]sol-domain[.]org`
    *   `hxxps[://]codegiant[.]io/dd/dd/dd[.]git/download/main/middleware[.]ts`
    *   `504e1a42.host.njalla[.]net`
    *   `185.241.208[.]115`

---
[Source](https://www.bleepingcomputer.com/news/security/escan-confirms-update-server-breached-to-push-malicious-update/){:target="_blank"}
