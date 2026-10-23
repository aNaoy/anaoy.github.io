---
title: 'Infostealer riding the AI Train'
date: 2026-10-23
permalink: /posts/2026/10/23/infostealer-riding-the-ai-train/
tags:
- veille-cyber
- zerodaysfans
---
### Aokigahara : Le nouveau malware ciblant les outils d'IA et de développement

**Points clés**
*   **Aokigahara** est un *infostealer* sophistiqué (potentiellement lié aux variantes Kamidere ou Stygian) conçu pour dérober des données sensibles.
*   Outre les cibles traditionnelles (navigateurs, portefeuilles crypto, messageries), il se distingue par sa capacité à collecter des fichiers d'authentification et de session liés aux outils d'IA (Claude, ChatGPT Desktop, GitHub Copilot, Cursor, Windsurf, Gemini CLI, etc.).
*   Le malware cible spécifiquement les environnements de développement (clés SSH, fichiers Git, accès AWS/Azure/GCP), exposant ainsi le code source et les infrastructures cloud.
*   Il intègre des mécanismes d'anti-analyse avancés (détection de VM, sandbox et débogueurs) et exclut les machines utilisant des langues issues de pays russophones ou ex-soviétiques.
*   La monétisation repose sur la vente d'accès aux services d'IA payants ou sur l'extorsion de données confidentielles (conversations, code propriétaire) traitées par ces outils.

**Vulnérabilités exploitées**
*   Le malware ne repose pas sur une CVE spécifique, mais exploite la **gestion locale des jetons de session (session tokens)** et des fichiers de configuration non chiffrés stockés par les applications de bureau, les IDE et les CLI de cloud/IA.

**Recommandations**
*   **Gestion des accès :** Ne jamais stocker de jetons d'accès ou de clés API persistantes de manière non protégée sur les postes de travail. Utiliser des coffres-forts de secrets ou des solutions de gestion d'identité (IAM) avec authentification MFA stricte.
*   **Surveillance des terminaux :** Déployer des solutions EDR capables de détecter des comportements anormaux, comme l'accès récurrent aux dossiers `Local Storage`, `globalStorage` ou aux fichiers de configuration spécifiques listés (ex: `.aws/credentials`, `storage.json` des IDE).
*   **Hygiène logicielle :** Restreindre l'accès en lecture aux répertoires contenant des jetons d'authentification et auditer régulièrement les permissions des outils de développement.
*   **Analyse réseau :** Bloquer les flux sortants vers les domaines C&C identifiés (ex: `dfwioeiofwr[.]info`, `kkeyyou[.]cc`) et surveiller les requêtes HTTP suspectes utilisant le User-Agent `Microsoft-CryptoAPI/10.0`.
*   **Détection :** Utiliser les règles YARA fournies pour identifier la présence de l'exécutable sur les machines du parc informatique.

---
[Source](https://research.checkpoint.com/2026/infostealer-riding-the-ai-train/){:target="_blank"}
