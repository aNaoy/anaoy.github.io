---
title: 'GlassWorm Supply-Chain Attack Abuses 72 Open VSX Extensions to Target Developers'
date: 2026-03-14
permalink: /posts/2026/03/14/glassworm-supply-chain-attack-abuses-72-open-vsx-extensions-to-target-developers/
tags:
- veille-cyber
- hackernews
---
### Escalade de la campagne GlassWorm : Abus des chaînes d'approvisionnement VS Code

La campagne malveillante **GlassWorm** a évolué vers une stratégie d'infection par propagation transitive. En exploitant les mécanismes `extensionPack` et `extensionDependencies` du registre Open VSX, les attaquants transforment des extensions initialement légitimes en vecteurs de distribution de malwares via des mises à jour ultérieures, contournant ainsi les processus de validation initiale.

**Points clés :**
*   **Expansion :** 72 nouvelles extensions malveillantes identifiées dans Open VSX, imitant des outils de développement populaires.
*   **Techniques de dissimulation :** Utilisation de caractères Unicode invisibles pour injecter du code malveillant dans des dépôts GitHub et des paquets npm, souvent générés par IA pour paraître crédibles.
*   **Persistance :** Utilisation de transactions Solana comme système de résolution (dead drop) pour récupérer les adresses de serveurs C2 (Command & Control).
*   **Ciblage :** Vol d'identifiants, de jetons CI/CD, de secrets et de portefeuilles de cryptomonnaies. Le malware évite délibérément les systèmes configurés avec une locale russe.

**Vulnérabilités :**
*   **Dépendances transitives :** L'architecture de VS Code installe automatiquement toutes les dépendances déclarées, permettant à une extension mise à jour de télécharger des composants malveillants sans interaction directe de l'utilisateur.
*   **Remote Dynamic Dependencies (RDD) :** L'utilisation d'URL personnalisées dans les fichiers `package.json` permet aux attaquants de modifier le code à la volée sur leurs serveurs distants, rendant les inspections statiques inefficaces.

**Recommandations :**
*   **Audit des dépendances :** Examiner systématiquement le fichier `package.json` des extensions pour repérer des dépendances suspectes ou des URL pointant vers des domaines externes non officiels.
*   **Vigilance sur les mises à jour :** Se méfier des mises à jour automatiques d'extensions, particulièrement si elles commencent soudainement à exiger de nouvelles permissions ou dépendances.
*   **Sécurisation CI/CD :** Ne pas stocker de secrets ou de jetons sensibles sur des machines de développement utilisées pour tester des extensions tierces non vérifiées.
*   **Veille sur les dépôts :** Surveiller les commits suspects sur les dépôts de code source, notamment les modifications mineures (documentation, typographie) qui pourraient masquer des injections de caractères Unicode.

---
[Source](https://thehackernews.com/2026/03/glassworm-supply-chain-attack-abuses-72.html){:target="_blank"}
