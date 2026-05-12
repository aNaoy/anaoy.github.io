---
title: 'Shai Hulud attack ships signed malicious TanStack, Mistral npm packages'
date: 2026-05-12
permalink: /posts/2026/05/12/shai-hulud-attack-ships-signed-malicious-tanstack-mistral-npm-packages/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission massive de la chaîne d'approvisionnement logicielle : la campagne Shai-Hulud

La campagne « Shai-Hulud », attribuée au groupe TeamPCP, a compromis des centaines de paquets sur npm et PyPI, notamment dans les écosystèmes TanStack, Mistral AI et Guardrails AI. Les attaquants parviennent à publier des versions malveillantes signées numériquement, bénéficiant d'une attestation de provenance valide (SLSA niveau 3), ce qui les rend impossibles à distinguer des versions légitimes pour les développeurs.

**Points clés :**
*   **Propagation :** Le malware utilise les identifiants volés lors d'une infection pour compromettre les comptes des mainteneurs et republier automatiquement des versions infectées de leurs paquets.
*   **Technique :** Utilisation de commits « orphelins » cachés dans le stockage objet de GitHub, référencés via des dépendances optionnelles malveillantes.
*   **Persistance :** Le malware s'installe dans les hooks Claude Code et les tâches VS Code, survivant ainsi à la désinstallation du paquet initial.
*   **Exfiltration :** Les données (clés AWS, jetons Kubernetes, SSH, secrets .env, etc.) sont exfiltrées via le réseau P2P « Session » pour contourner les blocages.
*   **Sabotage :** Présence d'un mécanisme de destruction (wipe) ciblant les environnements en Israël et en Iran.

**Vulnérabilités exploitées :**
*   Utilisation risquée du workflow `pull_request-target`.
*   Empoisonnement du cache des GitHub Actions.
*   Vol de jetons OIDC (OpenID Connect) dans la mémoire des runners.
*(Note : Bien que l'article décrive l'enchaînement de ces failles, aucun identifiant CVE spécifique n'est associé à cette attaque, car il s'agit d'une exploitation de logique CI/CD et non d'une faille logicielle unique).*

**Recommandations :**
*   **Rotation immédiate :** Révoquer et renouveler tous les secrets potentiellement exposés (tokens GitHub/npm, clés AWS, certificats, clés SSH).
*   **Audit machine :** Vérifier la présence de fichiers suspects (ex: `router_runtime.js`, `setup.mjs`) dans les répertoires IDE et systèmes.
*   **Sécurisation CI/CD :** Bannir `pull_request-target` pour les workflows sensibles et limiter les permissions des jetons OIDC.
*   **Filtrage réseau :** Bloquer les domaines liés à l'infrastructure C2 (`api.masscan.cloud`, `git-tanstack.com`, `*.getsession.org`).
*   **Approche défensive :** Privilégier les installations via des fichiers de verrouillage (lockfiles) pour éviter les mises à jour silencieuses et renforcer l'analyse comportementale lors de l'installation des dépendances.

---
[Source](https://www.bleepingcomputer.com/news/security/shai-hulud-attack-ships-signed-malicious-tanstack-mistral-npm-packages/){:target="_blank"}
