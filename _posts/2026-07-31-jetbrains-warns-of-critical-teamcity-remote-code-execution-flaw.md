---
title: 'JetBrains warns of critical TeamCity remote code execution flaw'
date: 2026-07-31
permalink: /posts/2026/07/31/jetbrains-warns-of-critical-teamcity-remote-code-execution-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique de RCE sur JetBrains TeamCity

JetBrains a émis une alerte concernant une vulnérabilité critique affectant l'ensemble des versions On-Premises de son serveur CI/CD TeamCity. Cette faille permet à un attaquant ayant un accès HTTPS au serveur de contourner l'authentification et d'exécuter des commandes arbitraires avec les privilèges du processus serveur.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-63077.
*   **Impact :** Exécution de code à distance (RCE), compromission potentielle des pipelines CI/CD, des identifiants stockés et des artefacts de build.
*   **Portée :** Toutes les installations TeamCity On-Premises. Les clients utilisant TeamCity Cloud ne sont pas affectés, car les correctifs ont déjà été appliqués.
*   **État de la menace :** Aucune exploitation active n'a été constatée à ce jour, bien que les failles sur TeamCity soient historiquement prisées par les groupes de ransomwares et les acteurs étatiques.

**Recommandations :**
*   **Mise à jour immédiate :** Passer aux versions 2025.11.7 ou 2026.1.3.
*   **Utilisation du patch :** Pour les versions antérieures (dès 2017.1), installer le plugin de correctif de sécurité fourni par JetBrains. 
*   **Mesures de sécurité additionnelles :** Restreindre l'accès aux serveurs exposés sur Internet via un VPN ou des couches de protection réseau supplémentaires.
*   **Maintenance :** Pour les versions 2017.1 à 2018.1, un redémarrage du serveur est nécessaire après l'application du patch.

---
[Source](https://www.bleepingcomputer.com/news/security/jetbrains-warns-of-critical-teamcity-remote-code-execution-flaw/){:target="_blank"}
