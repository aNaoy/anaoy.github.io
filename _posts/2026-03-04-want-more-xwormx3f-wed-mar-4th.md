---
title: 'Want More XWorm&#x3f;, (Wed, Mar 4th)'
date: 2026-03-04
permalink: /posts/2026/03/04/want-more-xwormx3f-wed-mar-4th/
tags:
- veille-cyber
- sans-isc
---
**Nouvelle Campagne de Distribution du Malware XWorm**

Une nouvelle vague de distribution du malware XWorm, une famille de logiciels malveillants bien connue et largement répandue, a été observée. Cette campagne utilise des techniques de livraison évoluées, démontrant l'ingéniosité des acteurs malveillants.

**Points Clés :**

*   **Multi-technologies :** La campagne emploie une combinaison de JavaScript, PowerShell et une DLL pour délivrer sa charge utile.
*   **Chargement Progressif :** Un script JavaScript obfusqué sert de charge initiale. Il exécute un script PowerShell temporaire qui, après décodage (Base64 + XOR), télécharge et exécute un autre script PowerShell en mémoire.
*   **Injection de Malware :** Le script PowerShell final déclenche une DLL exportant une fonction nommée "ProcessHollowing". Cette DLL agit comme un chargeur, injectant le client XWorm dans le processus du compilateur .Net.
*   **Infrastructure de Commande et Contrôle Réutilisée :** L'adresse IP du serveur de commande et contrôle (C2) utilisée dans cette campagne a déjà été identifiée dans des incidents précédents.
*   **XWorm v6.4 :** La configuration extraite indique la version XWorm V6.4.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est explicitement mentionnée dans le texte, mais le mécanisme d'infection repose sur l'exécution de code malveillant, souvent initiée par des techniques d'ingénierie sociale (non détaillées ici) ou par des vulnérabilités exploitées dans des applications exposées.

**Recommandations :**

*   **Surveillance des Communications C2 :** Maintenir une vigilance accrue sur l'infrastructure de commande et contrôle identifiée (204[.]10[.]160[.]190:7003).
*   **Analyse des Fichiers Suspects :** Examiner les fichiers aux indicateurs de compromission (IoCs) fournis, tels que les hachages SHA256 :
    *   `5140b02a05b7e8e0c0afbb459e66de4d74f79665c1d83419235ff0cdcf046e9c` (Inv-4091-CBM-4091-CUSTOM-Packing_List.js)
    *   `5a3d33efaaff4ef7b7d473901bd1eec76dcd9cf638213c7d1d3b9029e2aa99a4` (ps_5uGUQcco8t5W_1772542824586.ps1)
    *   `af3919de04454af9ed2ffa7f34e4b600b3ce24168f745dba4c372eb8bcc22a21` (MAD.dll)
    *   `58e38fffb78964300522d89396f276ae0527def8495126ff036e57f0e8d3c33b` (payload.exe - XWorm)
*   **Analyse Comportementale :** Utiliser des environnements sandbox pour analyser le comportement des fichiers suspects et comprendre les étapes d'exécution des malwares, en particulier pour le code obfusqué.
*   **Mises à Jour et Patchs :** Assurer la mise à jour des systèmes d'exploitation et des applications pour corriger les vulnérabilités connues qui pourraient être exploitées.

---
[Source](https://isc.sans.edu/diary/rss/32766){:target="_blank"}
