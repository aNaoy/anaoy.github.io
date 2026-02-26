---
title: 'UAT-10027 Targets U.S. Education and Healthcare with Dohdoor Backdoor'
date: 2026-02-26
permalink: /posts/2026/02/26/uat-10027-targets-us-education-and-healthcare-with-dohdoor-backdoor/
tags:
- veille-cyber
- hackernews
---
## Campagne de cyberattaque : Dohdoor cible les secteurs de l'éducation et de la santé aux États-Unis

Une campagne malveillante, désignée sous le nom d'UAT-10027, cible depuis fin 2025 les institutions éducatives et de santé américaines. L'objectif principal est le déploiement d'une nouvelle porte dérobée (backdoor) nommée Dohdoor.

### Points clés

*   **Cible :** Secteurs de l'éducation et de la santé aux États-Unis.
*   **Malware principal :** Dohdoor, une porte dérobée inédite.
*   **Communication :** Utilisation du protocole DNS-over-HTTPS (DoH) pour les communications de commande et de contrôle (C2), permettant de contourner les systèmes de détection basés sur le DNS.
*   **Technique d'exécution :** Utilisation de DLL légitimes renommer "propsys.dll" ou "batmeter.dll" et chargées via DLL side-loading par des exécutables Windows valides ("Fondue.exe", "mblctr.exe", "ScreenClippingHost.exe").
*   **Charge utile suivante :** L'implant Dohdoor télécharge et exécute en mémoire un autre payload, identifié comme étant un Cobalt Strike Beacon.
*   **Masquage des serveurs C2 :** Utilisation de l'infrastructure Cloudflare pour faire apparaître le trafic malveillant comme du trafic HTTPS légitime.
*   **Contournement des défenses :** Dohdoor peut déconnecter des appels système pour éviter la détection par les solutions EDR qui se basent sur des hooks user-mode dans NTDLL.dll.
*   **Acteur potentiel :** Des similarités tactiques ont été observées avec LazarLoader, associé au groupe Lazarus. Cependant, la cible privilégiée par UAT-10027 (éducation et santé) diffère du profil habituel de Lazarus (cryptomonnaies, défense). Des groupes nord-coréens ont déjà ciblé ces secteurs par le passé.
*   **Absence d'exfiltration de données :** Aucune preuve d'exfiltration de données n'a été constatée à ce jour.

### Vulnérabilités exploitées

L'article ne détaille pas de vulnérabilités spécifiques avec des identifiants CVE. Cependant, les techniques employées suggèrent l'exploitation de :

*   **Ingénierie sociale / Phishing :** Probablement utilisée pour obtenir l'exécution initiale d'un script PowerShell.
*   **Exécution de code à distance :** Permise par la porte dérobée Dohdoor pour télécharger et exécuter d'autres payloads.
*   **DLL Side-loading :** Technique permettant à un logiciel de charger une DLL malveillante à la place d'une DLL légitime portant le même nom, souvent stockée dans le même répertoire.

### Recommandations

Bien que l'article se concentre sur l'analyse de la menace, les pratiques suivantes sont implicitement recommandées pour se défendre contre ce type d'attaque :

*   **Renforcer la sécurité des emails :** Vigilance accrue face aux tentatives de phishing et de spear-phishing.
*   **Surveillance du trafic réseau :** Mise en place de solutions de détection avancées, capables d'identifier les communications C2 déguisées (même si DoH complique cela).
*   **Détection et réponse sur les points d'extrémité (EDR) :** Utilisation de solutions EDR capables de détecter les comportements suspects, y compris les tentatives de contournement des hooks système.
*   **Gestion rigoureuse des privilèges :** Limiter les droits d'accès pour réduire l'impact potentiel d'une compromission.
*   **Veille sur les nouvelles menaces :** Rester informé des campagnes malveillantes émergentes et des tactiques des acteurs de menaces.
*   **Mises à jour et correctifs :** S'assurer que tous les systèmes et logiciels sont à jour pour corriger les vulnérabilités connues.

---
[Source](https://thehackernews.com/2026/02/uat-10027-targets-us-education-and.html){:target="_blank"}
