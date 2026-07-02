---
title: 'Opera rolls out Paste Protect feature to fight ClickFix attacks'
date: 2026-07-02
permalink: /posts/2026/07/02/opera-rolls-out-paste-protect-feature-to-fight-clickfix-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Protection contre les attaques ClickFix : Opera déploie "Paste Protect"

Opera a lancé la fonctionnalité « Paste Protect » pour contrer les attaques de type « ClickFix », une technique d'ingénierie sociale consistant à tromper les utilisateurs en les incitant à copier et exécuter des commandes malveillantes dans leur terminal. Ces commandes, souvent présentées comme des procédures de vérification ou des correctifs techniques, permettent aux attaquants d'exécuter du code avec les privilèges de l'utilisateur, facilitant ainsi l'installation de logiciels malveillants de type *infostealer*.

**Points clés :**
*   **Fonctionnement :** La technologie utilise des règles de détection spécifiques à chaque plateforme (Windows, macOS, Linux) pour analyser le contenu copié dans le presse-papiers.
*   **Réaction du système :** En cas de détection de script suspect, l'opération de copie est bloquée, une alerte est affichée dans la barre d'adresse, et l'utilisateur peut visualiser les 120 premiers caractères du code.
*   **Flexibilité :** Un délai de sécurité de 5 secondes est imposé avant toute autorisation manuelle. Les utilisateurs peuvent également définir des listes blanches pour des sites de confiance (ex: GitHub).
*   **Vulnérabilité :** Il s'agit d'une vulnérabilité liée au comportement humain (ingénierie sociale) exploitant le presse-papiers pour contourner les défenses système (pas de CVE spécifique attribuée, car il s'agit d'un vecteur d'attaque global et non d'une faille logicielle isolée).

**Recommandations :**
*   **Activation :** La fonctionnalité est activée par défaut dans les dernières versions d'Opera. Les paramètres sont accessibles via *Paramètres > Confidentialité et sécurité > Paste Protect*.
*   **Prudence :** Ne jamais copier-coller ou exécuter des commandes trouvées en ligne dont vous ne comprenez pas parfaitement la nature ou la provenance.
*   **Gestion des permissions :** N'ajoutez des sites à votre liste blanche que si vous avez une confiance absolue dans la source et le contenu des scripts manipulés.

---
[Source](https://www.bleepingcomputer.com/news/security/opera-rolls-out-paste-protect-feature-to-fight-clickfix-attacks/){:target="_blank"}
