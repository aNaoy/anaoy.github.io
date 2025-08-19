---
title: 'GodRAT – New RAT targeting financial institutions'
date: 2025-08-19
permalink: /posts/2025/08/19/godrat-new-rat-targeting-financial-institutions/
tags:
- veille-cyber
- securelist
---
**GodRAT : une nouvelle menace évoluant à partir d'anciennes bases de code**

Des acteurs malveillants ciblent des institutions financières, telles que des sociétés de trading et de courtage, en distribuant des fichiers .scr (économiseurs d'écran) déguisés en documents financiers via Skype. Ces fichiers contiennent un nouveau cheval de Troie d'accès à distance (RAT) nommé GodRAT, dérivé du code de Gh0st RAT. Pour contourner les détections, des techniques de stéganographie sont utilisées pour dissimuler du shellcode dans des fichiers image, qui télécharge ensuite GodRAT à partir d'un serveur de commande et de contrôle (C2).

Une fois installé, GodRAT déploie des plugins, notamment un gestionnaire de fichiers pour explorer les systèmes compromis et des voleurs de mots de passe de navigateur pour subtiliser des informations d'identification. AsyncRAT est également utilisé comme implant secondaire pour maintenir un accès prolongé. GodRAT présente des similitudes frappantes avec AwesomePuppet, un autre malware basé sur Gh0st RAT, suggérant une évolution de ce dernier et un lien potentiel avec les activités du groupe Winnti APT.

**Points clés et vulnérabilités :**

*   **Méthode de distribution :** Diffusion de fichiers .scr et .pif contenant des documents financiers frauduleux via Skype.
*   **Technique d'évasion :** Utilisation de la stéganographie pour dissimuler le shellcode dans des fichiers image.
*   **Base de code :** GodRAT est basé sur la base de code de Gh0st RAT, une ancienne famille de RAT encore activement développée et utilisée.
*   **Fonctionnalités :**
    *   Collecte d'informations sur le système (OS, nom d'hôte, processus, antivirus).
    *   Exploration du système de fichiers, suppression et déplacement de fichiers/dossiers.
    *   Vol de mots de passe de navigateurs (Chrome, Edge).
    *   Téléchargement et exécution de fichiers.
    *   Ouverture de liens URL.
    *   Injection de plugins supplémentaires.
*   **Implants secondaires :** Utilisation d'AsyncRAT pour un accès persistant.
*   **Vulnerabilité exploitée :** Bien qu'aucun CVE spécifique ne soit mentionné, la vulnérabilité réside dans la capacité des attaquants à tromper les utilisateurs pour exécuter des fichiers malveillants et à exploiter des systèmes non patchés via le RAT lui-même.
*   **Connexion à Winnti APT :** La similitude avec AwesomePuppet suggère un lien potentiel avec les opérations du groupe Winnti APT.

**Recommandations :**

*   **Sensibilisation des utilisateurs :** Éduquer les utilisateurs sur les risques liés à l'ouverture de fichiers exécutables ou d'archives provenant de sources inconnues ou suspectes, en particulier lorsqu'ils sont reçus via des messageries instantanées.
*   **Mises à jour et patchs :** Maintenir les systèmes d'exploitation et les logiciels à jour avec les derniers correctifs de sécurité pour atténuer les vulnérabilités potentielles.
*   **Solutions de sécurité :** Mettre en œuvre des solutions de sécurité robustes, notamment des antivirus avancés, des systèmes de détection et de prévention des intrusions (IDS/IPS), et des outils d'analyse comportementale pour détecter et bloquer les activités malveillantes.
*   **Filtrage du trafic réseau :** Surveiller et filtrer le trafic réseau pour identifier et bloquer les communications avec les serveurs de commande et de contrôle (C2) identifiés.
*   **Analyse des indicateurs de compromission (IoC) :** Utiliser les IoC fournis (hashes de fichiers, chemins, domaines/IP) pour identifier et éradiquer les infections existantes.

---
[Source](https://securelist.com/godrat/117119/){:target="_blank"}
