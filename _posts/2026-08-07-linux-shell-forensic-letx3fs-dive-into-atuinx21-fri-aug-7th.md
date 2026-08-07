---
title: 'Linux Shell Forensic: Let&#x3f;s Dive Into Atuin&#x21;, (Fri, Aug 7th)'
date: 2026-08-07
permalink: /posts/2026/08/07/linux-shell-forensic-letx3fs-dive-into-atuinx21-fri-aug-7th/
tags:
- veille-cyber
- sans-isc
---
### Analyse forensique des historiques shell via Atuin

Les historiques de commandes shell classiques (ex: `.bash_history`) sont limités par leur volatilité, l'absence de précision temporelle et leur vulnérabilité à la manipulation. L'outil **Atuin** remplace ces fichiers par une base de données SQLite enrichie, offrant une source de preuves plus complète pour les enquêteurs.

#### Points clés
*   **Enrichissement des données :** Atuin enregistre le répertoire de travail, la durée d'exécution, le code de sortie (exit code), le nom d'hôte et l'identifiant de session pour chaque commande.
*   **Synchronisation :** L'outil permet une synchronisation chiffrée de bout en bout de l'historique entre plusieurs machines.
*   **Design "Soft-delete" :** Les commandes supprimées ne sont souvent que marquées comme telles (`deleted_at`), permettant potentiellement leur récupération.
*   **Persistance :** L'activité est stockée dans un fichier SQLite (`history.db`) accompagné de fichiers journaux (`-wal` et `-shm`) cruciaux pour l'investigation.

#### Vulnérabilités et limites
*   **Filtrage sélectif :** La configuration d'Atuin permet d'exclure certaines commandes ou répertoires de l'historique via des expressions régulières, créant des zones d'ombre volontaires.
*   **Gaps d'enregistrement :** Les shells non interactifs, les scripts ou les sessions où le hook d'initialisation n'est pas activé ne seront pas capturés.
*   **Manipulation de la source :** La présence d'une entrée dans la base ne garantit pas que la commande a été exécutée localement si la synchronisation est active ; elle peut provenir d'une autre machine.

#### Recommandations pour l'investigation
1.  **Localisation :** Rechercher les artefacts dans les dossiers conformes aux spécifications XDG (`~/.local/share/atuin/`). Vérifier systématiquement les fichiers de configuration (`config.toml`) pour identifier des chemins personnalisés.
2.  **Analyse de la base :** Utiliser des requêtes SQLite pour reconstruire la chronologie. Prioriser les fichiers `.db-wal` pour récupérer les entrées les plus récentes non encore fusionnées.
3.  **Récupération de données :** Interroger la colonne `deleted_at` pour identifier les activités effacées. Procéder à un carving standard sur les pages non allouées de la base SQLite.
4.  **Corrélation :** Croiser systématiquement les données d'Atuin avec les fichiers d'historique natifs du shell (`.bash_history`, `.zsh_history`) et les logs système (`syslog`/`journald`) pour confirmer la réalité d'une exécution.
5.  **Examen des hooks :** Vérifier les fichiers de configuration shell (`.bashrc`, `.zshrc`) pour confirmer l'activation d'Atuin et détecter d'éventuels filtres d'exclusion configurés par un attaquant pour masquer ses traces.

---
[Source](https://isc.sans.edu/diary/rss/33226){:target="_blank"}
