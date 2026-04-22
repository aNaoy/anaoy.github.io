---
title: 'New npm supply-chain attack self-spreads to steal auth tokens'
date: 2026-04-22
permalink: /posts/2026/04/22/new-npm-supply-chain-attack-self-spreads-to-steal-auth-tokens/
tags:
- veille-cyber
- bleepingcomp
---
### Propagation virale via des paquets npm compromis

Une nouvelle campagne d'attaque par chaîne d'approvisionnement cible l'écosystème **npm** en exploitant des comptes développeurs pour injecter du code malveillant dans des paquets légitimes. Le malware agit comme un ver informatique capable de s'auto-propager en utilisant les jetons d'authentification trouvés sur les systèmes infectés pour republier automatiquement des versions corrompues de paquets.

**Points clés :**
*   **Cibles :** Outils d'IA et opérations de bases de données (paquets de Namastex Labs).
*   **Mécanisme :** Le script identifie les jetons npm dans les variables d'environnement ou les fichiers `~/.npmrc` pour modifier et republier des paquets avec un numéro de version incrémenté.
*   **Polyvalence :** L'attaque s'étend aux environnements Python (via des fichiers `.pth`) et tente de voler des clés API, des accès cloud, des configurations Kubernetes/Docker, ainsi que des portefeuilles de cryptomonnaies (MetaMask, Exodus, etc.).
*   **Vulnérabilités :** Aucune CVE spécifique n'est associée, l'attaque repose sur l'exfiltration de secrets de développement et l'abus de privilèges d'accès aux registres de paquets.

**Recommandations :**
*   **Suppression immédiate :** Identifier et supprimer les paquets infectés (ex: `@automagik/genie`, `pgserve`, etc.) des pipelines CI/CD et des environnements de développement.
*   **Rotation des secrets :** Révoquer et renouveler systématiquement toutes les clés API, jetons d'authentification (npm, PyPI), mots de passe SSH et identifiants cloud potentiellement exposés.
*   **Audit de sécurité :** Examiner les journaux pour détecter des comportements anormaux liés à l'exécution de scripts `postinstall` et vérifier l'intégrité des caches et miroirs de paquets internes.

---
[Source](https://www.bleepingcomputer.com/news/security/new-npm-supply-chain-attack-self-spreads-to-steal-auth-tokens/){:target="_blank"}
