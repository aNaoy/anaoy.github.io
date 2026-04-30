---
title: 'New Python Backdoor Uses Tunneling Service to Steal Browser and Cloud Credentials'
date: 2026-04-30
permalink: /posts/2026/04/30/new-python-backdoor-uses-tunneling-service-to-steal-browser-and-cloud-credentials/
tags:
- veille-cyber
- hackernews
---
### Analyse du logiciel malveillant DEEP#DOOR

**Points clés**
*   **Nature de la menace :** DEEP#DOOR est un framework de porte dérobée (backdoor) basé sur Python, conçu pour l'espionnage et l'accès persistant.
*   **Vecteur d'attaque :** Utilisation probable de campagnes de phishing déployant un script batch (`install_obf.bat`) qui désactive les protections Windows pour extraire et exécuter le payload.
*   **Infrastructure C2 :** Le malware détourne le service de tunnelisation légitime **bore.pub** pour établir ses communications, évitant ainsi le recours à une infrastructure dédiée et masquant son trafic.
*   **Ciblage :** Bien que limité et ciblé pour le moment, le framework est modulaire et adaptable, posant un risque pour tout type d'environnement.
*   **Évasion :** Intègre des techniques avancées pour contourner l'analyse (détection de VM/Sandbox), masquer les logs, corrompre les traces ETW, et désactiver Microsoft Defender.

**Vulnérabilités exploitées**
*   Aucune CVE spécifique n'est mentionnée ; le malware exploite des fonctionnalités natives du système (WMI, registres, tâches planifiées) et manipule des composants de sécurité (AMSI, ETW) pour maintenir sa présence.

**Capacités de vol de données**
*   Identifiants de navigateurs (Chrome, Firefox).
*   Clés SSH et identifiants stockés dans le Gestionnaire d'identification Windows.
*   Identifiants Cloud (AWS, Google Cloud, Azure).
*   Surveillance via keylogging, accès webcam, micro et capture d'écran.

**Recommandations de sécurité**
*   **Surveillance des processus :** Détecter l'exécution de scripts batch suspects créant des tâches planifiées ou modifiant les clés de registre `Run`.
*   **Contrôle des accès :** Restreindre l'exécution de scripts Python et PowerShell non signés ou non approuvés par l'entreprise.
*   **Sécurisation des endpoints :** Maintenir une solution EDR (Endpoint Detection and Response) à jour capable de détecter les comportements d'évasion (patching de mémoire AMSI/ETW, techniques de "unhooking" de NTDLL).
*   **Gestion des accès cloud :** Renforcer les politiques d'authentification multifacteur (MFA) pour tous les accès aux consoles cloud, car le vol de jetons d'identification est une cible majeure du malware.
*   **Analyse réseau :** Surveiller les connexions sortantes inhabituelles vers des services de tunnelisation tiers comme `bore.pub`.

---
[Source](https://thehackernews.com/2026/04/new-python-backdoor-uses-tunneling.html){:target="_blank"}
