---
title: 'Global Salt Typhoon hacking campaigns linked to Chinese tech firms'
date: 2025-08-27
permalink: /posts/2025/08/27/global-salt-typhoon-hacking-campaigns-linked-to-chinese-tech-firms/
tags:
- veille-cyber
- bleepingcomp
---
## Campagnes de Cyberespionnage Mondial Liées à des Entreprises Technologiques Chinoises

Des agences de sécurité nationale de plusieurs pays, dont les États-Unis (NSA) et le Royaume-Uni (NCSC), ont établi un lien entre les campagnes mondiales de piratage attribuées au groupe "Salt Typhoon" et trois entreprises technologiques basées en Chine : Sichuan Juxinhe Network Technology Co. Ltd., Beijing Huanyu Tianqiong Information Technology Co., et Sichuan Zhixin Ruijie Network Technology Co. Ltd. Ces entreprises auraient fourni des produits et services informatiques au Ministère de la Sécurité d'État chinois et à l'Armée Populaire de Libération, facilitant ainsi des opérations d'espionnage cybernétique.

Depuis au moins 2021, ces acteurs ont compromis des réseaux gouvernementaux, de télécommunications, de transport, d'hébergement et militaires à travers le monde, dans le but de voler des données permettant de suivre les communications et les déplacements de leurs cibles. Les télécommunications ont été particulièrement visées pour espionner les communications privées à l'échelle mondiale.

### Points Clés :

*   **Acteurs soutenus par l'État chinois :** Les campagnes "Salt Typhoon" sont attribuées à des acteurs liés au gouvernement chinois.
*   **Cibles :** Principalement les secteurs des télécommunications, du gouvernement, du transport, de l'hôtellerie et des militaires à l'échelle mondiale.
*   **Objectifs :** Vol de données pour l'espionnage, la surveillance des communications et des déplacements.
*   **Méthodes :** Exploitation de vulnérabilités connues sur des équipements réseau périphériques, plutôt que des exploits "zero-day". Utilisation d'outils personnalisés pour la surveillance et le vol de données.
*   **Impact passé :** Compromission de grands opérateurs américains (AT&T, Verizon, Lumen) pour accéder aux communications et aux systèmes de surveillance de la police. Piratage de réseaux de la Garde Nationale de l'armée américaine.

### Vulnérabilités Exploités (avec CVE) :

*   **CVE-2024-21887** : Injection de commandes dans Ivanti Connect Secure.
*   **CVE-2024-3400** : Exécution de code à distance (RCE) dans Palo Alto PAN-OS GlobalProtect.
*   **CVE-2023-20273** et **CVE-2023-20198** : Contournement de l'authentification et élévation de privilèges dans Cisco IOS XE.
*   **CVE-2018-0171** : Exécution de code à distance (RCE) dans Cisco Smart Install.

Ces vulnérabilités ont permis aux acteurs d'accéder aux équipements réseau, de modifier les listes de contrôle d'accès, d'activer le SSH sur des ports non standards, de créer des tunnels GRE/IPsec et d'utiliser des conteneurs Cisco Guest Shell pour maintenir la persistance.

### Recommandations :

*   **Prioriser la mise à jour (patching) :** Appliquer rapidement les correctifs disponibles pour les équipements réseau, en particulier les appareils périphériques.
*   **Renforcer la configuration des appareils :**
    *   Restreindre les services de gestion à des réseaux dédiés.
    *   Imposer des protocoles sécurisés comme SSHv2 et SNMPv3.
    *   Désactiver les services inutiles, tels que Cisco Smart Install et Guest Shell lorsque ce n'est pas nécessaire.
*   **Surveillance continue :** Surveiller activement les changements non autorisés et rechercher les signes de compromission, étant donné que les campagnes exploitent des faiblesses connues.
*   **Auditer les journaux :** Examiner les journaux pour détecter toute activité suspecte, comme la redirection de serveurs TACACS+.

---
[Source](https://www.bleepingcomputer.com/news/security/global-salt-typhoon-hacking-campaigns-linked-to-chinese-tech-firms/){:target="_blank"}
