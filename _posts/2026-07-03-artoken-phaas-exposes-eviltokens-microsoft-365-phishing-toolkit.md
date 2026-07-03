---
title: 'ARToken PhaaS exposes EvilTokens Microsoft 365 phishing toolkit'
date: 2026-07-03
permalink: /posts/2026/07/03/artoken-phaas-exposes-eviltokens-microsoft-365-phishing-toolkit/
tags:
- veille-cyber
- bleepingcomp
---
### ARToken : L'extension automatisée des attaques par "Device Code Phishing"

La plateforme de Phishing-as-a-Service (PhaaS) « ARToken » a été identifiée comme une filiale du service EvilTokens. Elle se spécialise dans le vol de jetons d'authentification Microsoft 365 en exploitant le flux d'autorisation par code d'appareil (OAuth 2.0 Device Authorization Grant). Ce kit permet aux cybercriminels de contourner l'authentification multifacteur (MFA) et d'automatiser les fraudes par compromission d'e-mails professionnels (BEC).

**Points clés :**
*   **Fonctionnement :** Les victimes sont incitées à entrer un code d'appareil légitime sur un portail Microsoft contrefait, permettant aux attaquants de récupérer des jetons d'accès directs.
*   **Automatisation :** ARToken intègre des outils d'IA pour rédiger des campagnes BEC, traduire des messages et gérer les accès persistants (Primary Refresh Tokens - PRT).
*   **Capacités étendues :** La plateforme permet la surveillance en temps réel de boîtes mail, l'exfiltration de données SharePoint/OneDrive, et la configuration automatique de règles de transfert ou de suppression de mails pour masquer l'intrusion.
*   **Infrastructure :** Le service utilise les *Cloudflare Workers* pour déployer des pages de phishing adaptatives selon la localisation de la victime.

**Vulnérabilités exploitées :**
*   Il ne s'agit pas d'une vulnérabilité logicielle isolée avec CVE, mais d'un détournement du flux **OAuth 2.0 Device Authorization Grant** de Microsoft. En manipulant l'utilisateur pour qu'il s'authentifie via le flux légitime de Microsoft, l'attaquant reçoit les jetons d'accès, rendant les contrôles MFA traditionnels inefficaces.

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs aux risques spécifiques du "device code phishing" (ne jamais saisir un code d'appareil reçu par e-mail ou provenant d'une source non sollicitée).
*   **Sécurité comportementale :** Déployer des solutions d'IA comportementale capables de détecter les anomalies dans les accès aux boîtes mail et les activités suspectes post-authentification.
*   **Gestion des accès :** Restreindre l'utilisation de l'authentification par code d'appareil aux cas d'usage strictement nécessaires et monitorer les accès persistants (PRT) suspects.
*   **Visibilité :** Utiliser des outils de simulation de brèches pour tester la réactivité des systèmes SIEM et EDR face à ces techniques d'accès non autorisés.

---
[Source](https://www.bleepingcomputer.com/news/security/artoken-phaas-exposes-eviltokens-microsoft-365-phishing-toolkit/){:target="_blank"}
