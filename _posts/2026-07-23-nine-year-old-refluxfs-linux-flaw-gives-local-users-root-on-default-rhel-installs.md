---
title: 'Nine-Year-Old RefluXFS Linux Flaw Gives Local Users Root on Default RHEL Installs'
date: 2026-07-23
permalink: /posts/2026/07/23/nine-year-old-refluxfs-linux-flaw-gives-local-users-root-on-default-rhel-installs/
tags:
- veille-cyber
- hackernews
---
### RefluXFS : Vulnérabilité critique d'escalade de privilèges sous Linux

La faille **RefluXFS** permet à un utilisateur local non privilégié d'écraser des fichiers appartenant au compte "root" sur un système de fichiers XFS, entraînant une escalade de privilèges persistante. Cette vulnérabilité, découverte avec l'aide d'une IA, exploite une condition de concurrence (race condition) dans la gestion des verrous du noyau Linux lors des opérations de copie sur écriture (reflink).

**Points clés :**
*   **Origine :** La vulnérabilité est présente dans le noyau Linux depuis la version 4.11 (2017).
*   **Mécanisme :** Une erreur de type « check-then-use » lors du verrouillage permet d'effectuer une écriture directe (`O_DIRECT`) sur des blocs censés être protégés, en contournant les mécanismes de sécurité classiques (SELinux, seccomp).
*   **Impact :** L'attaquant peut modifier des fichiers système sensibles (comme `/etc/passwd`) ou des binaires `setuid-root` pour obtenir un accès root total et persistant.
*   **Contexte :** Les distributions utilisant par défaut XFS avec l'option `reflink=1` (RHEL, Fedora Server, Amazon Linux) sont principalement exposées.

**Vulnérabilité :**
*   **CVE-2026-64600**

**Conditions d'exploitation :**
1.  Utilisation d'un noyau Linux 4.11 ou supérieur non corrigé.
2.  Système de fichiers XFS configuré avec `reflink=1`.
3.  Présence de fichiers cibles et d'un répertoire accessible en écriture par l'attaquant sur le même volume XFS.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs de noyau fournis par votre distribution Linux (les correctifs sont disponibles depuis la mi-juillet 2026).
*   **Redémarrage obligatoire :** L'application du correctif nécessite un redémarrage du système pour charger le nouveau noyau en mémoire.
*   **Vérification :** Identifier les volumes exposés en exécutant la commande : `xfs_info / | grep reflink=`.
*   **Priorisation :** Sécuriser en priorité les environnements multi-locataires (serveurs mutualisés, environnements CI/CD) où des utilisateurs non fiables peuvent exécuter du code local.

---
[Source](https://thehackernews.com/2026/07/nine-year-old-refluxfs-linux-flaw-gives.html){:target="_blank"}
