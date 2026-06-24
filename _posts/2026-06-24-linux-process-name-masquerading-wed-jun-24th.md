---
title: 'Linux Process Name Masquerading, (Wed, Jun 24th)'
date: 2026-06-24
permalink: /posts/2026/06/24/linux-process-name-masquerading-wed-jun-24th/
tags:
- veille-cyber
- sans-isc
---
### Dissimulation de processus sous Linux : Technique et détection

La technique de masquage de nom de processus (référencée sous l'identifiant **MITRE ATT&CK T1036**) permet à un logiciel malveillant de se faire passer pour un processus légitime afin d'échapper à la surveillance des analystes.

**Points clés :**
*   **Emplacements cibles :** Sous Linux, le nom d'un processus est stocké dans deux fichiers principaux du répertoire `/proc/<pid>/` :
    *   `comm` : Limité à 15 caractères, utilisé par `ps` et `top`.
    *   `cmdline` : Contient la ligne de commande complète (arguments), utilisée par `ps aux` ou `pgrep -f`.
*   **Méthodologie d'attaque :**
    *   La modification du fichier `comm` est réalisable via l'appel système `prctl(PR_SET_NAME)`.
    *   La modification de `cmdline` est plus complexe car le buffer est fixe. Les attaquants contournent cette limite en écrasant la zone mémoire contiguë allouée aux arguments (`argv`) et aux variables d'environnement (`environ`).

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle spécifique (CVE), mais d'une **limitation architecturale** inhérente au fonctionnement des systèmes d'exploitation (Linux et Windows via le PEB). Le système fait confiance aux informations déclarées en mode utilisateur, qui peuvent être altérées par le processus lui-même.

**Recommandations :**
*   **Ne pas se fier uniquement aux outils standards :** Les commandes `ps`, `top` ou `htop` lisent des données qui peuvent être falsifiées.
*   **Utiliser des outils basés sur eBPF :** Des solutions comme **Kunai** permettent de capturer la ligne de commande réelle au moment de l'exécution et de corréler les événements, rendant le masquage inopérant.
*   **Analyse comportementale :** Privilégier la surveillance des arbres de processus (ancêtres) et des chemins d'exécution réels plutôt que les simples noms affichés.
*   **Sur Windows :** Garder à l'esprit que si le PEB est modifiable par l'attaquant, le noyau (EPROCESS) conserve une trace immuable du chemin d'image réel, accessible via des outils d'analyse forensique avancés ou des terminaux kernel.

---
[Source](https://isc.sans.edu/diary/rss/33102){:target="_blank"}
