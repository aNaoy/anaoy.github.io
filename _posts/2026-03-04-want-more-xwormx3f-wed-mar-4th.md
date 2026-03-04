---
title: 'Want More XWorm&#x3f;, (Wed, Mar 4th)'
date: 2026-03-04
permalink: /posts/2026/03/04/want-more-xwormx3f-wed-mar-4th/
tags:
- veille-cyber
- sans-isc
---
### Nouvelle campagne de XWorm : techniques d'infection évoluées

Une nouvelle vague de propagation du malware XWorm a été observée, démontrant l'ingéniosité des acteurs malveillants dans leurs méthodes de diffusion. Cette nouvelle variante utilise une approche multi-technologique pour infecter les systèmes.

Le processus d'infection débute par un script JavaScript, intentionnellement obscurci, qui, une fois exécuté dans un environnement contrôlé (sandbox), dépose un script PowerShell dans un répertoire temporaire. Ce script PowerShell, après avoir décodé un payload via Base64 et XOR, invoque une autre commande PowerShell en mémoire.

Le payload final, une DLL, exporte une fonction nommée "ProcessHollowing". Elle agit comme un chargeur, injectant le client XWorm dans le processus du compilateur .NET.

**Points Clés :**

*   **Multi-technologie :** Utilisation combinée de JavaScript, PowerShell et DLL.
*   **Techniques d'injection :** Le malware utilise la technique du "Process Hollowing" pour se dissimuler.
*   **C2 récurrent :** L'adresse IP du serveur de commande et de contrôle (C2) a déjà été observée dans des campagnes antérieures.
*   **Configuration extraite :** Inclut l'adresse C2, des indicateurs d'installation ("USB.exe"), une clé AES, le nom de la règle ("Xworm"), un mutex et la version du malware ("XWorm V6.4").

**Vulnérabilités :**

L'article ne mentionne pas explicitement de vulnérabilités spécifiques identifiées par des identifiants CVE. L'infection repose sur l'exécution de code malveillant via des vecteurs d'ingénierie sociale (impliqués par le type de fichier initial, bien que non détaillé ici) et l'exploitation de la capacité d'exécution de scripts sur le système cible.

**Recommandations :**

Bien que l'article ne fournisse pas de liste exhaustive de recommandations, les pratiques générales de cybersécurité s'appliquent :

*   **Vigilance face aux e-mails et fichiers suspects :** Être particulièrement prudent avec les pièces jointes et les liens provenant de sources inconnues ou inattendues, même s'ils semblent légitimes.
*   **Solutions de sécurité à jour :** Maintenir à jour les antivirus, les systèmes de détection d'intrusion et les pare-feux.
*   **Gestion des scripts :** Mettre en place des politiques pour limiter l'exécution non autorisée de scripts, notamment PowerShell.
*   **Analyse de code malveillant :** Utiliser des environnements sandbox pour analyser les fichiers suspects avant de les exécuter.

**Indicateurs de Compromission (IOCs) :**

*   **Fichiers :**
    *   `Inv-4091-CBM-4091-CUSTOM-Packing_List.js` (SHA256: `5140b02a05b7e8e0c0afbb459e66de4d74f79665c1d83419235ff0cdcf046e9c`)
    *   `ps_5uGUQcco8t5W_1772542824586.ps1` (SHA256: `5a3d33efaaff4ef7b7d473901bd1eec76dcd9cf638213c7d1d3b9029e2aa99a4`)
    *   `MAD.dll` (SHA256: `af3919de04454af9ed2ffa7f34e4b600b3ce24168f745dba4c372eb8bcc22a21`)
    *   `payload.exe` (XWorm) (SHA256: `58e38fffb78964300522d89396f276ae0527def8495126ff036e57f0e8d3c33b`)
*   **Serveur C2 :** `204[.]10[.]160[.]190:7003`

---
[Source](https://isc.sans.edu/diary/rss/32766){:target="_blank"}
