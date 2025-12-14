---
title: 'ClickFix Attacks Still Using the Finger, (Sat, Dec 13th)'
date: 2025-12-14
permalink: /posts/2025/12/14/clickfix-attacks-still-using-the-finger-sat-dec-13th/
tags:
- veille-cyber
- sans-isc
---
**Abus du Protocole Finger dans les Attaques ClickFix**

Le protocole réseau désuet "finger" est exploité dans des campagnes d'ingénierie sociale nommées ClickFix depuis fin 2025. Des acteurs malveillants comme KongTuke et SmartApeSG utilisent l'exécutable `finger.exe` sur les systèmes Windows pour récupérer du contenu malveillant.

**Points Clés:**

*   Les attaques ClickFix utilisent le protocole "finger" pour télécharger et exécuter du code malveillant.
*   Deux campagnes notables, KongTuke et SmartApeSG, ont été observées utilisant cette technique en décembre 2025.
*   Le trafic "finger" transite généralement sur le port TCP 79.
*   Les réponses du serveur "finger" contiennent des commandes PowerShell encodées en Base64 ou des scripts pour télécharger et exécuter des fichiers.

**Vulnérabilités:**

Bien qu'il ne s'agisse pas d'une vulnérabilité logicielle spécifique avec un numéro CVE identifié dans cet article, l'abus du protocole "finger" repose sur le fait que ce protocole, bien que largement obsolète, peut encore être activé ou non bloqué sur certains systèmes et réseaux. Son utilisation pour transmettre des commandes et du code malveillant exploite cette accessibilité.

**Recommandations:**

*   Bloquer le trafic TCP sur le port 79 au niveau des pare-feux et des proxys, en particulier dans les environnements d'entreprise.
*   Surveiller le trafic réseau pour détecter les communications utilisant le protocole "finger".
*   Sensibiliser les utilisateurs aux techniques d'ingénierie sociale, notamment celles qui peuvent se présenter sous forme de fausses pages de vérification (CAPTCHA).

---
[Source](https://isc.sans.edu/diary/rss/32566){:target="_blank"}
