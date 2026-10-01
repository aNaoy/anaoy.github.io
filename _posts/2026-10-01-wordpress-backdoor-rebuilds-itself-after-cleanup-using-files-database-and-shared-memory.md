---
title: 'WordPress Backdoor Rebuilds Itself After Cleanup Using Files, Database, and Shared Memory'
date: 2026-10-01
permalink: /posts/2026/10/01/wordpress-backdoor-rebuilds-itself-after-cleanup-using-files-database-and-shared-memory/
tags:
- veille-cyber
- hackernews
---
### Analyse de la menace SC : Un "maillage auto-guérisseur" pour WordPress

Des chercheurs en cybersécurité ont identifié une nouvelle porte dérobée baptisée **SC**, caractérisée par une persistance sophistiquée fonctionnant comme un système interconnecté plutôt que comme un simple fichier malveillant.

#### Points clés
*   **Système d'auto-réplication :** Le malware se propage à travers huit emplacements distincts (fichiers, base de données, mémoire partagée System V). Chaque composant est capable de reconstruire l'ensemble du système s'il est supprimé.
*   **Infrastructure blockchain :** Le logiciel malveillant utilise la blockchain Ethereum pour communiquer avec son serveur de commande et de contrôle (C2), rendant la détection et le blocage du trafic C2 particulièrement complexes.
*   **Persistance multi-niveaux :** L'usage de la mémoire partagée (RAM) permet au payload de survivre au nettoyage des fichiers et de la base de données. Il utilise également des tâches planifiées (cron) pour assurer sa réinstallation régulière.
*   **Fonctionnalités :** Vol de données, injection de scripts malveillants (skimmers), création de comptes administrateurs cachés et désactivation de plugins de sécurité.

#### Vulnérabilité associée
En parallèle, une faille critique de type injection SQL non authentifiée a été signalée et exploitée activement :
*   **CVE-2026-1581 :** Vulnérabilité dans le plugin *wpForo Forum* (jusqu'à la version 2.4.14), score CVSS 7.5.

#### Recommandations
*   **Audits de persistance :** Lors d'une compromission WordPress, ne pas se limiter à la suppression des fichiers suspects. Vérifier systématiquement la base de données, les dossiers `mu-plugins`, les fichiers `wp-config.php`, les thèmes, ainsi que les segments de mémoire partagée.
*   **Mise à jour immédiate :** Mettre à jour le plugin *wpForo Forum* vers une version corrigée pour contrer l'exploitation active de la CVE-2026-1581.
*   **Hygiène de sécurité :** Appliquer le principe du moindre privilège, utiliser des mots de passe robustes et auditer régulièrement les comptes administrateurs.
*   **Surveillance :** Utiliser des outils de monitoring capables d'identifier des changements inattendus dans les fichiers système et les hooks WordPress (notamment `plugins_loaded` et `auto_prepend_file`).

---
[Source](https://thehackernews.com/2026/10/wordpress-backdoor-rebuilds-itself.html){:target="_blank"}
