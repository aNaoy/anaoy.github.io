---
title: 'Cline CLI 2.3.0 Supply Chain Attack Installed OpenClaw on Developer Systems'
date: 2026-02-20
permalink: /posts/2026/02/20/cline-cli-230-supply-chain-attack-installed-openclaw-on-developer-systems/
tags:
- veille-cyber
- hackernews
---
**Compromission de Cline CLI : une Attaque par Chaîne d'Approvisionnement Installe OpenClaw**

Une faille de sécurité a affecté le package npm de l'assistant de codage open-source Cline CLI. La version 2.3.0, publiée le 17 février 2026, a été compromise via un token de publication npm volé. Cette mise à jour malveillante a installé en silence OpenClaw, un agent IA autonome, sur les systèmes des développeurs. Bien qu'OpenClaw ne soit pas intrinsèquement malveillant et que l'incident n'ait pas entraîné d'autres comportements nocifs, cette installation n'était ni autorisée ni intentionnelle.

L'attaque a touché les utilisateurs ayant installé Cline CLI version 2.3.0 durant une période de huit heures le 17 février 2026. Les extensions VS Code et les plugins JetBrains de Cline ne sont pas affectés.

La vulnérabilité sous-jacente, baptisée "Clinejection", permettait à des attaquants de voler les tokens d'authentification du dépôt via des injections de prompt exploitant une mauvaise configuration dans le processus d'analyse automatisée des tickets GitHub. Cette faille, introduite le 21 décembre 2025, a permis de manipuler l'IA pour exécuter des commandes arbitraires et de compromettre les publications de production grâce à l'empoisonnement du cache GitHub Actions.

Les développeurs de Cline ont résolu le problème en publiant la version 2.4.0, en dépréciant la version 2.3.0 et en révoquant le token compromis. Le mécanisme de publication npm a également été mis à jour pour supporter OIDC via GitHub Actions.

**Points Clés :**

*   **Type d'attaque :** Attaque par chaîne d'approvisionnement logicielle.
*   **Composant affecté :** Package npm de Cline CLI, version 2.3.0.
*   **Charge utile :** Installation silencieuse de l'agent IA OpenClaw.
*   **Période d'impact :** Environ huit heures le 17 février 2026 (3:26 AM PT à 11:30 AM PT).
*   **Mécanisme de compromission :** Token de publication npm volé, exploitant la vulnérabilité "Clinejection".

**Vulnérabilités :**

*   **Exploitation de token npm :** Un token de publication npm compromis a été utilisé pour pousser une version malveillante.
*   **Clinejection :** Une mauvaise configuration du workflow d'analyse des tickets GitHub, combinée à une injection de prompt, a permis l'exécution de commandes arbitraires.
*   **Empoisonnement du cache GitHub Actions :** Permet de passer d'un workflow de triage à des workflows privilégiés pour voler des identifiants de publication.

**Recommandations :**

*   Mettre à jour Cline CLI vers la dernière version (2.4.0 ou supérieure).
*   Vérifier les systèmes pour toute installation inattendue d'OpenClaw et le supprimer si non nécessaire.
*   Les mainteneurs de packages doivent renforcer la sécurité de leurs processus de publication, notamment en privilégiant des mécanismes de publication de confiance et en désactivant les tokens traditionnels.
*   Les utilisateurs de packages doivent être attentifs aux attestations de sécurité et aux changements soudains dans les dépendances.
*   Il est crucial de considérer les agents IA comme des acteurs privilégiés nécessitant une gouvernance appropriée dans le contexte de la sécurité de la chaîne d'approvisionnement.

---
[Source](https://thehackernews.com/2026/02/cline-cli-230-supply-chain-attack.html){:target="_blank"}
