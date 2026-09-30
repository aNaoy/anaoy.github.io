---
title: 'Microsoft is rolling out Linux container support to WSL'
date: 2026-09-30
permalink: /posts/2026/09/30/microsoft-is-rolling-out-linux-container-support-to-wsl/
tags:
- veille-cyber
- bleepingcomp
---
### Déploiement général des conteneurs Linux sur WSL

Microsoft a officialisé la disponibilité générale des conteneurs au sein du Sous-système Windows pour Linux (WSL). Cette mise à jour permet d'exécuter, de gérer et de déployer nativement des conteneurs Linux sur Windows via l'outil en ligne de commande `wslc.exe` (ou son alias `container.exe`) et une API dédiée pour les applications Windows.

**Points clés :**
* **Fonctionnalités étendues :** La version finale inclut la gestion du cycle de vie des conteneurs (redémarrage, santé), la copie de fichiers, les événements en temps réel et la configuration du stockage.
* **Intégration écosystémique :** Support intégré dans VS Code, avec une compatibilité future prévue pour `wsl compose up` afin d'utiliser les fichiers `compose.yaml` existants.
* **Performance :** Optimisation de l'accès aux fichiers Windows depuis l'environnement Linux, avec une accélération annoncée jusqu'à 2x.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée dans l'article. Toutefois, l'utilisation de conteneurs Linux sur un hôte Windows élargit la surface d'attaque, nécessitant une surveillance accrue des processus et des interactions réseau.

**Recommandations de sécurité :**
* **Visibilité accrue :** Utiliser l'intégration avec **Microsoft Defender for Endpoint** pour monitorer les activités (fichiers, réseaux, processus) à l'intérieur des conteneurs et les corréler avec l'hôte Windows.
* **Contrôle via Intune :** Appliquer des politiques via Microsoft Intune pour désactiver WSL si nécessaire ou restreindre l'exécution aux seules images provenant de **registres approuvés** (via des listes d'autorisation).
* **Gestion des privilèges :** S'assurer que les administrateurs limitent l'accès aux registres de conteneurs pour garantir la conformité aux exigences de sécurité organisationnelles.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-is-rolling-out-linux-container-support-to-wsl/){:target="_blank"}
