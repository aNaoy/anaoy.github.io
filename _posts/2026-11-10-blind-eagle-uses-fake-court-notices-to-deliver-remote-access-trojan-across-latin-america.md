---
title: 'Blind Eagle Uses Fake Court Notices to Deliver Remote Access Trojan Across Latin America'
date: 2026-11-10
permalink: /posts/2026/11/10/blind-eagle-uses-fake-court-notices-to-deliver-remote-access-trojan-across-latin-america/
tags:
- veille-cyber
- hackernews
---
### Nouvelle campagne de phishing du groupe Blind Eagle en Amérique latine

Le groupe cybercriminel **Blind Eagle (APT-C-36)** mène une campagne de grande envergure ciblant des organisations en Amérique latine (particulièrement en Colombie) au moyen d'e-mails de phishing imitant des notifications judiciaires, fiscales et administratives. L'objectif est le déploiement d'un cheval de Troie d'accès à distance (RAT) dérivé d'AsyncRAT et de DCRat.

**Points clés :**
*   **Mode opératoire :** Utilisation de fichiers XHTML contenant des images SVG piégées qui déclenchent du « HTML smuggling » pour contourner les passerelles de messagerie.
*   **Technique d'infection :** Les fichiers SVG assemblent localement un archive ZIP contenant un dropper JavaScript.
*   **Évasion :** Le malware intègre des mécanismes de contournement de l'AMSI (Antimalware Scan Interface) et de l'ETW (Event Tracing for Windows), tout en affichant une fausse citation pénale pour détourner l'attention.
*   **Persistance :** Le logiciel malveillant supprime les métadonnées « Mark of the Web » (MotW) et s'installe dans le dossier de démarrage Windows.
*   **Portée :** Près de 3 300 e-mails malveillants ont été identifiés entre fin octobre et début novembre 2026.

**Vulnérabilités exploitées :**
*   **HTML Smuggling :** Technique permettant d'assembler des charges utiles (payloads) directement via le navigateur, rendant les contrôles de sécurité périmétriques inopérants.
*   **Absence de CVE spécifique :** L'attaque repose sur l'ingénierie sociale et l'abus de fonctionnalités légitimes de Windows (PowerShell, VBScript) plutôt que sur l'exploitation d'une faille logicielle répertoriée (CVE).

**Recommandations de sécurité :**
*   **Sensibilisation :** Former les employés à la vigilance face aux e-mails officiels (judiciaires, administratifs) comportant des pièces jointes inhabituelles ou des liens vers des fichiers SVG/XHTML.
*   **Sécurisation du Web :** Bloquer le téléchargement de fichiers potentiellement dangereux (SVG, scripts JS, fichiers ZIP non autorisés) via les passerelles de messagerie et les proxys web.
*   **Endpoints :** Restreindre l'exécution de scripts (PowerShell, VBScript) par des politiques de contrôle d'application (AppLocker ou Windows Defender Application Control).
*   **Monitoring :** Surveiller les processus suspects lancés au démarrage du système et les requêtes PowerShell inhabituelles exécutées en mémoire.

---
[Source](https://thehackernews.com/2026/11/blind-eagle-uses-fake-court-notices-to.html){:target="_blank"}
