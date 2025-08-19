---
title: 'New GodRAT Trojan Targets Trading Firms Using Steganography and Gh0st RAT Code'
date: 2025-08-19
permalink: /posts/2025/08/19/new-godrat-trojan-targets-trading-firms-using-steganography-and-gh0st-rat-code/
tags:
- veille-cyber
- hackernews
---
**GodRAT : La Menace Persistante ciblant les Sociétés de Trading**

Une nouvelle campagne de cybersécurité a émergé, ciblant spécifiquement les sociétés de trading et de courtage avec un cheval de Troie d'accès à distance inconnu jusqu'à présent, nommé GodRAT. Les attaques, actives jusqu'en août 2025, utilisent des fichiers de protection d'écran (.SCR) déguisés en documents financiers, distribués via Skype.

**Points Clés :**

*   **Distribution:** Fichiers .SCR malveillants envoyés via Skype, déguisés en documents financiers.
*   **Technique d'Obscurcissement:** Utilisation de la stéganographie pour cacher le shellcode dans des fichiers image (.JPG) afin de télécharger le malware depuis un serveur de commande et de contrôle (C2).
*   **Origine:** GodRAT est basé sur le code de Gh0st RAT, une ancienne base de code (datant de 2008) qui a été réutilisée par divers groupes de pirates informatiques, notamment chinois. Il est considéré comme une évolution d'un autre backdoor basé sur Gh0st RAT, AwesomePuppet, potentiellement lié au groupe Winnti (APT41).
*   **Fonctionnalités:** Le trojan communique via TCP, collecte des informations système et la liste des logiciels antivirus installés. Il peut ensuite exécuter des commandes reçues du serveur C2, telles que l'injection de plugins, la terminaison de processus, le téléchargement de fichiers ou l'ouverture d'URL.
*   **Plugins:** Un plugin FileManager permet la manipulation de fichiers et le téléchargement de charges utiles secondaires, y compris un voleur de mots de passe pour les navigateurs Chrome et Edge, ainsi que le trojan AsyncRAT.
*   **Outil de Création:** Le code source complet du client et du constructeur de GodRAT a été trouvé sur VirusTotal en juillet 2024. Le constructeur permet de créer des exécutables ou des DLLs, et d'injecter le code malveillant dans des binaires légitimes comme `svchost.exe`, `cmd.exe`, `cscript.exe`, `curl.exe`, `wscript.exe`, `QQMusic.exe` et `QQScLauncher.exe`. Les charges utiles finales peuvent être enregistrées avec des extensions comme .exe, .com, .bat, .scr et .pif.
*   **Durabilité du Code Ancien:** L'article souligne que les anciennes bases de code de malware, comme Gh0st RAT, continuent d'être adaptées et utilisées, démontrant leur longévité dans le paysage de la cybersécurité.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec des identifiants CVE n'est mentionnée dans l'article pour GodRAT lui-même. Cependant, la méthode d'injection de code dans des binaires légitimes (living off the land) peut être considérée comme une technique exploitant la confiance accordée à ces processus système.

**Recommandations :**

Bien que l'article se concentre sur la description de la menace, les actions suivantes peuvent être déduites pour s'en prémunir :

*   **Vigilance accrue sur Skype:** Faire preuve d'une extrême prudence avec les fichiers reçus via Skype, même de la part de contacts connus, en particulier s'ils sont déguisés en documents financiers ou s'ils proviennent d'expéditeurs inattendus.
*   **Analyse des Fichiers de Protection d'Écran:** Traiter les fichiers .SCR avec suspicion et éviter de les exécuter sans une analyse préalable par des outils de sécurité à jour.
*   **Utilisation de Solutions de Sécurité Robustes:** Maintenir à jour un logiciel antivirus et anti-malware performant, capable de détecter les techniques d'obscurcissement et les comportements suspects.
*   **Mises à Jour Régulières:** S'assurer que tous les systèmes d'exploitation et applications, y compris les navigateurs web, sont régulièrement mis à jour pour corriger les failles potentielles.
*   **Formation des Utilisateurs:** Sensibiliser les employés aux menaces de phishing et aux techniques d'ingénierie sociale utilisées par les acteurs malveillants.
*   **Surveillance du Réseau:** Mettre en place des mécanismes de surveillance pour détecter les communications suspectes avec des serveurs de commande et de contrôle.

---
[Source](https://thehackernews.com/2025/08/new-godrat-trojan-targets-trading-firms.html){:target="_blank"}
