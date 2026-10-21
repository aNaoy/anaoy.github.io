---
title: 'Operation FlashHole: Lazarus breaks security, defies control'
date: 2026-10-21
permalink: /posts/2026/10/21/operation-flashhole-lazarus-breaks-security-defies-control/
tags:
- veille-cyber
- securelist
---
# Opération FlashHole : L'évolution modulaire du groupe Lazarus

Le groupe Lazarus a lancé l'opération « FlashHole », une campagne d'espionnage sophistiquée ciblant principalement les secteurs sud-coréens du logiciel, de la construction et de la fabrication d'équipements de communication. Cette opération se distingue par l'utilisation de sites de phishing conçus par IA (portfolios et CV) pour diffuser des malwares via l'exploitation de logiciels de sécurité financière obligatoires (ex: INISAFE CrossWeb EX).

### Points clés
*   **Stratégie évolutive :** Lazarus réutilise ses outils historiques (TechHub, Cubridge, LPEClient) en les rendant plus modulaires et segmentés pour échapper à la détection.
*   **Infection en mémoire :** La chaîne d'exécution initiale réside uniquement en mémoire pour dissimuler toute compromission sur le disque.
*   **Techniques avancées :** Utilisation intensive du *DLL side-loading* (notamment via `mscoree.dll`), usurpation de processus (PPID spoofing) et utilisation de cryptographie post-quantique (ML-KEM) pour protéger les charges utiles.
*   **C2 décentralisé :** Utilisation de dépôts GitHub (via API), de sites web légitimes compromis et, dans certains cas, de Dropbox comme canaux de commande et de contrôle.

### Vulnérabilités et vecteurs d'attaque
L'article ne mentionne pas de CVE spécifique, mais souligne une vulnérabilité systémique :
*   **Abus de logiciels de sécurité obligatoires :** Les solutions de sécurité financière, nécessaires à l'accès aux services bancaires/gouvernementaux, servent de vecteur d'attaque critique en raison de leur exécution avec des privilèges élevés.
*   **Persistance :** Installation de services malveillants usurpant des noms de services légitimes (svchost) pour maintenir l'accès au système.

### Recommandations et mesures de sécurité
*   **Réduction de la surface d'attaque :** La Corée du Sud prévoit la suppression progressive des logiciels de sécurité obligatoires d'ici 2026 ; les entreprises doivent privilégier des solutions de sécurité conformes aux standards modernes plutôt que des solutions locales propriétaires souvent vulnérables.
*   **Détection comportementale :** Surveiller les exécutions suspectes au sein des processus de logiciels financiers (ex: `INISAFECrossWebEXSvc.exe` lançant des processus système comme `fsquirt.exe`).
*   **Surveillance réseau :** Bloquer ou auditer les communications sortantes vers des services de stockage cloud (GitHub API, Dropbox) initiées par des processus non autorisés ou des binaires système.
*   **Gestion des logs :** Scruter les changements de privilèges (utilisation de `SetFileInformationByHandle`) et l'usurpation de timestamps (MAC times) sur les fichiers système.

---
[Source](https://securelist.com/lazarus-operation-flashhole/121541/){:target="_blank"}
