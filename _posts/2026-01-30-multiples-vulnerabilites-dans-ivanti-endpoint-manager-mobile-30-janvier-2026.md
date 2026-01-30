---
title: 'Multiples vulnérabilités dans Ivanti Endpoint Manager Mobile (30 janvier 2026)'
date: 2026-01-30
permalink: /posts/2026/01/30/multiples-vulnerabilites-dans-ivanti-endpoint-manager-mobile-30-janvier-2026/
tags:
- veille-cyber
- certfr
---
### Urgence de sécurité : Exécution de code arbitraire à distance dans Ivanti Endpoint Manager Mobile

Des vulnérabilités critiques ont été identifiées dans Ivanti Endpoint Manager Mobile (EPMM), permettant à un attaquant non authentifié d'exécuter du code à distance sur les systèmes affectés. L'éditeur confirme que ces failles font actuellement l'objet d'exploitations actives dans le cadre d'attaques ciblées.

**Points Clés :**

*   **Risque principal :** Exécution de code arbitraire à distance.
*   **Exploitation active :** Les vulnérabilités sont déjà utilisées par des attaquants.
*   **Méthodes de persistance :** Déploiement de webshells (console web malveillante) et de reverse shells (invite de commande inversée).

**Vulnérabilités :**

*   **CVE-2026-1281**
*   **CVE-2026-1340**

**Systèmes Affectés :**

*   Endpoint Manager Mobile (EPMM) versions 12.5.0.x, 12.5.1.x, 12.6.0.x, 12.6.1.x, 12.7.0.x, si les scripts correctifs appropriés (RPM_12.x.0.x ou RPM_12.x.1.x) ne sont pas appliqués.

**Recommandations :**

**En cas de suspicion de compromission :**

1.  **Isolation immédiate :** Isoler totalement les équipements EPMM et Sentry du réseau (Internet et interne).
2.  **Sauvegarde :** Réaliser un instantané ou une sauvegarde du disque.
3.  **Analyse des journaux :** Rechercher des tentatives d'exploitation dans les journaux d'accès Apache (`/var/log/httpd/https-access_log`) en identifiant les requêtes HTTP GET avec les chemins `/mifs/c/aftstore/fob/` ou `/mifs/c/appstore/fob/` renvoyant un code 404 et contenant des commandes bash.

**En cas de compromission avérée :**

1.  **Restauration :** Restaurer une sauvegarde saine d'EPMM ou recréer une instance EPMM et migrer les données.
2.  **Réinitialisation des identifiants :** Réinitialiser les mots de passe de tous les comptes EPMM locaux, comptes de service LDAP et KDC, et comptes de service internes/externes configurés avec EPMM.
3.  **Gestion des certificats :** Révoquer et remplacer les certificats publics utilisés par EPMM.

**Solutions :**

*   **Application des correctifs :** Télécharger et installer les scripts RPM correctifs 12.x.0.x et 12.x.1.x depuis le portail de téléchargement d'Ivanti.
*   **Mise à jour majeure :** Ces correctifs RPM sont temporaires et doivent être réappliqués à chaque montée de version jusqu'à la version 12.8.0.0 d'Ivanti Endpoint Manager Mobile.

---
[Source](https://www.cert.ssi.gouv.fr/alerte/CERTFR-2026-ALE-001/){:target="_blank"}
