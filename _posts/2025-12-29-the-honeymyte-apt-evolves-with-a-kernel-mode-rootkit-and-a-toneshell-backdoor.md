---
title: 'The HoneyMyte APT evolves with a kernel-mode rootkit and a ToneShell backdoor'
date: 2025-12-29
permalink: /posts/2025/12/29/the-honeymyte-apt-evolves-with-a-kernel-mode-rootkit-and-a-toneshell-backdoor/
tags:
- veille-cyber
- securelist
---
## Évolution de HoneyMyte : un rootkit noyau et une porte dérobée ToneShell

Une nouvelle menace, attribuée au groupe APT HoneyMyte, a été détectée utilisant un pilote malveillant signé avec un certificat numérique compromis. Ce pilote, s'enregistrant comme un mini-filtre, injecte une porte dérobée ToneShell dans les processus système. Le groupe est connu pour ses campagnes de cyberespionnage ciblant particulièrement les organisations gouvernementales d'Asie du Sud-Est et d'Asie de l'Est, avec des victimes récurrentes et une utilisation antérieure d'autres outils de HoneyMyte tels que ToneDisk et PlugX.

**Points Clés :**

*   **Nouveau Vecteur d'Attaque :** Utilisation d'un pilote noyau malveillant pour injecter la porte dérobée ToneShell.
*   **Certificat Compromis :** Le pilote est signé avec un ancien certificat numérique de Guangzhou Kingteller Technology Co., Ltd. (valide d'août 2012 à 2015).
*   **Fonctionnalités du Pilote :** Le pilote agit comme un rootkit, protégeant ses propres fichiers, les processus infectés et les clés de registre contre la détection et la suppression. Il utilise des techniques d'obfuscation comme la résolution dynamique d'API par hachage.
*   **Protection Renforcée :** Le pilote utilise des rappels (callbacks) pour intercepter et bloquer les opérations de suppression/renommage de fichiers et les modifications de clés de registre critiques. Il manipule également l'altitude des filtres pour contourner les protections antivirus.
*   **Injection de Charge Utile :** Le pilote injecte d'abord un shellcode pour créer un processus `svchost`, puis y injecte la porte dérobée ToneShell.
*   **Évolution de ToneShell :** La nouvelle variante de ToneShell utilise une méthode de génération d'identifiant d'hôte basée sur un fichier spécifique ou des valeurs système. Elle communique via TCP sur le port 443 avec de faux en-têtes TLS 1.3.
*   **Objectifs :** Cyberespionnage ciblant des organisations gouvernementales, notamment au Myanmar et en Thaïlande.

**Vulnérabilités :**

*   L'article ne mentionne pas de CVE spécifiques associées à ces nouvelles variantes. Les vulnérabilités exploitées pourraient inclure des failles dans la gestion des pilotes, des certificats numériques compromis, et potentiellement des vulnérabilités dans les systèmes d'exploitation ou les applications ciblées pour l'accès initial. La protection du pilote lui-même, via des méthodes de bas niveau noyau, est la principale menace.

**Recommandations :**

*   Mettre en œuvre des mesures de sécurité réseau robustes (pare-feu, systèmes de détection d'intrusion).
*   Utiliser des outils de détection et de réponse avancés (EDR).
*   Sensibiliser régulièrement les employés aux menaces de sécurité.
*   Effectuer des audits de sécurité et des évaluations de vulnérabilités régulières.
*   Considérer la mise en place d'un système SIEM pour la surveillance et l'analyse des données de sécurité.
*   La cybersécurité de la mémoire (memory forensics) est cruciale pour détecter les shellcodes injectés.

---
[Source](https://securelist.com/honeymyte-kernel-mode-rootkit/118590/){:target="_blank"}
