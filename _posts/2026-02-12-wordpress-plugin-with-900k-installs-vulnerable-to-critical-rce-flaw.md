---
title: 'WordPress plugin with 900k installs vulnerable to critical RCE flaw'
date: 2026-02-12
permalink: /posts/2026/02/12/wordpress-plugin-with-900k-installs-vulnerable-to-critical-rce-flaw/
tags:
- veille-cyber
- bleepingcomp
---
**Faille Critique dans WPvivid Backup & Migration : Risque d'Exécution de Code à Distance**

Un défaut de sécurité critique a été découvert dans le plugin WordPress WPvivid Backup & Migration, utilisé par plus de 900 000 sites. Il permet une exécution de code à distance (RCE) via l'upload de fichiers non authentifiés.

**Points Clés :**

*   **Impact Potentiel :** Prise de contrôle totale du site web.
*   **Condition d'Exploitation :** La vulnérabilité est critique uniquement pour les sites ayant activé l'option "recevoir des sauvegardes d'un autre site".
*   **Fenêtre d'Exploitation :** Limitée à 24 heures, correspondant à la durée de validité d'une clé générée pour les transferts de sauvegarde.
*   **Cause Racine :** Gestion incorrecte des erreurs lors du déchiffrement RSA et absence de nettoyage des chemins d'accès des fichiers.

**Vulnérabilités :**

*   **CVE-2026-1357** : Gravité de 9.8/10. Permet l'exécution de code à distance par l'upload de fichiers arbitraires sans authentification. L'échec du déchiffrement RSA mène à une clé prédictible, et le manque de sanitization des noms de fichiers permet le "directory traversal" pour écrire des fichiers PHP malveillants en dehors du répertoire de sauvegarde prévu.

**Recommandations :**

*   **Mise à jour Immédiate :** Les utilisateurs du plugin WPvivid Backup & Migration doivent impérativement passer à la version **0.9.124** ou supérieure.
*   **Corrections Apportées :** La version corrigée inclut une vérification pour arrêter l'exécution en cas d'échec du déchiffrement RSA, un nettoyage des noms de fichiers, et une restriction des types de fichiers autorisés pour les uploads (ZIP, GZ, TAR, SQL).

---
[Source](https://www.bleepingcomputer.com/news/security/wordpress-plugin-with-900k-installs-vulnerable-to-critical-rce-flaw/){:target="_blank"}
