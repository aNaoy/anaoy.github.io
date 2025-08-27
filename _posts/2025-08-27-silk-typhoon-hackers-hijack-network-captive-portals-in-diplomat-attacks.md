---
title: 'Silk Typhoon hackers hijack network captive portals in diplomat attacks'
date: 2025-08-27
permalink: /posts/2025/08/27/silk-typhoon-hackers-hijack-network-captive-portals-in-diplomat-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Le Piège du Portail Captif : Cyberespionnage contre les Diplomates**

Des pirates informatiques liés à l'activité "Silk Typhoon", identifiés par Google sous le nom d'UNC6384 et associés au groupe chinois TEMP.Hex (Mustang Panda), ont ciblé des diplomates en détournant le trafic web via des portails captifs.

**Méthodologie d'Attaque :**

*   **Usurpation de Portails Captifs :** Les attaquants exploitent une technique avancée d'adversaire-en-le-milieu (AitM) pour intercepter le trafic réseau.
*   **Redirection vers un Site Malin :** Après avoir compromis un appareil réseau, ils redirigent les utilisateurs naviguant sur Chrome vers une fausse page de mise à jour de plugin Adobe.
*   **Distribution de Malware :** Les victimes sont incitées à télécharger un fichier exécutable signé numériquement, "AdobePlugins.exe". Ce dernier installe un paquet MSI contenant un outil Canon, une DLL (CANONSTAGER) et une porte dérobée nommée SOGU.SEC (une variante de PlugX), tous deux chiffrés en RC4.
*   **Exécution et Contrôle :** CANONSTAGER utilise une technique de chargement latéral de DLL pour décrypter et charger le malware SOGU.SEC en mémoire système, permettant la collecte d'informations, le transfert de fichiers et l'obtention d'un shell de commande à distance.

**Points Clés et Vulnérabilités :**

*   **Technique AitM :** Le détournement du trafic réseau en exploitant les portails captifs pour le phishing ciblé.
*   **Ingénierie Sociale :** L'utilisation de fausses mises à jour de logiciels pour inciter au téléchargement de malwares.
*   **Utilisation de Certificats Signés :** Les fichiers malveillants étaient signés par Chengdu Nuoxin Times Technology Co., Ltd, potentiellement à l'insu de l'entreprise, rendant la détection plus difficile. L'origine de la signature reste à clarifier.
*   **Malware PlugX :** L'utilisation d'une porte dérobée connue, utilisée par plusieurs groupes d'acteurs malveillants chinois, témoignant de la sophistication et de la réutilisation des outils.
*   **Absence de CVE spécifique mentionnée dans l'article, mais la technique AitM sur les portails captifs représente une vulnérabilité systémique.**

**Recommandations :**

*   **Défiance envers les Certificats :** Traiter tous les certificats émis par Chengdu Nuoxin Times Technology Co., Ltd comme non fiables jusqu'à clarification de la situation.
*   **Détection :** Utiliser les règles YARA et les indicateurs de compromission (IoCs) partagés par Google pour détecter les échantillons de malware utilisés dans ces campagnes.
*   **Alertes de Sécurité :** Les utilisateurs de Gmail et Workspace ont reçu des alertes concernant les acteurs parrainés par des gouvernements.
*   **Surveillance :** Être vigilant face à l'évolution rapide et à la sophistication croissante des acteurs d'espionnage liés à la Chine, qui changent fréquemment d'infrastructure et de builds de logiciels malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/silk-typhoon-hackers-hijack-network-captive-portals-in-diplomat-attacks/){:target="_blank"}
