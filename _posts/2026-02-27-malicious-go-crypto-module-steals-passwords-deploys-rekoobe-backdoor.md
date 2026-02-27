---
title: 'Malicious Go Crypto Module Steals Passwords, Deploys Rekoobe Backdoor'
date: 2026-02-27
permalink: /posts/2026/02/27/malicious-go-crypto-module-steals-passwords-deploys-rekoobe-backdoor/
tags:
- veille-cyber
- hackernews
---
### Module Go Malveillant Exploitant la Confiance pour Déployer Rekoobe

Une campagne de cybercriminalité exploite un module Go malveillant, camouflé sous l'apparence d'une bibliothèque cryptographique légitime (`github.com/xinfeisoft/crypto`). Ce module intercepte les informations d'identification sensibles saisies par les utilisateurs, telles que les mots de passe, lorsqu'elles sont traitées par des applications vulnérables. Il est conçu pour abuser de la confusion de nom d'espace et de l'imitation du projet officiel `golang.org/x/crypto`.

Une fois les secrets collectés, le module exécute un script récupéré à distance. Ce script a pour rôle principal de permettre un accès persistant via SSH en ajoutant une clé publique à la liste des clés autorisées (`~/.ssh/authorized_keys`). Il tente également de relâcher les restrictions du pare-feu en configurant les règles `iptables` pour accepter tout trafic, avant de télécharger et d'exécuter des charges utiles supplémentaires masquées avec l'extension `.mp5`.

Parmi les charges utiles téléchargées, une sert à vérifier la connectivité Internet et à communiquer avec une adresse IP spécifique. L'autre charge utile est Rekoobe, un cheval de Troie Linux connu, utilisé depuis au moins 2015 et notamment par des groupes liés à la Chine comme APT31. Rekoobe est capable de recevoir des commandes pour télécharger d'autres malwares, voler des fichiers et établir une connexion shell inversée.

**Points Clés :**

*   **Imitation et Confusion de Nom :** Le module malveillant `github.com/xinfeisoft/crypto` se fait passer pour un composant légitime du projet Go, exploitant la confiance des développeurs dans les dépôts populaires.
*   **Vol de Mots de Passe :** Le code malveillant est injecté dans la fonction `ReadPassword()` du package `ssh/terminal/terminal.go`, permettant la capture de toutes les données sensibles tapées par l'utilisateur lors de l'appel à cette fonction.
*   **Persistance et Escalade :** Le module établit un accès persistant via SSH et tente d'assouplir les défenses réseau locales.
*   **Déploiement de Backdoor Rekoobe :** L'objectif final est de télécharger et d'exécuter Rekoobe, un backdoor Linux sophistiqué utilisé dans des campagnes de ciblage, y compris par des acteurs étatiques.

**Vulnérabilités :**

*   Aucune vulnérabilité logicielle spécifique (CVE) n'est mentionnée directement dans l'article concernant le module Go ou Rekoobe. L'exploitation repose sur la **confiance dans les dépendances logicielles** (supply chain attack) et l'**ingénierie sociale** (imitation de nom).

**Recommandations :**

*   **Vérification rigoureuse des dépendances :** Examiner attentivement les nouvelles dépendances ajoutées aux projets et s'assurer de leur légitimité.
*   **Surveillance des activités réseau :** Surveiller les communications sortantes suspectes vers des adresses IP ou des ports inhabituels.
*   **Gestion proactive des clés SSH :** Examiner et auditer régulièrement les fichiers `authorized_keys` sur les serveurs.
*   **Sécurisation des pare-feux :** Assurer une configuration de pare-feu stricte et surveiller toute modification non autorisée.
*   **Sensibilisation aux attaques par chaîne d'approvisionnement :** Les développeurs doivent être conscients des risques liés à l'utilisation de bibliothèques tierces et adopter des pratiques de sécurité robustes.
*   Les équipes de sécurité Go ont pris des mesures pour bloquer ce module malveillant. Cependant, le modèle d'attaque "low-effort et high-impact" laisse présager des attaques similaires à l'avenir, ciblant d'autres bibliothèques sensibles et utilisant des techniques d'obfuscation pour contourner la détection.

---
[Source](https://thehackernews.com/2026/02/malicious-go-crypto-module-steals.html){:target="_blank"}
