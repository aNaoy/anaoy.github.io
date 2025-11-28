---
title: 'Tomiris wreaks Havoc: New tools and techniques of the APT group'
date: 2025-11-28
permalink: /posts/2025/11/28/tomiris-wreaks-havoc-new-tools-and-techniques-of-the-apt-group/
tags:
- veille-cyber
- securelist
---
Voici un résumé de l'article :

**Évolution des Tactiques du Groupe APT Tomiris**

Le groupe APT Tomiris a étendu ses opérations depuis début 2025, ciblant des ministères étrangers, des organisations intergouvernementales et des entités gouvernementales. Une évolution notable de leurs tactiques réside dans l'utilisation accrue d'implants qui exploitent des services publics tels que Telegram et Discord pour leurs communications de commande et contrôle (C2). Cette approche vise à dissimuler le trafic malveillant parmi le trafic légitime pour échapper aux détections.

Les infections débutent généralement par des e-mails de phishing contenant des archives malveillantes, souvent protégées par mot de passe. Ces archives contiennent des exécutables conçus pour tromper l'utilisateur, parfois en imitant des icônes de documents ou en utilisant des extensions doubles.

Une fois le système compromis, Tomiris déploie des outils de type "reverse shell" développés dans divers langages de programmation (Go, Rust, C/C++/C#, Python). Ces implants initiaux servent à la reconnaissance du système et au téléchargement d'autres malwares. Dans plusieurs cas, les attaquants ont utilisé les frameworks open-source Havoc ou AdaptixC2 pour les phases post-exploitation.

Parmi les implants découverts figurent :
*   Des "reverse shells" en C/C++ qui téléchargent AdaptixC2.
*   Un "downloader" en Rust qui collecte des informations système et des chemins de fichiers, les envoyant via Discord.
*   Un "reverse shell" en Python utilisant Discord comme canal C2, capable de télécharger AdaptixC2 et un "filegrabber".
*   Un "filegrabber" en Python qui archive et exfiltre des fichiers vers le C2.
*   La backdoor "Distopia", basée sur un projet open-source, capable d'exécuter des commandes et de télécharger d'autres malwares.
*   Un "reverse shell" en Python utilisant Telegram comme canal C2.
*   D'autres implants variés en C#, Rust, Go, et PowerShell, certains utilisant Telegram pour la communication C2.
*   Des implants de type "reverse SOCKS proxy", probablement utilisés pour faciliter le mouvement latéral.

Les attaques ont ciblé des entités principalement russophones, ainsi que des utilisateurs au Turkménistan, au Kirghizistan, au Tadjikistan et en Ouzbékistan. Le groupe utilise des noms de fichiers spécifiques et des formats de mots de passe pour leurs archives, des caractéristiques observées précédemment avec l'outil JLORAT.

**Points Clés :**

*   Utilisation accrue de Telegram et Discord comme canaux C2.
*   Développement et déploiement d'implants variés en plusieurs langages de programmation.
*   Exploitation des frameworks open-source Havoc et AdaptixC2 pour la post-exploitation.
*   Techniques d'évasion incluant le déguisement des exécutables et l'utilisation de services publics pour le C2.
*   Ciblage de ministères, d'organisations intergouvernementales et d'entités gouvernementales, avec une attention particulière pour la région russophone.

**Vulnérabilités :**

Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article comme étant directement exploitée. Les attaques reposent sur des techniques d'ingénierie sociale (phishing), des malwares polymorphes et des méthodes de communication dissimulées.

**Recommandations :**

Bien que l'article ne formule pas de recommandations directes, les observations impliquent la nécessité de :
*   Mettre en place des solutions de sécurité capables de détecter les malwares et le trafic C2, y compris celui utilisant des services publics.
*   Renforcer la formation des utilisateurs sur la détection des e-mails de phishing.
*   Surveiller activement le trafic réseau pour identifier les communications suspectes avec des plateformes comme Telegram et Discord à des fins malveillantes.
*   Utiliser des stratégies de détection avancées basées sur l'analyse comportementale.

---
[Source](https://securelist.com/tomiris-new-tools/118143/){:target="_blank"}
