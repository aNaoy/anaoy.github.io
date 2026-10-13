---
title: 'When LLM Gateways Go Wrong: Findings from LiteLLM'
date: 2026-10-13
permalink: /posts/2026/10/13/when-llm-gateways-go-wrong-findings-from-litellm/
tags:
- veille-cyber
- zerodaysfans
---
### Analyse de sécurité : Vulnérabilités critiques dans LiteLLM

Des chercheurs ont découvert plusieurs failles critiques dans la passerelle (gateway) LLM open-source **LiteLLM** (corrigées dans la version 1.83.9). Ces vulnérabilités permettent à un attaquant authentifié de prendre le contrôle total du système, d'exfiltrer des données ou d'exécuter du code arbitraire.

#### Points clés
*   **Défaut de contrôle d'accès :** L'absence de vérification des rôles (RBAC) sur l'endpoint `/config/update` permet à tout utilisateur authentifié (même à faibles privilèges) de modifier la configuration système.
*   **Injection d'environnement :** La capacité de modifier les variables d'environnement permet de détourner des fonctionnalités critiques comme `UI_LOGO_PATH` (lecture arbitraire de fichiers) ou les identifiants administrateurs.
*   **Exécution de code (RCE) :** Le chargement dynamique de modules Python distants (via S3/GCS) dans les points de terminaison "pass-through" peut être exploité pour exécuter du code arbitraire sur le serveur.
*   **SSRF (Server-Side Request Forgery) :** L'usage du paramètre `user_config` contourne les restrictions, permettant de rediriger les requêtes vers des serveurs malveillants et de voler des clés API de fournisseurs.

#### Vulnérabilités identifiées
*   **CVE-2026-35029 :** Défaut d'autorisation sur l'endpoint `/config/update`.
*   **CVE-2026-59823 :** SSRF via le paramètre `user_config`.
*   **GHSA-69x8-hrgq-fjj8 :** Exposition de hashs de mots de passe et stockage non sécurisé (absence de salage et algorithmes faibles).

#### Recommandations
*   **Mise à jour immédiate :** Passer à la version **1.83.9** ou supérieure pour corriger ces failles.
*   **Gestion des accès :** Appliquer strictement le principe du moindre privilège pour les utilisateurs accédant à la passerelle LiteLLM.
*   **Audit de configuration :** Vérifier les configurations "pass-through" existantes pour s'assurer qu'aucun module externe non autorisé n'est chargé.
*   **Renforcement :** Désactiver les fonctionnalités inutilisées (ex: `user_config` ou points de terminaison de configuration dynamique) si elles ne sont pas requises pour le fonctionnement métier.
*   **Pratiques fondamentales :** Intégrer des revues de sécurité sur les contrôles d'accès et la validation des entrées pour tout nouvel outil d'infrastructure IA.

---
[Source](https://research.checkpoint.com/2026/when-llm-gateways-go-wrong-findings-from-litellm/){:target="_blank"}
