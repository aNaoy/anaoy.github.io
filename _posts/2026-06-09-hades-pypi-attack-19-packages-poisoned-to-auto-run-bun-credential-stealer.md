---
title: 'Hades PyPI Attack: 19 Packages Poisoned to Auto-Run Bun Credential Stealer'
date: 2026-06-09
permalink: /posts/2026/06/09/hades-pypi-attack-19-packages-poisoned-to-auto-run-bun-credential-stealer/
tags:
- veille-cyber
- hackernews
---
### Campagne Hades : Propagation de malwares sur PyPI via le runtime Bun

La campagne « Hades » constitue une nouvelle vague d'attaques sur la chaîne d'approvisionnement logicielle, ciblant le dépôt Python Package Index (PyPI) pour dérober des identifiants sensibles. Ce malware s'inscrit dans la lignée des campagnes « Shai-Hulud » et « Miasma ».

**Points clés :**
*   **Propagation :** 19 paquets PyPI (incluant des outils de bio-informatique) ont été compromis. Ils utilisent des fichiers `*-setup.pth` ou des hooks dans `__init__.py` pour s'exécuter automatiquement dès l'installation, sans intervention de l'utilisateur.
*   **Fonctionnement :** Le malware télécharge le runtime JavaScript **Bun** pour exécuter un script obfuscé (`_index.js`) capable de collecter des secrets (AWS, GCP, GitHub, SSH, Vault, `.env`, etc.) sur les systèmes des développeurs.
*   **Évasion :** Utilisation d'injections de prompts pour tromper les scanners de sécurité basés sur l'IA et vérification de la locale système (évite les machines en Russie).
*   **Capacités avancées :** Le malware peut persister, se propager latéralement via SSH, lire la mémoire des processus CI/CD pour extraire des tokens, et possède une fonction de « nettoyage » (wiper) en cas de révocation des accès.

**Vulnérabilités :**
*   Absence de CVE spécifique, car il s'agit d'un abus de fonctionnalités légitimes de Python (« site-packages » et « install hooks ») plutôt que d'une faille logicielle classique. La vulnérabilité réside dans le modèle de confiance des gestionnaires de paquets qui autorisent l'exécution de code lors de l'installation.

**Recommandations :**
*   **Vigilance accrue :** Soyez prudent lors de l'installation de bibliothèques tierces, surtout si elles sont peu connues ou récemment mises à jour.
*   **Analyse statique et linting :** L'utilisation de linters (ex: `ruff`) et d'outils de formatage de code peut bloquer l'insertion de code malveillant qui ne respecte pas les standards du projet.
*   **Zero Trust :** Ne considérez jamais un paquet signé comme intrinsèquement sûr. Limitez les permissions des jetons CI/CD et surveillez les accès aux secrets dans les environnements de build.
*   **Segmentation :** Isolez les environnements de développement et de CI/CD afin de limiter la portée d'une compromission éventuelle.

---
[Source](https://thehackernews.com/2026/06/hades-pypi-attack-19-packages-poisoned.html){:target="_blank"}
