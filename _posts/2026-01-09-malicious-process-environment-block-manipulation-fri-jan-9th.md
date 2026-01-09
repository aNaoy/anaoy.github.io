---
title: 'Malicious Process Environment Block Manipulation, (Fri, Jan 9th)'
date: 2026-01-09
permalink: /posts/2026/01/09/malicious-process-environment-block-manipulation-fri-jan-9th/
tags:
- veille-cyber
- sans-isc
---
**Manipulation de la ligne de commande des processus**

Cette technique permet à des logiciels malveillants de masquer leurs intentions en modifiant les informations relatives aux processus qu'ils créent. En exploitant le "Process Environment Block" (PEB), une structure de données accessible en mode utilisateur, un processus peut modifier sa propre ligne de commande ou celle d'un autre processus.

**Points clés :**

*   La création de processus sous Windows utilise l'appel API `CreateProcess()`.
*   L'option `CREATE_SUSPENDED` permet de créer un processus sans le lancer immédiatement, une pratique souvent associée à des activités malveillantes (comme le "process hollowing").
*   Le PEB contient des informations essentielles sur un processus, y compris ses paramètres d'exécution.
*   Les processus peuvent lire et modifier leur propre PEB.

**Vulnérabilités :**

Bien qu'aucune CVE spécifique ne soit mentionnée dans l'article, la technique elle-même exploite une fonctionnalité du système d'exploitation (l'accès au PEB) plutôt qu'une faille de sécurité traditionnelle. Elle peut être considérée comme une vulnérabilité de "design" ou une "caractéristique" qui peut être détournée à des fins malveillantes.

**Recommandations :**

*   **Surveillance des processus :** Les outils de sécurité, tels que les solutions EDR (Endpoint Detection and Response), doivent être capables de détecter les modifications des PEB et de corréler les informations originales au moment de la création du processus.
*   **Attention à `CREATE_SUSPENDED` :** L'utilisation de ce drapeau lors de la création de processus doit être examinée avec suspicion.
*   **Limitation :** Modifier la ligne de commande d'un processus existant est risqué si la nouvelle ligne de commande est plus longue que l'originale, ce qui pourrait entraîner un dépassement de tampon. Les journaux d'origine au moment de la création du processus ne sont pas affectés.

---
[Source](https://isc.sans.edu/diary/rss/32614){:target="_blank"}
