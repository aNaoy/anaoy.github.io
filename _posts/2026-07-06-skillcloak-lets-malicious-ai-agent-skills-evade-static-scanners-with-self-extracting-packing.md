---
title: 'SkillCloak Lets Malicious AI Agent Skills Evade Static Scanners with Self-Extracting Packing'
date: 2026-07-06
permalink: /posts/2026/07/06/skillcloak-lets-malicious-ai-agent-skills-evade-static-scanners-with-self-extracting-packing/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité des agents IA : Le danger des « compétences » malveillantes

Les outils de scan statiques utilisés pour valider les extensions (« skills ») des agents IA (Claude Code, OpenAI Codex, etc.) sont largement inefficaces face à des techniques d'évasion simples. L'étude "Cloak and Detonate" démontre que ces protections peuvent être contournées massivement, exposant les utilisateurs au vol de données, à l'injection de backdoors et à l'exécution de code malveillant.

#### Points clés
*   **Techniques d'évasion (SkillCloak) :**
    *   **Obfuscation légère :** Altération des signatures détectées par les scanners (substitution de caractères, découpage de commandes).
    *   **Auto-extraction (Packing) :** Dissimulation de la charge utile dans des répertoires ignorés par les scanners (ex: `.git/`), reconstruite dynamiquement à l'exécution.
    *   **Padding :** Ajout de fichiers volumineux ("junk data") pour dépasser les limites de taille des scanners et éviter l'analyse.
*   **Faille fondamentale :** Les scanners analysent l'apparence du code avant exécution, alors que les comportements malveillants ne se manifestent qu'au moment de l'exécution, souvent après le passage du filtre de sécurité.
*   **Efficacité :** Le packing permet de contourner plus de 90 % des scanners testés, là où la détection statique échoue systématiquement.

#### Vulnérabilités identifiées
*   Il n'existe pas de CVE spécifique, car il s'agit d'une vulnérabilité conceptuelle inhérente à l'architecture des places de marché d'agents IA et à la confiance excessive accordée aux scanners statiques.

#### Recommandations
*   **Privilégier l'analyse comportementale (SkillDetonate) :** Déplacer la vérification vers l'environnement d'exécution (sandbox) en surveillant les accès fichiers, les flux de données et les appels système en temps réel plutôt que le code source statique.
*   **Renforcement opérationnel :**
    *   Hashing : Vérifier l'intégrité du skill lors de l'installation et ré-analyser avant chaque exécution pour détecter les charges utiles décompressées tardivement.
    *   Principe du moindre privilège : Restreindre les accès des agents IA à leurs terminaux et systèmes de fichiers.
    *   Hygiène : Éviter d'exécuter des agents IA sur des machines contenant des secrets sensibles (clés API, mots de passe).
*   **Surveillance :** Être vigilant face à des fichiers anormalement volumineux ou des répertoires cachés (ex: `.git/`, `build/`) contenant du code opaque ou compressé.

---
[Source](https://thehackernews.com/2026/07/new-skillcloak-technique-lets-malicious.html){:target="_blank"}
