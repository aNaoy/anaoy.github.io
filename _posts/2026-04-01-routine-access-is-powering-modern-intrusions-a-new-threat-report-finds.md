---
title: 'Routine Access Is Powering Modern Intrusions, a New Threat Report Finds'
date: 2026-04-01
permalink: /posts/2026/04/01/routine-access-is-powering-modern-intrusions-a-new-threat-report-finds/
tags:
- veille-cyber
- bleepingcomp
---
### La montée en puissance des intrusions par accès légitimes

Le rapport annuel 2026 de Blackpoint Cyber souligne un changement majeur dans le paysage des menaces : les attaquants privilégient désormais l'utilisation d'outils légitimes et d'identifiants valides plutôt que l'exploitation de vulnérabilités logicielles.

**Points clés :**
*   **Abus des VPN SSL :** Représentent 32,8 % des incidents identifiés, souvent via des identifiants compromis permettant une connexion jugée légitime par les systèmes de sécurité.
*   **Détournement d'outils RMM (Remote Monitoring and Management) :** Utilisés dans 30,3 % des cas, avec une prédominance de *ScreenConnect* (plus de 70 % de ces cas). Ces outils facilitent la persistance sans alerter les défenses.
*   **Ingénierie sociale :** Les campagnes de type "Fake CAPTCHA" ou "ClickFix" constituent 57,5 % des incidents. Elles poussent les utilisateurs à exécuter des commandes via les outils natifs de Windows, contournant ainsi les logiciels malveillants classiques.
*   **Contournement de la MFA :** En utilisant le vol de jetons de session (Adversary-in-the-Middle), les attaquants accèdent aux environnements Cloud même lorsque l'authentification multifacteur est activée.
*   **Nouvelle menace :** Identification de l'implant *Roadk1ll*, conçu pour se déplacer latéralement en utilisant des communications basées sur WebSocket.

**Vulnérabilités :**
L'article ne mentionne aucune CVE spécifique. La vulnérabilité réside ici dans le **processus** (utilisation abusive d'outils légitimes) et dans la **faillibilité humaine** (ingénierie sociale) plutôt que dans des failles logicielles exploitables.

**Recommandations :**
*   **Gestion des accès distants :** Considérer tout accès distant comme une activité à haut risque et haut impact.
*   **Audit des outils RMM :** Maintenir un inventaire strict des outils d'administration autorisés et supprimer les agents obsolètes ou non utilisés.
*   **Contrôle des exécutions :** Restreindre l'installation de logiciels non approuvés et limiter l'exécution de programmes depuis les répertoires inscriptibles par l'utilisateur.
*   **Sécurité Cloud :** Implémenter des contrôles d'accès conditionnels évaluant la posture de l'appareil, la géolocalisation et le risque lié à la session pour contrer le vol de jetons.

---
[Source](https://www.bleepingcomputer.com/news/security/routine-access-is-powering-modern-intrusions-a-new-threat-report-finds/){:target="_blank"}
