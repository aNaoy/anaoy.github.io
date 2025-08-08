---
title: 'Fake WhatsApp developer libraries hide destructive data-wiping code'
date: 2025-08-08
permalink: /posts/2025/08/08/fake-whatsapp-developer-libraries-hide-destructive-data-wiping-code/
tags:
- veille-cyber
- bleepingcomp
---
Bibliothèques NPM et Go malveillantes utilisées pour la suppression de données

Deux bibliothèques NPM malveillantes, `naya-flore` et `nvlore-hsc`, ont été découvertes dans le registre NPM. Elles se font passer pour des outils de développement WhatsApp et visent les développeurs en leur envoyant un code de suppression de données qui supprime récursivement les fichiers sur leur machine. Ces bibliothèques imitent des bibliothèques légitimes utilisées pour l'API WhatsApp Business. Un mécanisme de "kill switch" basé sur une liste de numéros de téléphone indonésiens est présent pour exclure certaines cibles de l'attaque. De plus, une fonction d'exfiltration de données, bien que désactivée pour le moment, a également été détectée.

Parallèlement, 11 paquets Go malveillants ont été identifiés. Ils utilisent des techniques d'obfuscation pour exécuter des charges utiles à distance, ciblant les serveurs CI Linux et les stations de travail Windows. La plupart de ces paquets sont des typosquats, cherchant à tromper les développeurs par des noms similaires à ceux de paquets légitimes.

**Points Clés :**

*   Existence de paquets NPM et Go malveillants conçus pour cibler les développeurs.
*   Les paquets NPM imitant des bibliothèques WhatsApp Business.
*   Capacité des paquets malveillants à supprimer des fichiers de manière récursive (`rm -rf *`).
*   Présence d'un mécanisme de "kill switch" pour exclure certaines cibles.
*   Détection d'une fonction d'exfiltration de données potentielle (actuellement désactivée).
*   Utilisation de typosquatting et d'obfuscation pour dissimuler les paquets Go malveillants.
*   Les paquets malveillants sont toujours disponibles dans certains registres au moment de la rédaction.

**Vulnérabilités (non spécifiées avec CVE) :**

*   Les paquets NPM `naya-flore` et `nvlore-hsc` exécutent une commande de suppression de fichiers destructive.
*   Les paquets Go exécutent des charges utiles à distance obtenues via des domaines .icu ou .tech.

**Recommandations :**

*   Faire preuve d'une extrême prudence lors de l'utilisation de bibliothèques tierces, surtout celles se faisant passer pour des outils populaires.
*   Vérifier attentivement la provenance et la réputation des paquets avant de les intégrer dans des projets.
*   Surveiller les mises à jour de sécurité et les annonces de vulnérabilités dans les registres de paquets.
*   Éviter d'utiliser des paquets dont le nom est similaire à des paquets légitimes (typosquatting).

---
[Source](https://www.bleepingcomputer.com/news/security/fake-whatsapp-developer-libraries-hide-destructive-data-wiping-code/){:target="_blank"}
