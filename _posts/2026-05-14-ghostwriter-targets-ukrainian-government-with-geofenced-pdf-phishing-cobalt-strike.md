---
title: 'Ghostwriter Targets Ukrainian Government With Geofenced PDF Phishing, Cobalt Strike'
date: 2026-05-14
permalink: /posts/2026/05/14/ghostwriter-targets-ukrainian-government-with-geofenced-pdf-phishing-cobalt-strike/
tags:
- veille-cyber
- hackernews
---
### Nouvelles offensives du groupe Ghostwriter contre les institutions ukrainiennes

Le groupe de menace persistante avancée (APT) **Ghostwriter** (également connu sous les noms de FrostyNeighbor, UNC1151 ou TA445) intensifie ses cyberopérations contre le secteur gouvernemental ukrainien depuis mars 2026. Ce groupe se distingue par une grande maturité opérationnelle et une capacité d'adaptation constante de ses vecteurs d'attaque.

**Points clés :**
*   **Mode opératoire :** La campagne repose sur du *spear-phishing* utilisant des documents PDF malveillants usurpant l'identité de l'opérateur ukrainien Ukrtelecom.
*   **Géoblocage :** Les attaquants emploient une technique de filtrage géographique (geofencing) : les victimes situées hors d'Ukraine reçoivent un document PDF légitime, tandis que les cibles locales reçoivent la charge utile malveillante.
*   **Chaîne d'infection :** L'ouverture du lien dans le PDF déclenche le téléchargement d'une archive RAR contenant une version JavaScript de **PicassoLoader**. Ce dernier profile la machine de la victime et transmet les données aux serveurs des attaquants toutes les 10 minutes, permettant une validation manuelle avant le déploiement final de **Cobalt Strike**.
*   **Diversification des menaces :** Parallèlement, d'autres acteurs comme **Gamaredon** exploitent la vulnérabilité **CVE-2025-8088** contre les institutions ukrainiennes, tandis que des groupes comme **BO Team** et **Hive0117** mènent des opérations distinctes ciblant respectivement des infrastructures russes et des systèmes comptables.

**Vulnérabilités mentionnées :**
*   **CVE-2023-38831** (Score CVSS 7.8) : Vulnérabilité WinRAR exploitée précédemment pour le déploiement de malwares.
*   **CVE-2024-42009** (Score CVSS 9.3) : Flaille XSS dans Roundcube utilisée pour le vol d'identifiants de messagerie.
*   **CVE-2025-8088** : Vulnérabilité utilisée par le groupe Gamaredon pour propager des archives malveillantes.

**Recommandations de sécurité :**
*   **Vigilance sur les pièces jointes :** Sensibiliser les utilisateurs aux risques liés aux documents PDF et aux archives RAR, même lorsqu'ils semblent provenir d'organismes de confiance.
*   **Filtrage réseau et EDR :** Déployer des solutions de détection et de réponse (EDR) capables d'identifier les comportements suspects de scripts (JavaScript/VBScript) et d'isoler les processus liés à Cobalt Strike.
*   **Mise à jour des systèmes :** Appliquer les correctifs de sécurité pour toutes les applications critiques, notamment les logiciels de compression (WinRAR) et les clients de messagerie (Roundcube), afin d'éliminer les vecteurs d'exécution de code à distance.
*   **Gestion des accès :** Imposer l'authentification multifacteur (MFA) sur tous les comptes de messagerie pour prévenir le vol d'identifiants et l'utilisation ultérieure des boîtes mails compromises comme outils de propagation.

---
[Source](https://thehackernews.com/2026/05/ghostwriter-targets-ukrainian.html){:target="_blank"}
