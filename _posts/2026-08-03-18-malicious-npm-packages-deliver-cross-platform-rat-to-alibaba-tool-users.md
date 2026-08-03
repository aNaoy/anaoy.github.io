---
title: '18 Malicious npm Packages Deliver Cross-Platform RAT to Alibaba Tool Users'
date: 2026-08-03
permalink: /posts/2026/08/03/18-malicious-npm-packages-deliver-cross-platform-rat-to-alibaba-tool-users/
tags:
- veille-cyber
- hackernews
---
### Attaque sophistiquée par empoisonnement de la supply chain npm ciblant Alibaba

Des chercheurs en cybersécurité ont identifié 18 paquets npm malveillants conçus pour déployer un cheval de Troie d'accès à distance (RAT) multiplateforme. Cette campagne cible spécifiquement les développeurs utilisant des outils internes du groupe Alibaba. En usurpant l'identité de paquets privés (scope `@ali`), les attaquants exploitent le mécanisme de résolution des dépendances pour injecter un code malveillant capable d'espionnage industriel.

**Points clés :**
*   **Méthodologie :** Utilisation de paquets « leurres » qui téléchargent, via un moteur de règles, des charges utiles secondaires depuis des serveurs distants.
*   **Ciblage :** L'attaque détecte le système d'exploitation de la victime (Windows, Linux, macOS) pour adapter ses techniques de persistance et d'exécution.
*   **Impact :** Le malware peut compromettre des applications professionnelles (DingTalk, Wukong), exfiltrer des données, exécuter des commandes arbitraires et réaliser des mouvements latéraux.
*   **Origine probable :** Les indices techniques (commentaires en chinois, fuseau horaire UTC+08:00) suggèrent un acteur malveillant sinophone.

**Vulnérabilités :**
Il ne s'agit pas de failles logicielles classiques (CVE), mais d'une exploitation du **typosquatting** et de **l'empoisonnement de la supply chain** (compromission de comptes de mainteneurs ou publication de paquets malveillants usurpant des noms de confiance).

**Recommandations :**
*   **Audit immédiat :** Rechercher la présence des 18 paquets identifiés dans les environnements de développement (ex: `lib-mtop`, `aone-kit`, `smart-config-manager`, etc.).
*   **Rotation des accès :** En cas de détection, considérer le système comme compromis. Réinitialiser immédiatement tous les identifiants et clés API depuis une machine saine.
*   **Sécurisation :** Renforcer la vigilance sur les dépendances ajoutées aux projets et isoler les environnements de build pour limiter les risques de mouvement latéral.

---
[Source](https://thehackernews.com/2026/08/18-malicious-npm-packages-deliver-cross.html){:target="_blank"}
