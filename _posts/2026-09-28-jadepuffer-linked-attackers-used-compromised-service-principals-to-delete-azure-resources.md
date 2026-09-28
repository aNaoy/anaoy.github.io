---
title: 'JADEPUFFER-Linked Attackers Used Compromised Service Principals to Delete Azure Resources'
date: 2026-09-28
permalink: /posts/2026/09/28/jadepuffer-linked-attackers-used-compromised-service-principals-to-delete-azure-resources/
tags:
- veille-cyber
- hackernews
---
### Offensive d'IA et compromission de Service Principals dans Azure par JADEPUFFER

Le groupe de menace JADEPUFFER (suivi par Microsoft sous le nom **Storm-3168**) utilise des agents d'IA pour orchestrer des cyberattaques automatisées contre des infrastructures cloud. L'incident récent dans l'environnement Azure a démontré une exécution coordonnée visant à paralyser les capacités de récupération des victimes via la suppression massive de ressources.

**Points clés :**
*   **Mode opératoire :** Utilisation de deux comptes « Service Principal » compromis, l'un dédié à la reconnaissance et l'autre aux actions destructrices.
*   **Cibles :** Comptes de stockage Azure, bases de données SQL, Key Vaults, machines virtuelles et plans d'App Service.
*   **Automatisation :** L'attaque souligne une tendance croissante vers des opérations orchestrées par IA, capables d'enchaîner rapidement des techniques de post-compromission pour maximiser les dégâts.
*   **Origine de la compromission :** Les identifiants (Client ID/Secret) ont été exposés par erreur dans l'historique d'édition d'un ticket public sur GitHub.

**Vulnérabilités exploitées :**
*   **CVE-2025-3248 :** Faille dans Langflow utilisée initialement par JADEPUFFER pour l'intrusion initiale et le déploiement de rançongiciels (ENCFORGE).
*   **Exposition d'identifiants :** Fuite de secrets en texte clair dans des dépôts de code publics.

**Recommandations :**
*   **Protection des ressources :** Activer systématiquement les verrous de ressources Azure (*Azure resource locks*) et les protections contre la suppression au niveau des comptes de stockage, qui se sont avérés efficaces pour bloquer les actions malveillantes.
*   **Gestion des secrets :** Ne jamais stocker de secrets dans des dépôts de code (même temporairement). En cas d'exposition, révoquer immédiatement les clés et renouveler les secrets.
*   **Surveillance :** Mettre en place des outils de détection basés sur l'IA pour contrer la vitesse des attaques orchestrées par des agents autonomes.
*   **Principe du moindre privilège :** Restreindre strictement les permissions accordées aux Service Principals pour limiter l'impact d'une éventuelle compromission.

---
[Source](https://thehackernews.com/2026/09/jadepuffer-linked-attackers-used.html){:target="_blank"}
