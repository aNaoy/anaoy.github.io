---
title: 'Jade Sleet Linked to Indian IT Provider Breach With FLATROOF and ROOFDECK Backdoors'
date: 2026-09-21
permalink: /posts/2026/09/21/jade-sleet-linked-to-indian-it-provider-breach-with-flatroof-and-roofdeck-backdoors/
tags:
- veille-cyber
- hackernews
---
### Infiltration de prestataires IT par le groupe Jade Sleet via des backdoors macOS

Le groupe de cybermenace nord-coréen **Jade Sleet** (alias PUKCHONG, TraderTraitor) cible activement les développeurs dans les secteurs DevOps, financier et Web3. Les attaquants utilisent des campagnes d'ingénierie sociale basées sur de fausses offres d'emploi pour inciter les victimes à télécharger des projets de codage piégés.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de dépôts GitHub factices contenant des fichiers de verrouillage Terraform (`.terraform.lock.hcl`) malveillants. L'exécution de `terraform init` déclenche le téléchargement de modules contrôlés par l'attaquant.
*   **Cibles privilégiées :** Postes de travail de développeurs (macOS ARM/Apple Silicon), offrant un accès stratégique aux pipelines CI/CD, au code source et aux infrastructures cloud.
*   **Mode opératoire :** Utilisation de backdoors sophistiqués pour l'exfiltration de données, la reconnaissance système et le mouvement latéral. Les implants sont régulièrement mis à jour pour échapper à la détection (suppression des symboles et informations de débogage).

**Malwares identifiés :**
*   **FLATROOF (Gaslight) :** Backdoor utilisant Telegram pour le C2, capable de voler des données de navigateurs, des historiques de terminal, des trousseaux d'accès (`login.keychain-db`) et de gérer des fichiers.
*   **ROOFDECK :** Backdoor utilisant le protocole décentralisé Nostr pour le C2. Il permet un accès distant via un shell, la manipulation de fichiers et l'établissement de persistance via des *Launch Agents*.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur une exploitation de confiance au sein du flux de travail des développeurs (Supply Chain Attack) via des dépendances Terraform détournées.

**Recommandations :**
*   **Sécurisation des endpoints :** Renforcer la surveillance des postes de travail des développeurs, qui constituent le point d'entrée critique vers les actifs cloud.
*   **Audit des dépendances :** Vérifier systématiquement l'intégrité des fichiers de configuration et de verrouillage (ex: `terraform.lock.hcl`) avant toute exécution, en s'assurant qu'ils pointent vers des registres officiels et légitimes.
*   **Gestion des accès :** Appliquer le principe du moindre privilège sur les environnements de développement et limiter l'accès aux secrets/clés d'infrastructure depuis les machines locales.
*   **Veille :** Sensibiliser les équipes de développement aux méthodes d'ingénierie sociale, particulièrement lors de processus de recrutement informels impliquant l'exécution de code ou de projets tests.

---
[Source](https://thehackernews.com/2026/09/jade-sleet-linked-to-indian-it-provider.html){:target="_blank"}
