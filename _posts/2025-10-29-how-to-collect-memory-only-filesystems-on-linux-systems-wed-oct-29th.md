---
title: 'How to collect memory-only filesystems on Linux systems, (Wed, Oct 29th)'
date: 2025-10-29
permalink: /posts/2025/10/29/how-to-collect-memory-only-filesystems-on-linux-systems-wed-oct-29th/
tags:
- veille-cyber
- sans-isc
---
### Collecte d'informations sur les systèmes de fichiers en mémoire sous Linux

Les attaquants utilisent fréquemment les systèmes de fichiers résidant uniquement en mémoire, tels que `/dev/shm` ou d'autres emplacements `tmpfs`, pour dissimuler des outils malveillants ou préparer l'exfiltration de données. Une méthode efficace pour collecter des données forensiques à partir de ces systèmes consiste à acquérir d'abord les métadonnées (informations sur les inodes) avant de capturer le contenu des fichiers, afin d'éviter de modifier les horodatages d'accès.

**Points clés :**

*   Les systèmes de fichiers `tmpfs` ne peuvent pas être directement imagés de manière forensiquement saine à l'aide d'outils comme `dd` car ils n'ont pas de périphérique bloc sous-jacent.
*   La collecte séquentielle des métadonnées, puis du contenu, est cruciale pour préserver l'intégrité des horodatages.
*   Cette technique s'est avérée efficace sur de nombreux systèmes Linux, y compris des systèmes dérivés de Unix comme les routeurs Juniper et d'anciennes versions de Solaris.

**Vulnérabilités / Défis :**

*   Certains systèmes peuvent manquer de la commande `stat`, limitant la collecte aux seuls contenus des fichiers.
*   Les versions de `coreutils` antérieures à 8.32 peuvent ne pas utiliser l'appel système `statx()` pour accéder à l'horodatage de création, même si celui-ci est présent dans l'inode sur les systèmes récents.

**Recommandations :**

*   **Collecte des métadonnées :** Utiliser la commande `find` pour parcourir le système de fichiers `tmpfs` (par exemple, `/dev/shm`) et exécuter `stat` sur chaque élément. L'option `-exec $(which stat) -c '0|%N|%i|%A|%u|%g|%s|%X|%Y|%Z|%W'` permet de recueillir des informations détaillées sur les fichiers. L'utilisation de `sed` est nécessaire pour compenser les versions de `stat` qui ne prennent pas en charge le format `%W` (temps de création). Les sorties sont envoyées à un système distant via `ssh` dans un format `bodyfile` pour être traitées par `mactime` (The Sleuth Kit) afin de générer une chronologie du système de fichiers.
    ```bash
    find /dev/shm -exec $(which stat) -c '0|%N|%i|%A|%u|%g|%s|%X|%Y|%Z|%W' {} \; | sed -e 's/|W$/|0/' -e s'/|?$/|0/' | ssh foo@system "cat - > $(hostname)-dev-shm-bodyfile"
    ```
*   **Collecte du contenu des fichiers :** Une fois les métadonnées collectées, utiliser `find` pour localiser les fichiers réguliers (`-type f`) et les envoyer à `tar` pour la compression et l'archivage. La sortie est ensuite transmise via `ssh` vers le système de collecte.
    ```bash
    find /dev/shm -type f -print | tar czvO -T - | ssh foo@system "cat - > $(hostname)-dev-shm-fs.tgz"
    ```
*   Il est recommandé de hacher les fichiers sur le système source avant la collecte, bien que le hachage de l'archive résultante sur le système de destination soit une pratique courante.

---
[Source](https://isc.sans.edu/diary/rss/32432){:target="_blank"}
