---
title: 'New Check Point flaw lets hackers execute code with root privileges'
date: 2026-09-18
permalink: /posts/2026/09/18/new-check-point-flaw-lets-hackers-execute-code-with-root-privileges/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique d'exécution de code sur les systèmes Check Point

Check Point a publié des correctifs pour une faille critique affectant ses serveurs de gestion et de journaux, permettant à des attaquants non authentifiés d'exécuter du code arbitraire avec des privilèges "root".

**Points clés :**
*   **Cible :** *Security Management Server* et *Log Server* de Check Point.
*   **Nature de l'attaque :** Attaque peu complexe, sans interaction utilisateur requise.
*   **Indicateur de compromission :** La présence de messages d'erreur « Administrator failed to log in: Username too long » dans les logs d'audit.
*   **Contexte :** Cette vulnérabilité s'ajoute à une série de failles critiques découvertes récemment sur les infrastructures Check Point (dont CVE-2026-85102 et CVE-2026-85103), poussant les autorités de cybersécurité à recommander une mise à jour immédiate.

**Vulnérabilité identifiée :**
*   **CVE-2026-91843 :** Débordement de tampon basé sur la pile (*stack-based buffer overflow*) lors du processus de connexion.

**Recommandations :**
*   **Application des correctifs :** Déployer le *LivePatch* fourni par l'éditeur dès que possible.
*   **Atténuation temporaire :** En cas d'impossibilité de mise à jour, renforcer la sécurité du système et restreindre l'accès à la console d'administration (*SmartConsole*) aux seules adresses IP et sous-réseaux approuvés via la configuration des « Trusted Clients ».

---
[Source](https://www.bleepingcomputer.com/news/security/check-point-warns-critical-flaw-lets-hackers-execute-code-as-root/){:target="_blank"}
