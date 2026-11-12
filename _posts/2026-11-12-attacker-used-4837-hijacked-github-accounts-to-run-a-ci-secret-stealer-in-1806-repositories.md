---
title: 'Attacker Used 4,837 Hijacked GitHub Accounts to Run a CI Secret Stealer in 1,806+ Repositories'
date: 2026-11-12
permalink: /posts/2026/11/12/attacker-used-4837-hijacked-github-accounts-to-run-a-ci-secret-stealer-in-1806-repositories/
tags:
- veille-cyber
- hackernews
---
### Vague massive : 4 800 comptes GitHub compromis pour le vol de secrets CI

Une campagne malveillante majeure a exploité des identifiants GitHub volés sur 4 837 comptes pour injecter des outils de vol de secrets dans plus de 1 800 dépôts. Les attaquants utilisent des pull requests trompeuses (titrées "docs: dependency audit notes") pour exécuter des scripts malveillants lors des workflows CI/CD, visant à exfiltrer des credentials cloud (AWS, Azure, GCP) et des clés d'accès.

**Points clés :**
*   **Mode opératoire :** Utilisation de comptes compromis pour soumettre des workflows malveillants ou des hooks `postinstall` dans `package.json`.
*   **Objectif :** Exfiltration massive de secrets (GitHub Actions, jetons OIDC, clés API) et maintien d'un accès persistant dans les environnements cloud via la modification de politiques IAM ou l'ajout d'identités fédérées (`wfx-ci-*`).
*   **Ampleur :** Plus de 60 000 dépôts ont reçu des tests de vulnérabilité. Le malware a été détecté dans des paquets npm, des modules Go et des dépôts WebdriverIO.
*   **Persistance :** Le malware est capable de survivre à la rotation des clés en créant des backdoors dans les fournisseurs de cloud (ex: politiques AWS modifiées).

**Indicateurs de compromission (IoC) :**
*   **Branches suspectes :** `wfx-docs`, `chore/[a-z0-9]{8}`, `ci-check-[0-9]{4}`.
*   **Messages de commit :** `ci: refresh build cache`, `chore: add ci helper`, `ci: restore`.
*   **Infrastructure réseau :** Trafic vers `194.150.166[.]244`, `18.143.168[.]96`, `153.75.82[.]159` ou via Telegram.

**Recommandations :**
*   **Audit immédiat :** Vérifier l'historique des commits à la recherche des branches et messages suspects listés ci-dessus.
*   **Nettoyage cloud :** Rechercher des identités fédérées non autorisées (ex: `wfx-ci-*` dans Entra ID) et des modifications suspectes de politiques IAM (AWS CloudTrail).
*   **Réinitialisation complète :** En cas de compromission, considérer comme volés tous les secrets accessibles par les workflows CI/CD, les clés SSH, les jetons OAuth et les sessions de machines ayant exécuté `npm install`.
*   **Sécurisation :** Activer l'authentification à deux facteurs (2FA) sur tous les comptes GitHub et restreindre les permissions des jetons CI/CD au strict nécessaire.

---
[Source](https://thehackernews.com/2026/11/4837-hijacked-github-accounts-ran-ci.html){:target="_blank"}
