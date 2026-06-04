---
title: 'Microsofts Coreutils for Windows, (Thu, Jun 4th)'
date: 2026-06-04
permalink: /posts/2026/06/04/microsofts-coreutils-for-windows-thu-jun-4th/
tags:
- veille-cyber
- sans-isc
---
### Lancement des Microsoft Coreutils pour Windows

Microsoft a officiellement publié sa propre version des utilitaires GNU (`coreutils`) pour Windows, offrant une alternative moderne aux anciennes versions GnuWin32.

**Points clés :**
* **Développement :** L'ensemble est compilé en Rust dans un exécutable unique (`coreutils.exe`).
* **Architecture :** Chaque commande individuelle est implémentée via un lien physique (*hard link*) pointant vers l'exécutable principal.
* **Installation :** Disponible via l'outil de gestion de paquets `winget` (`winget install Microsoft.Coreutils`) ou par un installateur disponible sur GitHub.
* **Contenu :** Le paquet inclut les commandes classiques de l'environnement Unix (ex: `ls`, `cat`, `grep`, `rm`, `find`, `sha256sum`, etc.).

**Vulnérabilités :**
* Aucune vulnérabilité n'est mentionnée dans cet article.

**Recommandations :**
* Privilégier l'installation via `winget` pour faciliter la gestion et les mises à jour.
* Vérifier l'intégration dans le PATH système après l'installation pour s'assurer que les commandes sont accessibles depuis le terminal.

---
[Source](https://isc.sans.edu/diary/rss/33048){:target="_blank"}
