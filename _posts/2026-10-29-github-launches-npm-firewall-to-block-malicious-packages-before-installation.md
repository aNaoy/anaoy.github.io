---
title: 'GitHub Launches npm Firewall to Block Malicious Packages Before Installation'
date: 2026-10-29
permalink: /posts/2026/10/29/github-launches-npm-firewall-to-block-malicious-packages-before-installation/
tags:
- veille-cyber
- hackernews
---
### Sécurisation de la Supply Chain : GitHub déploie un pare-feu pour paquets npm

GitHub a lancé en préversion publique un pare-feu pour paquets (Package Firewall) destiné aux clients GitHub Enterprise Cloud. Ce dispositif s'interpose entre les environnements de développement (agents IA, serveurs CI/CD) et les registres publics pour bloquer automatiquement l'installation de dépendances malveillantes.

**Points clés :**
*   **Filtrage à l'installation :** Le pare-feu inspecte les requêtes de métadonnées et les téléchargements en temps réel, agissant comme une barrière de conformité.
*   **Protection automatisée :** Conçu pour sécuriser les systèmes où les dépendances sont installées sans intervention humaine, limitant ainsi l'impact des attaques par injection.
*   **Tendance écosystémique :** Cette initiative s'inscrit dans une tendance globale (Rust, npm, PyPI) visant à imposer des périodes de latence ("cooldown periods") pour limiter la propagation rapide des paquets compromis.

**Politiques de blocage configurables :**
*   **Malwares connus :** Vérification basée sur la base de données d'avis de sécurité GitHub.
*   **Vulnérabilités :** Blocage selon la sévérité des failles détectées (par défaut : critique).
*   **Intégrité des attestations :** Blocage des versions sans attestation SLSA.
*   **Scripts suspects :** Détection de l'ajout récent de scripts (`preinstall` ou `postinstall`) pouvant compromettre les données.
*   **Période de latence (Cooldown) :** Blocage des paquets trop récents (personnalisable de 1 à 365 jours, défaut à 1 jour).

**Vulnérabilités :**
Bien que l'article ne mentionne pas de CVE spécifiques, il souligne les risques liés aux **attaques par dépendances empoisonnées** et au détournement de comptes de mainteneurs. Le pare-feu vise à mitiger ces risques en neutralisant l'exploitation automatique des vulnérabilités connues (non patchées) et des nouveaux paquets malveillants avant leur exécution.

**Recommandations :**
*   **Configurer le pare-feu :** Les administrateurs doivent définir des politiques strictes de sécurité adaptées à leurs besoins spécifiques.
*   **Utiliser le mécanisme d'exception :** En cas de blocage légitime, instaurer un processus de revue pour permettre l'installation de correctifs urgents via une demande d'exception.
*   **Adopter les délais de publication :** Pour les écosystèmes hors npm, appliquer manuellement ou via les outils de gestion de paquets (ex: `cargo/config.toml`) des périodes de latence pour permettre aux chercheurs en sécurité de détecter les menaces avant qu'elles ne soient massivement adoptées.

---
[Source](https://thehackernews.com/2026/10/github-launches-npm-firewall-to-block.html){:target="_blank"}
