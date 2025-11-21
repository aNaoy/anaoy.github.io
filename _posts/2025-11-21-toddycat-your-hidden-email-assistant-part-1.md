---
title: 'ToddyCat: your hidden email assistant. Part 1'
date: 2025-11-21
permalink: /posts/2025/11/21/toddycat-your-hidden-email-assistant-part-1/
tags:
- veille-cyber
- securelist
---
**ToddyCat : Stratégies d'Accès aux Communications d'Entreprise**

Le groupe ToddyCat APT adapte ses méthodes pour accéder furtivement aux correspondances par email des organisations. Les attaques récentes, observées fin 2024 et début 2025, révèlent une évolution des tactiques visant à contourner les mesures de sécurité.

**Points Clés :**

*   **Évolution de TomBerBil :** Une nouvelle variante de TomBerBil, écrite en PowerShell, est désormais utilisée. Elle cible les contrôleurs de domaine pour extraire les cookies, l'historique de navigation et les mots de passe enregistrés des navigateurs Chrome, Edge et Firefox via le protocole SMB. Cette version exploite les fichiers de clés de chiffrement DPAPI présents sur les systèmes ciblés pour déchiffrer localement les données volées.
*   **Extraction des Fichiers OST d'Outlook :** Pour accéder aux emails, ToddyCat utilise un outil nommé TCSectorCopy. Ce dernier effectue une copie bloc par bloc des fichiers OST (Offline Storage Table) d'Outlook, même lorsqu'ils sont verrouillés par l'application. Les données extraites sont ensuite traitées par XstReader pour exporter le contenu des emails et des pièces jointes.
*   **Vol de Jetons d'Accès OAuth 2.0 :** Face aux limitations des méthodes basées sur la collecte de fichiers, le groupe cible les jetons d'accès OAuth 2.0 dans la mémoire des processus liés à Microsoft 365. L'outil SharpTokenFinder, ou à défaut ProcDump, est utilisé pour extraire ces jetons, permettant ainsi un accès aux emails en dehors de l'infrastructure compromise.

**Vulnérabilités :**

Bien que l'article ne mentionne pas de CVE spécifiques, les vulnérabilités exploitées découlent de l'accès à des informations sensibles stockées localement (mots de passe, clés de chiffrement) et de l'utilisation de méthodes d'accès à bas niveau pour contourner les protections des fichiers (TCSectorCopy). Le vol de jetons d'accès OAuth 2.0 exploite la manière dont ces jetons sont gérés en mémoire par les applications Microsoft 365.

**Recommandations :**

*   **Surveillance des Accès aux Fichiers :** Mettre en place une journalisation des accès aux dossiers de navigateurs et aux fichiers `.ost` d'Outlook. Surveiller spécifiquement les connexions SMB aux dossiers de profils utilisateurs et les accès directs aux disques (Event ID 9 Sysmon) pour détecter l'utilisation de TCSectorCopy.
*   **Surveillance des Processus et Lignes de Commande :** Surveiller l'exécution de ProcDump avec des arguments ciblant les processus Microsoft 365 (comme `OUTLOOK.exe`) pour détecter les tentatives de vol de jetons d'accès.
*   **Solutions de Sécurité :** Utiliser des solutions EPP (Endpoint Protection Platform) comme Kaspersky Endpoint Security for Business et des systèmes de surveillance avancée des menaces comme Kaspersky Anti Targeted Attack.
*   **Intelligence sur les Menaces :** S'appuyer sur des services d'intelligence sur les menaces pour obtenir des informations actualisées sur les indicateurs de compromission et les règles de détection.

---
[Source](https://securelist.com/toddycat-apt-steals-email-data-from-outlook/118044/){:target="_blank"}
