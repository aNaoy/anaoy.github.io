---
title: 'Malicious Script Delivering More Maliciousness, (Wed, Feb 4th)'
date: 2026-02-05
permalink: /posts/2026/02/05/malicious-script-delivering-more-maliciousness-wed-feb-4th/
tags:
- veille-cyber
- sans-isc
---
**Un Script Malveillant Déploie un Trojan de Vol de Données via des Images et Telegram**

Une campagne de phishing utilise un script malveillant pour télécharger et exécuter un programme .NET conçu pour voler des informations. Ce script, dérivé de dépôts publics, incorpore des techniques d'obfuscation pour masquer son code, notamment en utilisant des caractères "poubelles" dans des chaînes Base64.

La charge utile initiale est récupérée depuis une image PNG située sur un serveur web. Cependant, cette image contient en réalité des données délimitées, extraites via des balises spécifiques. Ces données représentent un shellcode qui, une fois décodé (utilisant une technique de décodage inversé et de nettoyage hexadécimal, potentiellement avec l'aide d'outils comme ChatGPT), révèle un programme .NET.

Ce programme .NET vise à établir une persistance sur le système infecté en créant une tâche planifiée (`schtasks.exe`) nommée "Chromiumx2". Il utilise ensuite Telegram comme canal de commande et de contrôle (C2) pour communiquer avec les attaquants, leur envoyant des informations système détaillées comme le nom d'utilisateur, le nom complet du système d'exploitation, le type de processeur, la quantité de RAM, et le groupe auquel le malware appartient (identifié ici comme "XWorm V7.1"). Il s'agit d'une méthode d'infection élaborée où un script malveillant sert de lanceur pour un autre programme malveillant.

**Points Clés :**

*   **Technique d'Obfuscation :** Utilisation de caractères "poubelles" dans des chaînes Base64 pour masquer le code.
*   **Livraison par Image :** Utilisation d'une image PNG comme conteneur pour une charge utile exécutable.
*   **Persistance :** Création d'une tâche planifiée pour assurer une exécution continue.
*   **Canal C2 :** Utilisation de Telegram pour la communication avec les attaquants.
*   **Malware Identifié :** Le payload final est identifié comme faisant partie de la famille XWorm.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article, mais la technique repose sur l'exécution de scripts et le téléchargement de charges utiles, ce qui exploite la confiance des utilisateurs dans les e-mails et les fichiers joints, ainsi que la capacité des systèmes à exécuter des fichiers téléchargés depuis des sources non fiables.

**Recommandations :**

*   Soyez vigilant face aux e-mails inattendus contenant des pièces jointes, même si elles semblent provenir de sources légitimes.
*   Évitez d'ouvrir des pièces jointes ou de cliquer sur des liens dans des e-mails suspects.
*   Maintenez vos logiciels antivirus et antimalware à jour pour détecter et bloquer les menaces connues.
*   Appliquez les mises à jour de sécurité pour votre système d'exploitation et vos applications afin de corriger les vulnérabilités potentielles.
*   Désactivez l'exécution automatique des scripts lorsque cela est possible ou renforcez les politiques de sécurité associées.

---
[Source](https://isc.sans.edu/diary/rss/32682){:target="_blank"}
