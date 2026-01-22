---
title: 'Malicious PyPI Package Impersonates SymPy, Deploys XMRig Miner on Linux Hosts'
date: 2026-01-22
permalink: /posts/2026/01/22/malicious-pypi-package-impersonates-sympy-deploys-xmrig-miner-on-linux-hosts/
tags:
- veille-cyber
- hackernews
---
**Malware PyPI : Le mineur de cryptomonnaie XMRig se déguise en SymPy**

Un nouveau paquet malveillant, nommé `sympy-dev`, a été découvert sur le Python Package Index (PyPI). Ce paquet se fait passer pour une version de développement de la bibliothèque populaire de calcul symbolique SymPy afin de tromper les développeurs. Une fois installé, il déploie un mineur de cryptomonnaie XMRig sur les systèmes Linux ciblés.

Ce logiciel malveillant modifie des fonctions spécifiques de la bibliothèque pour agir comme un téléchargeur. Il récupère une configuration JSON à distance et un exécutable ELF, qu'il lance ensuite directement en mémoire à l'aide de techniques comme `memfd_create` et `/proc/self/fd`. Cette méthode vise à minimiser les traces sur le disque. Les chercheurs ont observé que cette technique est similaire à celles utilisées par des campagnes de cryptojacking antérieures comme FritzFrog et Mimo.

L'objectif final de cette attaque est d'utiliser les ressources CPU des machines compromises pour miner de la cryptomonnaie Monero (XMR) via le mineur XMRig, en utilisant des connexions chiffrées sur le port 3333. Il est important de noter que ce code malveillant pourrait potentiellement servir de charge utile plus générale, capable de télécharger et d'exécuter tout autre code.

**Points Clés :**

*   **Usurpation d'identité :** Le paquet `sympy-dev` imite SymPy pour gagner la confiance des utilisateurs.
*   **Déploiement furtif :** Le code malveillant s'exécute en mémoire pour éviter la détection sur le système de fichiers.
*   **Mineur de cryptomonnaie :** La charge utile principale est un mineur XMRig pour le minage de Monero.
*   **Flexibilité :** L'implant peut servir de charge utile polyvalente pour d'autres codes malveillants.

**Vulnérabilités / Menaces :**

*   Aucune vulnérabilité spécifique (avec un identifiant CVE) n'est explicitement mentionnée dans l'article concernant le paquet malveillant lui-même ou l'environnement d'installation (PyPI). La menace réside dans l'ingénierie sociale et la distribution via une plateforme de confiance.

**Recommandations :**

*   **Vérification rigoureuse des dépendances :** Les développeurs doivent faire preuve d'une extrême prudence lors de l'installation de paquets à partir de dépôts publics comme PyPI, en vérifiant attentivement les noms des paquets et leurs origines.
*   **Surveillance de l'activité système :** Surveiller l'utilisation inhabituelle du CPU, qui pourrait indiquer un processus de minage de cryptomonnaie.
*   **Maintien à jour des outils de sécurité :** Utiliser des outils de sécurité et des antivirus à jour pour détecter et bloquer les logiciels malveillants connus.
*   **Limitation des privilèges :** Exécuter les processus avec les privilèges minimaux nécessaires pour limiter l'impact potentiel d'une compromission.

---
[Source](https://thehackernews.com/2026/01/malicious-pypi-package-impersonates.html){:target="_blank"}
