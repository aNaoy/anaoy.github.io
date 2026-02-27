---
title: 'Fake Fedex Email Delivers Donuts&#x21;, (Fri, Feb 27th)'
date: 2026-02-27
permalink: /posts/2026/02/27/fake-fedex-email-delivers-donutsx21-fri-feb-27th/
tags:
- veille-cyber
- sans-isc
---
## Campagne de Malwares : "Livraison Fedex"

Une campagne de phishing imitant des notifications de livraison Fedex a été observée. L'email joint une archive "fedex_shipping_document.7z" contenant un script batch (.bat) conçu pour établir une persistance et exécuter une charge utile PowerShell.

### Points Clés :

*   **Technique d'Obfuscation:** Le script batch utilise des variables d'environnement étendues de manière différée (`!var!`) et l'activation de `setlocal enableDelayedExpansion` pour contourner les recherches simples de variables.
*   **Charge Utile PowerShell:** La charge utile initiale, encodée en Base64, est ensuite décodée et exécutée via une ligne de commande PowerShell. Cette charge utile recherche la présence d'un processus "explorer" avant de continuer.
*   **Double Chiffrement:** La charge utile PowerShell déchiffre ensuite une autre charge utile (shellcode) préalablement chiffrée avec AES, utilisant les IV et sels extraits du script.
*   **Injection et Persistance:** Le shellcode obtenu est injecté dans le processus `explorer.exe` et une nouvelle thread est lancée, typique du comportement du malware DonutLoader.
*   **Communication C2:** Le shellcode communique avec un serveur de commande et contrôle (C2) à l'adresse `204[.]10[.]160[.]190:7003`, identifié comme étant XWorm.

### Vulnérabilités :

*   Aucune vulnérabilité logicielle spécifique (avec numéro CVE) n'est directement exploitée. L'attaque repose sur l'ingénierie sociale (convaincre l'utilisateur d'ouvrir l'archive) et l'exécution de scripts malveillants.

### Recommandations :

*   **Sensibilisation des utilisateurs:** Informer les utilisateurs sur les risques des emails de phishing, en particulier ceux concernant des livraisons et demandant l'ouverture de pièces jointes ou d'archives.
*   **Analyse des pièces jointes:** Ne jamais ouvrir de pièces jointes ou d'archives provenant d'expéditeurs non fiables ou dont la nature n'est pas claire.
*   **Solutions de sécurité:** Utiliser et maintenir à jour des solutions antivirus/antimalware capables de détecter les scripts suspects et les charges utiles connues.
*   **Surveillance des processus:** Mettre en place une surveillance des processus pour détecter les injections inhabituelles dans des processus légitimes comme `explorer.exe`.
*   **Blocage des C2:** Bloquer les communications vers les adresses IP et les ports connus pour héberger des serveurs C2 de malwares.

---
[Source](https://isc.sans.edu/diary/rss/32754){:target="_blank"}
