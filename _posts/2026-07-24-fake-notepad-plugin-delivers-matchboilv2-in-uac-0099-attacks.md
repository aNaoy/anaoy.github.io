---
title: 'Fake Notepad++ Plugin Delivers MATCHBOIL.V2 in UAC-0099 Attacks'
date: 2026-07-24
permalink: /posts/2026/07/24/fake-notepad-plugin-delivers-matchboilv2-in-uac-0099-attacks/
tags:
- veille-cyber
- hackernews
---
### Espionnage cybernétique : Campagnes malveillantes russes contre des cibles stratégiques

**Points clés**
*   **Menace UAC-0099 :** Ce groupe lié à la Russie utilise une fausse extension pour Notepad++ afin de compromettre des systèmes Windows. L'attaque commence par un phishing dirigeant vers un fichier ZIP contenant un script VBScript, lui-même déguisé en document PDF. Le script déploie une charge utile appelée `MATCHBOIL.V2`.
*   **Tactique de distraction :** L'exécution du malware affiche un faux PDF à l'utilisateur pendant qu'une version légitime de Notepad++ charge une DLL malveillante (`NppExport.dll`) pour établir une persistance via une tâche planifiée.
*   **Espionnage par messagerie :** Parallèlement, des groupes comme *Laundry Bear* (TA488) et TA458 mènent des campagnes d'espionnage sur des serveurs mail (Zimbra, Roundcube, Kerio, SOGo). Ils exploitent des techniques de type "half-click" (affichage d'un email compromis sans interaction utilisateur requise) pour déployer des backdoors.

**Vulnérabilités identifiées**
*   **CVE-2025-66376 :** Exploité pour injecter le malware *ZimReaper* sur les serveurs Zimbra.
*   **CVE-2025-49113 :** Utilise le gestionnaire de téléchargement de fichiers de Roundcube pour déclencher une désérialisation PHP non sécurisée.
*   **CVE-2026-8496 :** Vulnérabilité zero-day dans les plateformes de webmail SOGo et Kerio.

**Recommandations**
*   **Mises à jour logicielles :** Appliquer immédiatement les correctifs pour WinRAR, 7-Zip, Notepad++, ainsi que pour les solutions de messagerie (Zimbra, Roundcube, SOGo, etc.).
*   **Vigilance accrue :** Sensibiliser les utilisateurs aux emails de phishing et à la méfiance envers les fichiers exécutables ou scripts provenant de sources non vérifiées, même s'ils semblent inoffensifs.
*   **Sécurisation des services web :** Désactiver les fonctionnalités inutilisées des serveurs de messagerie et surveiller étroitement les accès aux interfaces webmail, en privilégiant des solutions maintenues et à jour.

---
[Source](https://thehackernews.com/2026/07/fake-notepad-plugin-delivers.html){:target="_blank"}
