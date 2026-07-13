---
title: 'New MemGhost Attack Plants Persistent False Memories in AI Agents Through One Email'
date: 2026-07-13
permalink: /posts/2026/07/13/new-memghost-attack-plants-persistent-false-memories-in-ai-agents-through-one-email/
tags:
- veille-cyber
- hackernews
---
### La menace MemGhost : Injection de faux souvenirs persistants dans les agents IA

L'attaque par **injection de mémoire furtive** (Stealth Memory Injection), baptisée **MemGhost**, permet à un attaquant de modifier durablement le comportement d'un agent IA personnel via un simple e-mail piégé. Contrairement aux attaques précédentes qui visaient le vol de données ponctuel, MemGhost exploite la capacité des agents à lire des e-mails et à écrire dans leurs propres fichiers de mémoire persistante pour y introduire de fausses informations qui influencent toutes les sessions ultérieures de l'utilisateur.

**Points clés :**
*   **Mécanisme :** L'outil génère automatiquement un e-mail contenant des instructions déguisées. Lorsque l'agent traite cet e-mail, il interprète les instructions comme des faits légitimes et les écrit dans ses fichiers de configuration ou de mémoire (ex: `MEMORY.md`).
*   **Persistance :** Une fois le "faux souvenir" injecté, l'agent l'utilise lors de chaque nouvelle interaction, modifiant ses réponses ou ses actions sans que l'utilisateur ne s'en aperçoive.
*   **Discrétion :** L'attaque réussit dans plus de 80 % des cas en mode arrière-plan, car l'agent n'affiche généralement pas ses opérations de lecture/écriture de fichiers dans l'interface de chat.
*   **Précédents :** Cette vulnérabilité s'inscrit dans la lignée de failles comme **CVE-2025-32711 (EchoLeak)**, qui permettait déjà d'exfiltrer des données via des commandes cachées.

**Vulnérabilités :**
*   Absence de cloisonnement entre les données entrantes non fiables (e-mails) et la mémoire persistante de l'agent.
*   Manque de traçabilité et de transparence sur les modifications apportées aux fichiers de configuration par l'IA.
*   Défaut de validation humaine pour les écritures en mémoire.

**Recommandations :**
*   **Isolation stricte :** Séparer physiquement le processus de lecture des e-mails (agent dédié sans accès aux outils de mémoire ou au shell) de l'agent principal.
*   **Traçabilité des données :** Implémenter un système de "provenance" pour chaque information stockée, permettant d'identifier son origine.
*   **Contrôle des écritures :** Exiger une validation explicite de l'utilisateur avant toute modification durable des fichiers de configuration ou de mémoire par l'IA.
*   **Audit :** Journaliser systématiquement chaque modification apportée à la mémoire persistante pour permettre une détection après-coup des anomalies.

---
[Source](https://thehackernews.com/2026/07/new-memghost-attack-plants-persistent.html){:target="_blank"}
