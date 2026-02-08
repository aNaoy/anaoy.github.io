---
title: 'New tool blocks imposter attacks disguised as safe commands'
date: 2026-02-08
permalink: /posts/2026/02/08/new-tool-blocks-imposter-attacks-disguised-as-safe-commands/
tags:
- veille-cyber
- bleepingcomp
---
### Tirith : un outil pour contrer les attaques par homoglyphes dans les lignes de commande

Un nouvel outil open-source et multiplateforme nommé Tirith permet de détecter et de bloquer les attaques par homoglyphes dans les environnements de ligne de commande. Il analyse les URL présentes dans les commandes tapées par l'utilisateur et interrompt leur exécution. Tirith s'intègre aux shells populaires (zsh, bash, fish, PowerShell) en inspectant chaque commande avant son exécution.

L'objectif principal est de contrecarrer les techniques d'usurpation qui s'appuient sur des URL contenant des symboles issus de différents alphabets. Ces symboles peuvent paraître identiques ou très similaires à l'œil humain, mais sont interprétés différemment par l'ordinateur. Les attaquants exploitent cela pour créer des noms de domaine qui ressemblent à des marques légitimes, mais qui redirigent vers des serveurs contrôlés par l'attaquant lorsque l'URL est résolue. Bien que les navigateurs aient partiellement résolu ce problème, les terminaux restent vulnérables en raison de leur capacité à afficher des caractères Unicode, des séquences d'échappement ANSI et des caractères invisibles.

Tirith est capable de détecter et bloquer plusieurs types d'attaques :
*   **Attaques par homographe** : utilisation de caractères Unicode ressemblants dans les domaines, le punycode, et les scripts mixtes.
*   **Injection dans le terminal** : usage de séquences d'échappement ANSI, de substitutions bidirectionnelles, et de caractères de largeur nulle.
*   **Schémas de redirection vers un shell** : comme `curl | bash` ou `wget | sh`.
*   **Détournement de fichiers de configuration** : tels que `~/.bashrc` ou `~/.ssh/authorized_keys`.
*   **Transport non sécurisé** : comme l'utilisation de HTTP avec des commandes shell, ou la désactivation de TLS.
*   **Risques de la chaîne d'approvisionnement** : dépôts Git avec typosquatting, registres Docker non fiables.
*   **Exposition d'identifiants** : URL avec `userinfo`, raccourcisseurs cachant la destination réelle.

Des exemples passés incluent des campagnes de phishing utilisant des caractères Unicode trompeurs pour usurper des sites comme Booking.com, et des attaques de type ClickFix exploitant des caractères cachés dans les commandes pour déployer des malwares. Tirith fonctionne sur Windows, Linux et macOS. L'outil garantit que toutes les analyses sont effectuées localement, sans appels réseau, et sans modifier les commandes de l'utilisateur. Il ne s'exécute pas en arrière-plan et ne nécessite aucune connexion ou clé API.

**Points Clés :**
*   Détection des attaques par homoglyphes dans les lignes de commande.
*   Intégration avec divers shells (zsh, bash, fish, PowerShell).
*   Analyse des URL et des commandes pour identifier les caractères trompeurs.
*   Fonctionnement local et sécurisé, sans transmission de données.
*   Compatibilité multiplateforme (Windows, Linux, macOS).

**Vulnérabilités / Types d'attaques détectées :**
*   Attaques par homographe (Unicode lookalike characters, punycode, mixed scripts).
*   Injection dans le terminal (ANSI escapes, bidi overrides, zero-width chars).
*   Pipe-to-shell patterns (`curl | bash`, `wget | sh`, `eval $(…)`)
*   Dotfile hijacking (`~/.bashrc`, `~/.ssh/authorized_keys`)
*   Insecure transport (HTTP to shell, TLS disabled)
*   Supply-chain risks (typosquatted git repos, untrusted Docker registries)
*   Credential exposure (userinfo URLs, shorteners hiding destinations)

**Recommandations :**
*   Utiliser Tirith pour renforcer la sécurité lors de l'exécution de commandes dans un terminal.
*   Être particulièrement vigilant avec les URL et les commandes provenant de sources externes.
*   Considérer l'installation de Tirith via les gestionnaires de paquets disponibles (Homebrew, apt/dnf, npm, Cargo, Nix, Scoop, Chocolatey, Docker).

---
[Source](https://www.bleepingcomputer.com/news/security/new-tool-blocks-imposter-attacks-disguised-as-safe-commands/){:target="_blank"}
