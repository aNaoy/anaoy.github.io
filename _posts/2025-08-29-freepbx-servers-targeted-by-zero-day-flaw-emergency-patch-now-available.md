---
title: 'FreePBX Servers Targeted by Zero-Day Flaw, Emergency Patch Now Available'
date: 2025-08-29
permalink: /posts/2025/08/29/freepbx-servers-targeted-by-zero-day-flaw-emergency-patch-now-available/
tags:
- veille-cyber
- hackernews
---
### Alerte de Sécurité : Exploitation Active d'une Vulnérabilité Critique sur FreePBX

Des attaquants exploitent activement une faille de sécurité "zero-day" dans la plateforme de communication open-source FreePBX, particulièrement lorsque le panneau de contrôle administrateur est accessible via Internet. Cette vulnérabilité, identifiée comme **CVE-2025-57819** avec une note de sévérité maximale (CVSS 10.0), permet à des utilisateurs non authentifiés de manipuler la base de données et d'exécuter du code à distance.

L'exploitation est attribuée à un problème de traitement des données fournies par l'utilisateur dans le module commercial "endpoint". Les attaques ont débuté aux alentours du 21 août 2025.

**Versions Affectées :**

*   FreePBX 15 avant la version 15.0.66
*   FreePBX 16 avant la version 16.0.89
*   FreePBX 17 avant la version 17.0.3

**Points Clés et Exploitation :**

*   Permet l'accès administrateur sans authentification.
*   Conduit à la manipulation de la base de données et à l'exécution de code à distance.
*   Des rapports indiquent que des attaquants cherchent à obtenir un accès de niveau root après l'exploitation initiale.
*   L'exploitation active vise les systèmes exposés publiquement, potentiellement sans filtrage IP adéquat.
*   Des backdoors sont installées après compromission.

**Recommandations :**

*   **Mettre à jour FreePBX** vers les dernières versions prises en charge (>= 15.0.66 pour v15, >= 16.0.89 pour v16, >= 17.0.3 pour v17).
*   **Restreindre l'accès public** au panneau de contrôle administrateur.
*   **Scanner les environnements** à la recherche d'indicateurs de compromission (IoCs) :
    *   Modification ou suppression récente du fichier `/etc/freepbx.conf`.
    *   Présence du fichier `/var/www/html/.clean.sh`.
    *   Requêtes POST suspectes vers `modular.php` dans les logs Apache depuis le 21 août 2025.
    *   Appels vers l'extension 9998 dans les logs Asterisk.
    *   Présence d'un utilisateur "ampuser" suspect dans la table `ampusers` ou d'autres utilisateurs inconnus.
*   En cas de doute, déconnecter immédiatement les systèmes concernés.

---
[Source](https://thehackernews.com/2025/08/freepbx-servers-targeted-by-zero-day.html){:target="_blank"}
