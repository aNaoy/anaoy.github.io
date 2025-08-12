---
title: 'Docker Hub still hosts dozens of Linux images with the XZ backdoor'
date: 2025-08-12
permalink: /posts/2025/08/12/docker-hub-still-hosts-dozens-of-linux-images-with-the-xz-backdoor/
tags:
- veille-cyber
- bleepingcomp
---
## L'ombre de la porte dérobée XZ plane toujours sur Docker Hub

Au moins 35 images Linux sur Docker Hub continuent d'héberger la porte dérobée XZ-Utils, découverte en mars 2024. Cette situation expose les utilisateurs, les organisations et leurs données à des risques potentiels, car de nombreux systèmes de production et pipelines CI/CD utilisent ces images comme base pour leurs propres conteneurs.

La porte dérobée, référencée sous **CVE-2024-3094**, était dissimulée dans la bibliothèque `liblzma.so` des versions 5.6.0 et 5.6.1 de l'outil de compression xz-utils. Elle permettait de contourner l'authentification SSH et d'exécuter des commandes à distance avec des privilèges root, en exploitant le mécanisme IFUNC de glibc pour intercepter la fonction `RSA_public_decrypt`.

Des chercheurs ont constaté que certaines de ces images compromises sont toujours disponibles publiquement, et que d'autres images ont été construites à partir de ces bases infectées, créant ainsi des contaminations transitives. Malgré cela, Debian a choisi de ne pas retirer de Docker Hub les images concernées utilisant les versions compromises de la bibliothèque, arguant d'un faible risque d'exploitation et de l'importance de la continuité archivistique. Cette décision est contestée par les chercheurs qui soulignent le risque d'installations accidentelles ou d'utilisation dans des constructions automatisées.

### Points Clés :

*   La porte dérobée XZ-Utils affecte toujours des images Linux sur Docker Hub.
*   Les images compromises peuvent entraîner une infection des conteneurs qui en dépendent.
*   Debian a choisi de conserver des images vulnérables sur Docker Hub, les considérant comme des artefacts historiques.

### Vulnérabilités :

*   **CVE-2024-3094** : Porte dérobée dans les versions 5.6.0 et 5.6.1 de xz-utils. Permet un accès root à distance via SSH en contournant l'authentification.

### Recommandations :

*   Utiliser uniquement des images Docker à jour.
*   Vérifier manuellement que la bibliothèque xz-utils est à la version 5.6.2 ou ultérieure (la dernière stable étant 5.8.1).
*   Être vigilant quant aux images utilisées comme couches de base dans les pipelines de développement et de production.

---
[Source](https://www.bleepingcomputer.com/news/security/docker-hub-still-hosts-dozens-of-linux-images-with-the-xz-backdoor/){:target="_blank"}
