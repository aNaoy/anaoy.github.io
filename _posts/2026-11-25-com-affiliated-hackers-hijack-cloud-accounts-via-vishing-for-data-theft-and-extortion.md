---
title: 'Com-Affiliated Hackers Hijack Cloud Accounts via Vishing for Data Theft and Extortion'
date: 2026-11-25
permalink: /posts/2026/11/25/com-affiliated-hackers-hijack-cloud-accounts-via-vishing-for-data-theft-and-extortion/
tags:
- veille-cyber
- hackernews
---
### Vague de cyberattaques par "vishing" et compromission de comptes cloud

Des groupes de cybercriminels affiliés à "Com" mènent depuis août 2026 des campagnes sophistiquées de vol de données et d'extorsion ciblant divers secteurs (finance, santé, services juridiques) aux États-Unis, au Royaume-Uni et en Australie. Ces attaquants utilisent le **vishing** (phishing vocal) pour se faire passer pour le support informatique interne et diriger les employés vers des pages de phishing personnalisées.

**Points clés :**
*   **Mode opératoire :** Utilisation de kits de phishing "Adversary-in-the-Middle" (AiTM) comme *Doko's Panel* pour intercepter en temps réel les identifiants et les jetons de session MFA.
*   **Persistance :** Une fois l'accès obtenu, les attaquants enregistrent leurs propres dispositifs MFA, créent des identifiants temporaires et autorisent des applications OAuth malveillantes.
*   **Exfiltration et extorsion :** Utilisation de scripts Python ou du SDK Microsoft Graph pour extraire massivement des données (SharePoint, OneDrive, mails). Les victimes sont ensuite contactées via Microsoft Teams pour des demandes de rançon.
*   **Outillage avancé :** Déploiement d'extensions de navigateur malveillantes (sideloading) capables d'enregistrer des frappes clavier, de voler des cookies de session, de capturer des flux webcam et de prendre le contrôle à distance via le protocole Chrome DevTools.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique ne soit mentionnée, la vulnérabilité réside dans la **faiblesse des processus d'authentification humaine** face au social engineering (vishing) et dans la capacité des kits AiTM à contourner les protections MFA classiques.

**Recommandations :**
*   **Renforcer l'authentification :** Privilégier les méthodes d'authentification résistantes au phishing (comme les clés de sécurité physiques FIDO2) plutôt que les notifications push SMS ou applications classiques, facilement interceptables par les kits AiTM.
*   **Surveillance proactive :** Auditer régulièrement les accès OAuth tiers autorisés, les nouvelles inscriptions de dispositifs MFA et les modifications suspectes apportées aux règles de messagerie ou aux alertes de sécurité cloud.
*   **Sensibilisation :** Former les employés à la méfiance envers les appels entrants non sollicités, même s'ils semblent provenir du support informatique interne.
*   **Sécurité des postes :** Restreindre la possibilité d'installer des extensions de navigateur non approuvées et surveiller l'activation du "Mode Développeur" sur les navigateurs basés sur Chromium.

---
[Source](https://thehackernews.com/2026/11/com-affiliated-hackers-hijack-cloud.html){:target="_blank"}
