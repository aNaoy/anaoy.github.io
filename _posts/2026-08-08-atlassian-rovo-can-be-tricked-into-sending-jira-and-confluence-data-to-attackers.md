---
title: 'Atlassian Rovo Can Be Tricked Into Sending Jira and Confluence Data to Attackers'
date: 2026-08-08
permalink: /posts/2026/08/08/atlassian-rovo-can-be-tricked-into-sending-jira-and-confluence-data-to-attackers/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités d'exfiltration de données dans l'assistant Atlassian Rovo

L'assistant IA Atlassian Rovo présentait deux vecteurs d'attaque distincts permettant d'exfiltrer des données confidentielles depuis Jira et Confluence vers des serveurs contrôlés par des attaquants. Ces failles exploitent la capacité de l'IA à manipuler des URL sans validation rigoureuse, permettant de transférer des informations auxquelles l'utilisateur authentifié a accès.

**Points clés :**
*   **RovoBlast (corrigé) :** Une faille utilisant le paramètre d'URL `rovoChatPrompt` pour injecter des instructions malveillantes via un simple clic d'un utilisateur authentifié.
*   **Injection par contenu (statut incertain) :** Une technique d'injection indirecte où des instructions malveillantes sont dissimulées dans des documents chargés par l'utilisateur. Rovo traite ces instructions pour collecter et envoyer des données Jira/Confluence vers une URL externe sans approbation préalable.
*   **Impact :** L'exfiltration est limitée aux données accessibles par l'utilisateur ciblé. Aucune preuve d'exploitation réelle n'a été constatée à ce jour.
*   **CVE :** Aucune identification CVE n'est associée à ces vulnérabilités.

**Vulnérabilités identifiées :**
*   **RovoBlast :** Correction déployée par Atlassian le 8 juillet 2026 (via Bugcrowd).
*   **Injection indirecte via fichiers :** Rapportée par PromptArmor ; le correctif de cette méthode n'est pas confirmé par les chercheurs.

**Recommandations :**
*   **Gestion des accès :** Examiner et restreindre les autorisations accordées aux applications et groupes utilisant Rovo.
*   **Contrôle granulaire :** Utiliser les paramètres d'administration pour désactiver les fonctionnalités Rovo sur les applications ou périmètres jugés sensibles.
*   **Limites de configuration :** Ne pas considérer le bouton « recherche web » comme une frontière de sécurité suffisante, car les vecteurs d'exfiltration peuvent fonctionner indépendamment de cette option.
*   **Surveillance des permissions :** S'assurer que le principe du moindre privilège est appliqué aux accès Jira et Confluence, car l'assistant Rovo hérite des droits de l'utilisateur connecté.

---
[Source](https://thehackernews.com/2026/08/atlassian-rovo-can-be-tricked-into.html){:target="_blank"}
