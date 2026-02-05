---
title: 'Infy Hackers Resume Operations with New C2 Servers After Iran Internet Blackout Ends'
date: 2026-02-05
permalink: /posts/2026/02/05/infy-hackers-resume-operations-with-new-c2-servers-after-iran-internet-blackout-ends/
tags:
- veille-cyber
- hackernews
---
**Le groupe Infy reprend ses activités avec de nouvelles infrastructures C2 après la levée du black-out internet iranien**

Le groupe de menace iranien connu sous le nom d'Infy (ou Prince of Persia) a relancé ses opérations en utilisant de nouvelles infrastructures de commande et de contrôle (C2) peu après la fin du black-out internet imposé par le régime iranien début janvier 2026. Cette reprise d'activité, observée le 26 janvier 2026, soit la veille de l'assouplissement des restrictions, confirme le lien présumé entre le groupe et l'État iranien. Infy, actif depuis 2004, est connu pour ses attaques ciblées d'espionnage et de collecte de renseignements, visant à rester discret.

Les recherches ont révélé l'utilisation par Infy de versions mises à jour de ses outils malveillants, Foudre et Tonnerre. La dernière version de Tonnerre, nommée Tornado (version 50 puis 51), utilise désormais à la fois HTTP et Telegram pour sa communication C2. Cette évolution inclut une nouvelle méthode de génération de noms de domaine C2 via un algorithme DGA et des noms fixes basés sur des données blockchain, offrant une plus grande flexibilité.

Le groupe semble également exploiter une vulnérabilité "zero-day" (1-day) dans WinRAR (potentiellement CVE-2025-8088 ou CVE‑2025‑6218) pour déployer le payload Tornado sur les systèmes compromis. Cette technique vise à améliorer le taux de réussite des campagnes. Les archives RAR malveillantes, trouvées sur VirusTotal, suggèrent que l'Allemagne et l'Inde pourraient avoir été ciblées.

Au sein des archives RAR, un auto-extractible (SFX) contient le fichier principal Tornado v51 (AuthFWSnapin.dll) et un installateur (reg7989.dll). Cet installateur vérifie l'absence d'Avast, puis crée une tâche planifiée pour la persistance avant d'exécuter Tornado. Ce dernier communique via HTTP pour télécharger et exécuter le backdoor, collecter des informations système, ou utilise l'API Telegram pour exfiltrer des données et recevoir des commandes.

L'analyse des communications sur Telegram a permis de découvrir l'utilisation d'un bot Telegram par Tonnerre. Des messages extraits révèlent le déploiement de ZZ Stealer, un infostealer personnalisé basé sur StormKitty. Ce dernier, en réponse à la commande "8==3", télécharge et exécute un malware de second étage portant le même nom. Une corrélation a également été établie entre la chaîne d'attaque de ZZ Stealer et une campagne ciblant le répertoire PyPI avec un package nommé "testfiwldsd21233s". Une corrélation plus faible est suspectée avec le groupe Charming Kitten en raison de l'utilisation de fichiers ZIP, LNK et d'une technique de chargement PowerShell.

**Points Clés :**

*   Le groupe Infy, présumé sponsorisé par l'État iranien, a repris ses activités après une interruption liée au black-out internet en Iran.
*   Utilisation de nouvelles infrastructures de commande et de contrôle (C2), notamment via HTTP et Telegram.
*   Développement de nouveaux outils malveillants, dont Tornado, la dernière version de Tonnerre.
*   Exploitation d'une vulnérabilité "zero-day" dans WinRAR pour le déploiement de malware.
*   Découverte d'un infostealer (ZZ Stealer) et de liens potentiels avec des campagnes de malwares sur PyPI.

**Vulnérabilités :**

*   WinRAR "1-day" vulnerability (potentiellement CVE-2025-8088 ou CVE‑2025‑6218)

**Recommandations :**

*   Maintenir les logiciels, y compris WinRAR, à jour pour corriger les vulnérabilités connues.
*   Surveiller les communications via Telegram pour détecter d'éventuelles activités malveillantes.
*   Mettre en place des mécanismes de détection et de prévention des malwares, y compris les infostealers.
*   Adopter des pratiques de sécurité robustes pour minimiser le risque d'exploitation des vulnérabilités.

---
[Source](https://thehackernews.com/2026/02/infy-hackers-resume-operations-with-new.html){:target="_blank"}
