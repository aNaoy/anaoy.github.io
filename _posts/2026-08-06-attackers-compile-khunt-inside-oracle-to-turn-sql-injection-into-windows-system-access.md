---
title: 'Attackers Compile khunt Inside Oracle to Turn SQL Injection Into Windows SYSTEM Access'
date: 2026-08-06
permalink: /posts/2026/08/06/attackers-compile-khunt-inside-oracle-to-turn-sql-injection-into-windows-system-access/
tags:
- veille-cyber
- hackernews
---
### Compromission Oracle via Injection SQL et exécution "fileless"

**Points clés**
*   **Méthode d'attaque :** Des attaquants utilisent une injection SQL sur une application web pour injecter du code Java directement dans une base de données Oracle.
*   **Technique "Fileless" :** Le code est compilé par la JVM intégrée d'Oracle en objets de schéma stockés. Aucun exécutable n'est écrit sur le disque, ce qui permet de contourner les outils de détection classiques (EDR/Antivirus).
*   **Escalade de privilèges :** Le toolkit nommé **khunt** permet l'exécution de commandes système avec les privilèges **SYSTEM** sur le serveur Windows hébergeant la base de données.
*   **Toolkit khunt :** Composé de plusieurs objets Java (`KhuntCmd`, `KhuntHash`, `KhuntFS`, etc.), il permet d'exécuter des commandes OS, de voler des hashs de mots de passe, d'explorer le système de fichiers et d'extraire les ruches du registre Windows.

**Vulnérabilités**
*   **Injection SQL :** Le point d'entrée initial via un champ de recherche non validé.
*   **Sur-privilèges :** Le compte de service utilisé par l'application possédait des droits excessifs, incluant la création d'objets Java et l'exécution de procédures système (non associée à une CVE spécifique, il s'agit d'une faille de configuration et de design).

**Recommandations**
*   **Sécurisation applicative :** Implémenter des requêtes paramétrées et une validation stricte des entrées utilisateur pour neutraliser les injections SQL.
*   **Principe du moindre privilège :** Restreindre drastiquement les droits du compte utilisateur de la base de données. Celui-ci ne doit pas avoir la capacité de créer des sources Java (`CREATE JAVA SOURCE`) ou d'exécuter des procédures stockées inutiles.
*   **Détection :** Rechercher dans les logs SQL les commandes commençant par `KHUNT%` et inspecter les objets de schéma nommés `Khunt` au sein de l'installation Oracle.
*   **Audit de configuration :** Surveiller l'utilisation de `Runtime.exec` et des permissions d'exécution de fichiers au sein de la JVM intégrée.

---
[Source](https://thehackernews.com/2026/08/attackers-compile-khunt-inside-oracle.html){:target="_blank"}
