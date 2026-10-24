---
title: 'Leaked LiteLLM Master Key Let Attackers Steal GitHub Tokens and Hijack Release Pipeline'
date: 2026-10-24
permalink: /posts/2026/10/24/leaked-litellm-master-key-let-attackers-steal-github-tokens-and-hijack-release-pipeline/
tags:
- veille-cyber
- hackernews
---
### Attaque de la chaîne d'approvisionnement LiteLLM : Analyse de l'incident

L'entreprise LiteLLM a été victime d'une attaque sophistiquée sur sa chaîne d'approvisionnement logicielle, ayant conduit à la publication d'une version malveillante de son package Python (v1.107.0). L'incident trouve son origine dans la compromission d'une clé maîtresse de plateforme d'agents, initialement exposée par erreur dans un dépôt public en mai 2026. Malgré une tentative de révocation, la persistance de cette clé a permis à un attaquant d'accéder aux jetons GitHub de l'organisation.

**Points clés :**
* **Vecteur initial :** Fuite d'une clé maîtresse dans un fichier de configuration sur GitHub.
* **Escalade :** L'attaquant a utilisé la clé pour dérober des jetons OAuth, contourner les protections de branches et infiltrer les pipelines de publication.
* **Technique d'évasion :** Utilisation de branches éphémères ("ci-tmp") pour injecter des workflows malveillants et supprimer toute trace historique.
* **Impact :** La version 1.107.0 du package contenait un logiciel malveillant capable de s'exécuter automatiquement au démarrage de Python, exfiltrant une vaste gamme de identifiants (SSH, tokens cloud, bases de données, outils de développement).

**Vulnérabilités exploitées :**
* **Exposition de secrets (Hardcoded secrets) :** Clé maîtresse laissée dans un dépôt public.
* **Gestion des privilèges :** Jetons GitHub non restreints (scope trop large) avec accès propriétaire.
* **Pipeline de CI/CD :** Assouplissement des règles de validation des releases, permettant une compromission via des comptes mainteneurs détournés.

**Recommandations :**
* **Gestion stricte des secrets :** Automatiser la révocation immédiate de toute clé exposée et utiliser des solutions de gestion de coffres-forts (Vault) avec rotation automatique.
* **Sécurisation des pipelines (CI/CD) :** Maintenir des politiques strictes de "Least Privilege" pour les jetons d'accès et exiger une approbation physique ou multi-facteurs pour toute modification du pipeline de production.
* **Hygiène du code :** Scanner les commits pour détecter les secrets avant la fusion (ex: GitGuardian) et auditer régulièrement les workflows GitHub pour détecter toute activité suspecte ou création de branches éphémères.
* **Remédiation post-compromission :** En cas d'exposition de jetons, procéder à une réinitialisation complète de toutes les clés d'API et identifiants associés aux systèmes internes et services tiers (AWS, Anthropic, OpenAI, etc.).

---
[Source](https://thehackernews.com/2026/10/leaked-litellm-master-key-let-attackers.html){:target="_blank"}
