---
title: 'Another day, another malicious JPEG, (Mon, Feb 23rd)'
date: 2026-02-24
permalink: /posts/2026/02/24/another-day-another-malicious-jpeg-mon-feb-23rd/
tags:
- veille-cyber
- sans-isc
---
**Campagne Malveillante : De l'e-mail au RAT via des Fichiers Obfusqués**

Une nouvelle campagne de diffusion de logiciels malveillants a été identifiée, exploitant des techniques d'obfuscation pour dissimuler sa charge utile. L'infection débute par un e-mail d'apparence légitime, usurpant l'identité d'une entreprise tchèque. Malgré les tentatives de tromperie (logo, adresse d'expéditeur falsifiée), des contrôles comme DMARC/SPF auraient dû le signaler comme suspect.

L'e-mail contient une pièce jointe sous forme de fichier JScript, remarquablement volumineux (1.17 Mo) en raison d'une première couche d'obfuscation massive. Après nettoyage, le script se réduit à 34 lignes, dont une tentative de persistance basique en copiant le fichier dans le dossier de démarrage.

L'analyse du code résiduel, en travaillant de la fin vers le début, révèle la construction d'une commande PowerShell. Cette commande utilise `Win32_Process.Create` pour lancer une instance PowerShell cachée qui décode un contenu Base64 à partir d'une variable (`whatsamatta`) et l'exécute via `Invoke-Expression`.

La variable `whatsamatta` contient elle-même du code Base64, masqué par une chaîne de caractères aléatoires. Après désobscuration et décodage, ce code révèle une URL d'où le prochain stade du malware est censé être téléchargé. Bien que l'URL initiale renvoyait vers un fichier JPEG (nommé `MSI_PRO_with_b64.png` ou `optimized_msi.png`), le contenu de ce fichier est constitué de données Base64.

Ces données Base64, une fois décodées, révèlent une liste d'arguments destinés à un autre script. Parmi ces arguments, on trouve des indications d'utilisation du dossier de téléchargements et de la ligne de commande Windows. Un argument particulier, une chaîne inversée et encodée en Base64, mène à une URL encore active pointant vers un fichier `.txt`.

Ce fichier texte contient un fichier exécutable (EXE) encodé en Base64 et inversé. L'analyse sur VirusTotal confirme que ce fichier EXE est une variante du **Remcos RAT** (Remote Access Trojan), constituant ainsi le stade final présumé de cette chaîne d'infection.

**Points Clés :**

*   **Technique d'infection :** E-mail de phishing avec pièce jointe JScript.
*   **Obfuscation :** Utilisation de techniques d'obfuscation multiples et de grande échelle pour masquer le code.
*   **Chainage :** Implication de plusieurs étapes pour livrer la charge utile finale.
*   **Outils utilisés par l'attaquant :** JScript, PowerShell, WMI (`Win32_Process.Create`), Base64, Remcos RAT.
*   **Fichiers impliqués :** Fichier JScript (1er étage), fichier JPEG/PNG contenant des données Base64 (2ème étage), fichier TXT contenant un EXE encodé (3ème étage), fichier EXE Remcos RAT (charge utile finale).

**Vulnérabilités :**

*   Aucune vulnérabilité logicielle spécifique (CVE) n'est explicitement mentionnée dans le texte. La campagne exploite des fonctionnalités système légitimes (PowerShell, WMI) et des techniques d'ingénierie sociale.

**Recommandations :**

*   **Vigilance accrue face aux e-mails :** Ne pas ouvrir de pièces jointes provenant de sources inconnues ou suspectes.
*   **Vérification des en-têtes d'e-mails :** Examiner les en-têtes pour détecter des incohérences (par exemple, échec des contrôles SPF/DMARC).
*   **Solutions de sécurité :** Utiliser des antivirus et des solutions de sécurité e-mail capables de détecter les scripts malveillants et les chaînes d'infection complexes.
*   **Analyse des scripts :** Disposer d'outils et de compétences pour analyser les scripts obfusqués et en extraire la logique.
*   **Mises à jour :** Maintenir les systèmes d'exploitation et les logiciels à jour pour corriger les éventuelles vulnérabilités exploitables.

---
[Source](https://isc.sans.edu/diary/rss/32738){:target="_blank"}
