---
title: 'Inside Ink Dragon: Revealing the Relay Network and Inner Workings of a Stealthy Offensive Operation'
date: 2025-12-16
permalink: /posts/2025/12/16/inside-ink-dragon-revealing-the-relay-network-and-inner-workings-of-a-stealthy-offensive-operation/
tags:
- veille-cyber
- zerodaysfans
---
**Ink Dragon : Un Réseau d'Attaque Sophistiqué Repositionne les Victimes en Acteurs C2**

Une nouvelle vague d'attaques, attribuée au groupe de menace chinois Ink Dragon (également connu sous les noms d'Earth Alux, Jewelbug, REF7707, CL-STA-0049), cible de manière croissante les infrastructures gouvernementales, notamment en Europe, en plus de ses activités traditionnelles en Asie du Sud-Est et en Amérique du Sud. L'originalité de cette opération réside dans sa capacité à transformer les serveurs compromis en nœuds actifs d'un réseau relais distribué. En utilisant un module personnalisé baptisé "ShadowPad IIS Listener", Ink Dragon fait de ses victimes des relais pour le trafic et les commandes, intégrant ainsi les systèmes compromis à son infrastructure de commandement et contrôle (C2).

Les méthodes d'accès initiales exploitent des vulnérabilités connues dans les configurations des serveurs IIS et SharePoint, notamment la désérialisation de ViewState via des clés de machine ASP.NET divulguées publiquement. Dans certains cas, la vulnérabilité ToolShell de Microsoft SharePoint (CVE-2025-49706, CVE-2025-53771, CVE-2025-49704, CVE-2025-53770 et autres) est également exploitée.

Une fois l'accès initial obtenu, Ink Dragon procède à des opérations internes incluant :

*   **Mouvement latéral :** Exploitation des identifiants récupérés des processus de travail IIS et utilisation du protocole RDP pour se déplacer au sein du réseau. Des outils natifs comme SMB sont également utilisés pour déployer des implants.
*   **Persistance :** Création de tâches planifiées sous des noms trompeurs (ex: `SYSCHECK`) et installation de services dissimulés (ex: `WindowsTempUpdate`) pour assurer l'exécution des charges utiles.
*   **Élévation de privilèges :** Utilisation d'outils comme `PrintNotifyPotato` pour obtenir des privilèges système, puis exfiltration de données sensibles via des outils comme `LalsDumper` pour réaliser des dumps de LSASS et des ruches de registre. L'exploitation de sessions RDP inactives appartenant à des administrateurs de domaine est également une technique privilégiée.
*   **Contournement des contrôles de sortie :** Modification des règles de pare-feu hôtes pour permettre un trafic sortant non restreint, déguisé sous des noms de processus légitimes (ex: `Microsoft MsMpEng`).

Le cœur de l'opération est le module **ShadowPad IIS Listener**. Ce composant s'intègre au processus IIS, intercepte le trafic HTTP correspondant à des motifs d'URL spécifiques, déchiffre les commandes et, surtout, peut enregistrer des nœuds comme "serveurs" ou "clients" pour construire un réseau relais. Ce mécanisme permet à Ink Dragon de relayer le trafic entre différentes victimes, rendant l'origine des commandes très difficile à tracer. Le module fonctionne également comme un backdoor ShadowPad complet, offrant des fonctionnalités de reconnaissance, de gestion de fichiers, de contrôle de processus et de tunneling.

D'autres outils post-exploitation observés incluent :

*   **ShadowPad Loader :** Triade de chargement (exécutable, DLL, payload chiffré) utilisé pour exécuter le cœur de ShadowPad en mémoire.
*   **CDBLoader :** Utilise le débogueur Microsoft (`cdb.exe`) pour exécuter du shellcode en mémoire, qui déchiffre et charge ensuite le payload réel.
*   **LalsDumper :** Outil interne pour l'extraction de dumps LSASS en s'enregistrant comme fournisseur de support de sécurité (SSP) et en utilisant des appels système directs pour éviter la détection.
*   **032Loader :** Chargeur qui utilise l'entropie spécifique de l'hôte (date d'installation du système) pour déchiffrer et exécuter des payloads en mémoire.
*   **FinalDraft :** Un RAT modulaire mis à jour, utilisant l'API Microsoft Graph pour masquer le trafic C2 dans les flux de messagerie Outlook. Il dispose de fonctionnalités étendues pour la collecte d'informations (historique RDP), l'affaiblissement des contrôles de sécurité (désactivation de fonctionnalités comme Restricted Admin, Token Filtering, PPL) et l'exfiltration de données à haut débit.

**Points Clés et Vulnérabilités :**

*   **Réseau Relais Victim-Based :** Ink Dragon transforme les serveurs compromis en nœuds d'un réseau de relais ShadowPad distribué.
*   **Exploitation de Configurations IIS/SharePoint :**
    *   Désérialisation de ViewState via des clés de machine ASP.NET publiques.
    *   Vulnérabilité ToolShell sur SharePoint (CVE-2025-49706, CVE-2025-53771, CVE-2025-49704, CVE-2025-53770, et autres).
*   **Nouveaux Outils et TTPs :**
    *   Variante améliorée de FinalDraft avec une meilleure furtivité et un débit d'exfiltration accru.
    *   Utilisation avancée de techniques d'évasion et de mouvement latéral.
*   **Utilisation du ShadowPad IIS Listener :** Composant clé permettant l'interception de trafic HTTP, la construction du réseau relais, et offrant des fonctionnalités backdoor complètes.

**Recommandations :**

*   **Surveillance des Connexions IIS :** Surveiller de manière proactive les configurations des serveurs IIS et SharePoint, notamment les clés de machine ASP.NET et les vulnérabilités connues.
*   **Segmentation Réseau :** Limiter la portée latérale des attaques en segmentant le réseau.
*   **Gestion des Identifiants :** Implémenter des politiques strictes de gestion des identifiants et privilèges, y compris l'utilisation de l'authentification multifacteur.
*   **Surveillance du Trafic Sortant :** Analyser le trafic sortant pour détecter des anomalies, y compris le trafic déguisé dans des canaux légitimes.
*   **Mises à Jour et Patchs :** Maintenir les systèmes à jour et appliquer les correctifs de sécurité rapidement, en particulier pour les serveurs exposés sur Internet.
*   **Détection et Réponse :** Renforcer les capacités de détection et de réponse aux incidents pour identifier et neutraliser rapidement les implants et les activités malveillantes.
*   **Analyse des Tâches Planifiées et Services :** Surveiller la création de tâches planifiées et de services suspects, surtout ceux utilisant des noms génériques ou déguisés.
*   **Surveillance de l'Activité LSASS :** Mettre en place des mesures pour détecter les tentatives de dump LSASS.
*   **Évaluation des Configurations C2 :** Porter une attention particulière aux communications utilisant des API cloud légitimes comme Microsoft Graph.

---
[Source](https://research.checkpoint.com/2025/ink-dragons-relay-network-and-offensive-operation/){:target="_blank"}
