---
title: 'CFITSIO Fuzzing: Memory Corruptions and a Codex-Assisted Pipeline'
date: 2026-04-19
permalink: /posts/2026/04/19/cfitsio-fuzzing-memory-corruptions-and-a-codex-assisted-pipeline/
tags:
- veille-cyber
- zerodaysfans
---
### Automatisation de la recherche de vulnérabilités via IA : Étude de cas sur CFITSIO

Cet article détaille une méthodologie de fuzzing assistée par intelligence artificielle (Codex) appliquée à la bibliothèque **CFITSIO**, largement utilisée par la communauté astronomique pour manipuler le format de fichiers FITS. En se concentrant sur l'**Extended Filename Syntax (EFS)**, un parseur complexe capable d'exécuter des opérations de filtrage, l'auteur a identifié 16 vulnérabilités critiques liées à la gestion mémoire.

#### Points clés
*   **Approche automatisée :** L'auteur a mis en place un pipeline intégrant AFL++ (fuzzing), AFLtriage (tri des plantages) et un modèle de langage (Codex) pour analyser les causes racines et générer des correctifs.
*   **Surface d'attaque :** La syntaxe EFS (ex: `myfile.fits[FILTRE]`) expose la bibliothèque à des entrées non fiables traitées avant même l'ouverture du fichier.
*   **Efficacité de l'IA :** Codex a permis de déboguer rapidement des erreurs complexes, notamment des problèmes de priorité d'opérateurs en C, et de vérifier l'absence de régressions (fuites mémoires) dans les correctifs.

#### Vulnérabilités identifiées
La plupart des failles découvertes relèvent d'une gestion insécurisée des chaînes de caractères et des calculs d'index :
*   **Dépassements de tampon (Stack/Heap Overflow) :** Dus à des erreurs de calcul de taille (ex: `strncat` mal utilisé).
*   **Erreurs de priorité d'opérateurs :** Un exemple notable (`CFITSIO-EFS-01`) montre comment une priorité incorrecte entre les opérateurs `+` et `?:` a rendu une vérification de sécurité inopérante, permettant des corruptions mémoire.
*   **Fuites mémoires :** Introduites par une gestion incorrecte des pointeurs `realloc`.

*Note : Bien que l'article mentionne 16 vulnérabilités, les identifiants CVE spécifiques n'ont pas été listés dans le texte source.*

#### Recommandations
*   **Utilisation des API sécurisées :** Privilégier les fonctions de manipulation de chaînes de caractères qui effectuent des vérifications de limites strictes.
*   **Validation des entrées :** Désinfecter systématiquement les noms de fichiers provenant de sources externes avant de les passer à des fonctions comme `fits_open_file`.
*   **Adoption de l'automatisation :** Intégrer des outils de génération de correctifs basés sur l'IA dans les pipelines CI/CD pour accélérer la remédiation et détecter les erreurs de logique ou de priorité d'opérateurs, souvent invisibles lors de revues manuelles rapides.
*   **Utiliser les alternatives sécurisées :** Préférer `fits_open_diskfile` plutôt que `fits_open_file` lorsque l'interprétation EFS n'est pas nécessaire.

---
[Source](https://blog.doyensec.com/2026/04/20/cfitsio-fuzzing.html){:target="_blank"}
