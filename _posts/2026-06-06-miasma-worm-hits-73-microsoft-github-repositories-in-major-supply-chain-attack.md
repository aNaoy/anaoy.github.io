---
title: 'Miasma Worm Hits 73 Microsoft GitHub Repositories in Major Supply Chain Attack'
date: 2026-06-06
permalink: /posts/2026/06/06/miasma-worm-hits-73-microsoft-github-repositories-in-major-supply-chain-attack/
tags:
- veille-cyber
- hackernews
---
### Attaque massive par chaîne d'approvisionnement : le ver Miasma infiltre Microsoft

Le ver informatique **Miasma**, une variante évolutive du malware *Mini Shai-Hulud*, a compromis 73 dépôts GitHub appartenant à Microsoft (notamment Azure et MicrosoftDocs). Cette attaque illustre une persistance des acteurs malveillants, qui ont réussi à réinfecter des projets comme `durabletask` après une première compromission le mois précédent.

**Points clés :**
* **Propagation virale :** Le malware se propage de manière exponentielle en exploitant les accès légitimes des mainteneurs compromis, rendant les activités malveillantes indistinguables de mises à jour standards.
* **Technique d'infection :** Contrairement aux attaques classiques par registre (npm/PyPI), le ver injecte désormais du code directement dans les dépôts source.
* **Vecteur d'exécution :** Le payload s'exécute automatiquement lorsqu'un développeur clone le dépôt et l'ouvre via des outils d'assistance au code (AI coding agents) tels que Claude Code, Gemini CLI, Cursor ou VS Code.
* **Cibles :** En plus de l'écosystème Azure, le ver a été détecté dans divers dépôts tiers (ex: `icflorescu/mantine-datatable`).

**Vulnérabilités :**
* Aucune faille logicielle spécifique (CVE) n'est exploitée ; l'attaque repose sur une faille de **confiance dans le modèle de chaîne d'approvisionnement**. La compromission des identifiants des mainteneurs permet au ver d'opérer via des canaux authentifiés.

**Recommandations :**
* **Rotation immédiate des secrets :** Toute clé d'API, jeton d'accès ou identifiant lié aux dépôts compromis doit être considéré comme compromis et immédiatement révoqué/renouvelé.
* **Audit des accès :** Vérifier rigoureusement les accès aux dépôts GitHub et renforcer l'authentification multifacteur (MFA) pour tous les contributeurs.
* **Vigilance sur les outils d'IA :** Inspecter le code source avant ouverture dans des environnements de développement automatisés ou des agents d'IA, car ces outils peuvent déclencher l'exécution automatique de scripts malveillants présents dans les fichiers de configuration du projet.
* **Surveillance des commits :** Mettre en place des mécanismes de revue stricte des commits (code review) pour détecter toute injection de "payload runner" ou comportement suspect dans les scripts de test (`npm test`).

---
[Source](https://thehackernews.com/2026/06/miasma-worm-hits-73-microsoft-github.html){:target="_blank"}
