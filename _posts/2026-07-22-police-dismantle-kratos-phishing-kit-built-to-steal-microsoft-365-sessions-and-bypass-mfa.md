---
title: 'Police Dismantle Kratos Phishing Kit Built to Steal Microsoft 365 Sessions and Bypass MFA'
date: 2026-07-22
permalink: /posts/2026/07/22/police-dismantle-kratos-phishing-kit-built-to-steal-microsoft-365-sessions-and-bypass-mfa/
tags:
- veille-cyber
- hackernews
---
### Démantèlement du kit de phishing « Kratos » (SneakyLog)

Les autorités allemandes et américaines, en collaboration avec les autorités indonésiennes, ont neutralisé l’infrastructure du service de phishing « Kratos » (également connu sous le nom de **SneakyLog**). Ce service fonctionnait sur un modèle de franchise, permettant à environ 1 800 cybercriminels de mener des campagnes automatisées à grande échelle, visant principalement les comptes Microsoft 365.

**Points clés :**
*   **Mode opératoire :** Utilisation de la technique du "Adversary-in-the-Middle" (AiTM) via un proxy inverse Node.js pour intercepter en temps réel les identifiants et les jetons de session.
*   **Impact :** Des centaines de milliers de victimes dans plus de 30 pays depuis 2024.
*   **Infrastructure :** Plus de 200 serveurs saisis ; les attaquants utilisaient des domaines jetables et des sites WordPress compromis.
*   **Techniques de leurre :** Utilisation de courriels sur le thème des impôts incluant des QR codes renvoyant vers de fausses pages de connexion Microsoft 365.

**Vulnérabilités exploitées :**
*   Le kit exploite le manque de protection contre l'AiTM lors de l'authentification MFA classique. L'acquisition du **cookie de session** permet aux attaquants de contourner le second facteur d'authentification, rendant la simple réinitialisation du mot de passe insuffisante si la session active n'est pas révoquée.
*   *Note : Aucune CVE spécifique n'est associée, il s'agit d'une vulnérabilité logique liée au détournement de jetons de session.*

**Recommandations :**
*   **Révoquer les sessions actives :** En cas de compromission avérée via un proxy inverse, la réinitialisation du mot de passe ne suffit pas ; il est impératif d'invalider les jetons de session existants côté serveur.
*   **Adopter une authentification résistante au phishing :** Migrer les comptes à haut risque vers des méthodes d'authentification matérielles (clés FIDO2/WebAuthn) qui ne sont pas vulnérables aux proxys inverses.
*   **Détection :** Rechercher des traces spécifiques liées à ce kit, notamment le chargement systématique des fichiers `barr.svg` et `lg.svg` sur les pages de connexion suspectes, ainsi que des requêtes POST vers des points de terminaison nommés `next.php` ou `save.php`.

---
[Source](https://thehackernews.com/2026/07/police-dismantle-kratos-phishing-kit.html){:target="_blank"}
