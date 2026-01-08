---
title: 'ThreatsDay Bulletin: RustFS Flaw, Iranian Ops, WebUI RCE, Cloud Leaks, and 12 More Stories'
date: 2026-01-08
permalink: /posts/2026/01/08/threatsday-bulletin-rustfs-flaw-iranian-ops-webui-rce-cloud-leaks-and-12-more-stories/
tags:
- veille-cyber
- hackernews
---
## Panorama des Menaces Cyber Sécurité : Tendances et Alertes

Cette semaine, le paysage des menaces cyber met en lumière l'évolution rapide des tactiques des attaquants, l'exploitation de vulnérabilités communes et l'émergence de nouvelles menaces. Les attaques ciblent aussi bien les infrastructures critiques que les utilisateurs individuels, avec une tendance à l'automatisation et à l'utilisation de techniques sophistiquées pour contourner les défenses.

**Points Clés et Vulnérabilités :**

*   **GeoServer Exploité pour le Minage de Cryptomonnaies :** La vulnérabilité CVE-2024-36401 dans GeoServer est activement exploitée pour déployer des mineurs de cryptomonnaies (XMRig) et d'autres malwares, permettant potentiellement l'installation d'autres menaces ou le vol de données.
*   **Augmentation des Vulnérabilités Connues et Exploité :** Le catalogue CISA KEV a connu une expansion significative en 2025 avec l'ajout de 245 vulnérabilités, dont certaines datent de 2002, exploitées notamment par des groupes de ransomware. Les principaux éditeurs concernés incluent Microsoft, Apple et Cisco.
*   **Risque de Code Exécution dans Open WebUI :** La fonctionnalité de Connexions Directes dans Open WebUI (versions antérieures à 0.6.35), sous CVE-2025-64496, présente un risque de prise de contrôle de compte et d'exécution de code à distance (RCE) si un utilisateur est redirigé vers un serveur malveillant.
*   **Faiblesse Critique dans RustFS :** Une vulnérabilité critique non identifiée par CVE dans RustFS (versions alpha.13 à alpha.77) permet une authentification via un token statique prévisible, ouvrant la voie à la destruction de données, la manipulation de politiques et la modification de la configuration du cluster.
*   **Sophistication Croissante des Phishing Kits :** Le nombre de kits de phishing-as-a-service (PhaaS) a doublé en 2025, avec des fonctionnalités avancées comme le contournement de l'authentification multifacteur (MFA), des techniques d'obfuscation et l'utilisation de QR codes malveillants.
*   **Exécution de Code dans Zed IDE :** Deux vulnérabilités de gravité élevée (CVE-2025-68433 et CVE-2025-68432) dans Zed IDE exposent les développeurs à l'exécution de code arbitraire lors de l'interaction avec des dépôts de code malveillants, notamment via la confiance implicite dans les configurations MCP et LSP.
*   **Attaques Cybercriminelles de Grande Échelle :** Les attaques attribuées à des groupes iraniens (MuddyWater) évoluent, utilisant des backdoors dédiés comme Phoenix et UDPGangster à travers des exécutables déguisés. Des campagnes de malvertising et de SEO poisoning utilisent des packers comme pkr_mtsi pour distribuer divers types de malwares.
*   **Augmentation des Menaces sur les Infrastructures Critiques :** Les attaques contre le secteur énergétique de Taïwan ont été multipliées par dix en 2025, attribuées à des groupes cybercriminels chinois. Les cyberattaques sur les hôpitaux ont également été une cible notable.

**Vulnérabilités Spécifiques (avec CVE lorsque disponible) :**

*   **CVE-2024-36401 :** GeoServer (exploitation pour distribution de cryptomineurs).
*   **CVE-2007-0671 :** Microsoft Office Excel Remote Code Execution.
*   **CVE-2002-0367 :** Windows NT/2000 "smss.exe" privilege escalation.
*   **RustFS Hardcoded Token Vulnerability :** Non CVE, CVSS 9.8 (versions alpha.13 à alpha.77).
*   **CVE-2025-64496 :** Open WebUI (versions 0.6.34 et antérieures), CVSS 7.3.
*   **CVE-2025-68433 :** Zed IDE (MCP settings), CVSS 7.8.
*   **CVE-2025-68432 :** Zed IDE (LSP configurations), CVSS 7.8.

**Recommandations :**

*   **Mise à jour et Patch Management :** Maintenir les systèmes à jour est crucial pour corriger les vulnérabilités connues, notamment celles ajoutées au catalogue CISA KEV.
*   **Activation de l'Authentification Multifacteur (MFA) :** L'activation de l'MFA est une mesure essentielle pour contrer les attaques basées sur des identifiants compromis, comme souligné par les alertes sur ownCloud.
*   **Vigilance face aux Techniques d'Ingénierie Sociale :** Une vigilance accrue est nécessaire face aux malvertising, SEO poisoning et aux kits de phishing qui exploitent la confiance des utilisateurs.
*   **Sécurisation des Déploiements :** Pour les projets comme RustFS, il est impératif de revoir les mécanismes d'authentification pour éviter l'utilisation de tokens statiques prévisibles.
*   **Protection des Infrastructures Critiques :** Les organisations gérant des infrastructures critiques doivent renforcer leurs défenses contre les attaques ciblées.
*   **Connaissance des Risques Logiciels :** Les développeurs doivent être conscients des risques liés à l'intégration de certaines fonctionnalités, comme le chargement automatique de configurations ou la confiance implicite dans des sources externes (ex: Zed IDE, Open WebUI).
*   **Utilisation de Solutions de Sécurité :** L'utilisation de solutions de sécurité avancées, incluant la détection et la réponse aux menaces, est recommandée pour identifier et neutraliser les activités malveillantes.

---
[Source](https://thehackernews.com/2026/01/threatsday-bulletin-rustfs-flaw-iranian.html){:target="_blank"}
