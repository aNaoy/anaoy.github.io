---
title: 'ThreatsDay Bulletin: Smart TV Proxyware, 24-Year curl Bug, AI Crime Forums + 13 More Stories'
date: 2026-06-25
permalink: /posts/2026/06/25/threatsday-bulletin-smart-tv-proxyware-24-year-curl-bug-ai-crime-forums-13-more-stories/
tags:
- veille-cyber
- hackernews
---
### Actualités cybersécurité : Vulnérabilités critiques et menaces émergentes

Le paysage actuel des menaces montre que les attaquants exploitent principalement des vecteurs simples et persistants : identifiants obsolètes, confiance mal placée dans les applications, fausses mises à jour et ingénierie sociale.

#### Points clés et menaces majeures
*   **Proxyware sur Smart TV :** Plus d'un tiers des applications sur LG webOS et Samsung Tizen intègrent des kits de développement (SDK) transformant les téléviseurs en nœuds de proxy résidentiels à l'insu des propriétaires.
*   **Convergence État-Cybercriminalité :** Les acteurs étatiques adoptent de plus en plus les outils et tactiques (dont les rançongiciels) des groupes criminels pour masquer leurs opérations d'espionnage.
*   **Phishing collaboratif :** Exploitation des fonctionnalités de partage de Microsoft 365 et Outlook pour rendre les attaques par hameçonnage plus légitimes via des invitations ou des fichiers partagés.
*   **Adoption de l'IA par le crime :** Les forums underground débattent de l'intégration de l'IA pour le développement de malwares, l'automatisation de l'ingénierie sociale et le tri de données volées.
*   **Cyber-surveillance :** Des failles dans le contrôle des exportations de l'UE permettent à des entreprises, comme la bulgare Circles, de vendre des outils de surveillance à des régimes autoritaires.

#### Vulnérabilités identifiées
*   **Hoppscotch (CVE-2026-50160 - Score 10.0/10) :** Faille critique d'assignation de masse dans l'API permettant à un attaquant non authentifié de compromettre totalement le serveur et de voler les clés de signature JWT.
*   **Bibliothèque curl (6 vulnérabilités) :** Notamment **CVE-2026-8932**, un bug vieux de 24 ans permettant la réutilisation de connexions malgré des configurations mTLS contradictoires. 

#### Campagnes malveillantes notables
*   **Edgecution :** Extension Edge malveillante utilisée par des courtiers d'accès pour interagir avec les applications natives du système et exécuter du code arbitraire.
*   **ClickFix / AMOS (Atomic macOS Stealer) :** Campagnes ciblant macOS via des commandes copier-coller dans le Terminal ou des fichiers DMG piégés pour voler des portefeuilles crypto et des données sensibles.
*   **BitB (Browser-in-the-Browser) :** Utilisation de fenêtres pop-up contrefaites pour simuler des mises à jour logicielles ou des pages de connexion Microsoft 365 afin de dérober des identifiants.

#### Recommandations de sécurité
*   **Gestion des accès :** Révoquer systématiquement les accès tiers ou les identifiants utilisés pour des projets pilotes passés.
*   **Mise à jour :** Passer immédiatement à **curl 8.21.0** et **Hoppscotch-backend 2026.5.0**.
*   **Audit des équipements :** Traiter les appareils connectés (Smart TV, IoT) comme des ordinateurs et surveiller leur activité réseau, car ils servent souvent de points d'entrée discrets.
*   **Surveillance administrative :** Activer les alertes sur *tous* les changements de mot de passe des comptes administrateurs, et non uniquement pour les super-administrateurs.
*   **Formation utilisateur :** Sensibiliser sur les méthodes de "phishing collaboratif" et la méfiance envers les invites de copie de commandes dans le terminal.

---
[Source](https://thehackernews.com/2026/06/threatsday-bulletin-smart-tv-proxyware.html){:target="_blank"}
