---
title: 'Four OpenClaw Flaws Enable Data Theft, Privilege Escalation, and Persistence'
date: 2026-05-15
permalink: /posts/2026/05/15/four-openclaw-flaws-enable-data-theft-privilege-escalation-and-persistence/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans OpenClaw : La menace "Claw Chain"

Des chercheurs en cybersécurité ont identifié quatre vulnérabilités critiques dans OpenClaw, baptisées collectivement « Claw Chain ». Enchaînées, ces failles permettent à un attaquant de s'extraire de l'environnement sandbox, d'accéder à des données sensibles, d'élever ses privilèges et d'assurer une persistance sur le système hôte.

**Points clés :**
*   **Mécanisme d'attaque :** L'exploitation commence par une exécution de code dans le bac à sable (sandbox) OpenShell via un plugin malveillant ou une injection de prompt, suivi d'une escalade progressive vers un contrôle total.
*   **Dissimulation :** Les actions de l'attaquant imitent le comportement légitime de l'agent, ce qui rend la détection par les outils de sécurité traditionnels particulièrement complexe.

**Vulnérabilités identifiées :**
*   **CVE-2026-44112 (Score 9.6) :** Problème de type "Time-of-check/time-of-use" (TOCTOU) permettant l'écriture de fichiers hors du répertoire racine autorisé.
*   **CVE-2026-44113 (Score 7.7) :** Faille TOCTOU permettant la lecture illicite de fichiers en dehors de la sandbox.
*   **CVE-2026-44115 (Score 8.8) :** Contournement de validation via l'injection de jetons dans des documents de type "heredoc", permettant l'exécution de commandes non approuvées.
*   **CVE-2026-44118 (Score 7.8) :** Contrôle d'accès défaillant permettant à un client non autorisé d'usurper l'identité du propriétaire pour obtenir des privilèges administrateur.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer sans délai la version **2026.4.22** d'OpenClaw, qui corrige l'intégralité de ces failles.
*   **Correctif spécifique :** La correction pour la CVE-2026-44118 implique l'abandon de l'indicateur d'appartenance (`senderIsOwner`) au profit d'un système de jetons (bearer tokens) distincts pour les propriétaires et les non-propriétaires, garantissant une authentification sécurisée.

---
[Source](https://thehackernews.com/2026/05/four-openclaw-flaws-enable-data-theft.html){:target="_blank"}
