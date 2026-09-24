---
title: 'Placeholder domain used in dev docs now serves ClickFix attacks'
date: 2026-09-24
permalink: /posts/2026/09/24/placeholder-domain-used-in-dev-docs-now-serves-clickfix-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement du domaine « third-party.com » pour des attaques ClickFix

Le domaine « third-party.com », largement utilisé par erreur dans la documentation technique et le code open-source comme espace réservé (placeholder), est actuellement exploité pour mener des attaques de type **ClickFix**. Contrairement aux domaines réservés comme « example.com », ce domaine est actif et ses propriétaires actuels l'utilisent pour piéger les développeurs et les utilisateurs.

**Points clés :**
*   **Méthodologie ClickFix :** Le site affiche une fausse vérification Cloudflare (CAPTCHA). Une fois le bouton cliqué, un script malveillant est copié dans le presse-papier de l'utilisateur.
*   **Ingénierie sociale :** La victime est invitée à effectuer une combinaison de touches (`Windows + R`, `Ctrl + V`, `Entrée`), exécutant ainsi un script PowerShell qui télécharge et installe une charge utile malveillante.
*   **Ciblage sélectif :** L'attaque ne s'exécute que sur Windows. Les utilisateurs sous Linux ou macOS reçoivent un message indiquant que leur système n'est pas supporté, ce qui permet à l'attaque d'échapper à la détection par les outils d'analyse automatisés.
*   **Risque lié à la documentation :** Des milliers de dépôts (incluant des projets comme Chromium) contiennent des références à ce domaine. Si des développeurs copient ces exemples sans les modifier, leurs applications ou outils pourraient être redirigés vers cette page malveillante.

**Vulnérabilités :**
*   **CVE :** Aucune vulnérabilité logicielle (CVE) spécifique n'est exploitée ; il s'agit d'une attaque par ingénierie sociale utilisant les fonctionnalités natives de Windows (Presse-papier et PowerShell).
*   **Vecteur :** Abus de confiance envers des domaines présentés comme exemples dans la documentation technique.

**Recommandations :**
*   **Auditer le code :** Rechercher dans les bases de code, les documentations internes et les configurations les occurrences de `third-party.com` et les remplacer par des domaines réservés légitimes tels que `example.com`, `example.net` ou `example.org`.
*   **Vigilance utilisateur :** Ne jamais suivre d'instructions consistant à copier/coller des commandes inconnues dans l'exécuteur de commandes Windows (Win+R) ou dans un terminal, particulièrement suite à une demande de type CAPTCHA sur une page web.
*   **Filtrage :** Envisager de bloquer le domaine `third-party.com` au niveau du pare-feu ou du serveur DNS de l'entreprise pour prévenir toute interaction accidentelle.

---
[Source](https://www.bleepingcomputer.com/news/security/placeholder-domain-used-in-dev-docs-now-serves-clickfix-attacks/){:target="_blank"}
