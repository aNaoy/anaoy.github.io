---
title: 'Red Hat npm packages compromised to steal developer credentials'
date: 2026-06-02
permalink: /posts/2026/06/02/red-hat-npm-packages-compromised-to-steal-developer-credentials/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par chaîne d'approvisionnement sur les paquets npm de Red Hat

Plus de 30 paquets du namespace `@redhat-cloud-services` sur npm ont été compromis afin de distribuer "Miasma", une variante du logiciel malveillant de vol d'identifiants *Shai-Hulud*. L'attaque a permis l'exfiltration massive de secrets (AWS, Google Cloud, Azure, jetons CI/CD, clés SSH, etc.) auprès des développeurs ayant installé les versions corrompues.

**Points clés :**
*   **Vecteur d'attaque :** Compromission du compte GitHub d'un employé de Red Hat, permettant d'injecter des flux de travail (GitHub Actions) malveillants.
*   **Mécanisme :** Utilisation de jetons OIDC pour authentifier les publications automatiques sur npm et masquer le code malveillant dans les scripts `preinstall`.
*   **Impact :** 32 paquets et 96 versions touchés. Bien que Red Hat affirme que l'incident se limite à des outils de développement internes, plus de 300 dépôts GitHub ont été identifiés comme compromis par la campagne Miasma à ce jour.
*   **Vulnérabilités :** Pas de CVE spécifique attribuée, mais l'attaque repose sur l'abus des mécanismes de publication automatisée (Trusted Publishing) et des accès privilégiés aux dépôts de code source.

**Recommandations :**
*   **Rotation immédiate :** Les organisations ayant installé les paquets concernés doivent impérativement révoquer et renouveler l'ensemble des clés, jetons, mots de passe et fichiers `.env` présents sur les machines infectées.
*   **Sécurité des comptes :** Renforcer la protection des comptes liés aux dépôts (GitHub) via une authentification multifacteur (MFA) rigoureuse et surveiller les journaux d'audit des flux de travail CI/CD.
*   **Audit de dépendances :** Vérifier les versions des paquets utilisés et auditer les scripts d'installation (`preinstall`, `postinstall`) dans les projets.

---
[Source](https://www.bleepingcomputer.com/news/security/red-hat-npm-packages-compromised-to-steal-developer-credentials/){:target="_blank"}
