---
title: 'Microsoft: New Remote Desktop warnings may display incorrectly'
date: 2026-04-28
permalink: /posts/2026/04/28/microsoft-new-remote-desktop-warnings-may-display-incorrectly/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement des avertissements de sécurité RDP sous Windows

Microsoft a confirmé un bug d'affichage affectant les nouvelles alertes de sécurité liées aux fichiers de connexion Bureau à distance (.rdp), introduites lors des mises à jour cumulatives d'avril 2026.

**Points clés :**
*   **Problème technique :** Les fenêtres d'avertissement de sécurité s'affichent de manière incorrecte (texte chevauchant ou boutons masqués), rendant l'interaction impossible pour l'utilisateur.
*   **Cause identifiée :** Le bug survient principalement lors de l'utilisation de configurations multi-écrans avec des paramètres de mise à l'échelle (DPI) différents.
*   **Contexte :** Ces mesures de sécurité visent à contrer l'utilisation malveillante de fichiers RDP (souvent utilisés dans des campagnes de phishing par des groupes comme APT29 pour le vol de données et d'identifiants).

**Vulnérabilités :**
*   Aucune CVE n'est associée à ce bug d'affichage. Il s'agit d'un problème d'interface utilisateur (UI) impactant l'efficacité des nouvelles protections de sécurité.
*   **Systèmes impactés :** Windows 11 (KB5083768, KB5083769), Windows 10 (KB5082200) et Windows Server (KB5082063).

**Recommandations :**
*   En attendant un correctif officiel de Microsoft, les utilisateurs confrontés à ce problème peuvent essayer d'harmoniser les paramètres de mise à l'échelle de leurs écrans.
*   Par mesure de précaution, il est fortement conseillé de ne pas ouvrir de fichiers .rdp provenant de sources inconnues ou non vérifiées, malgré les difficultés d'affichage des avertissements de sécurité, afin d'éviter toute compromission système.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-new-remote-desktop-warnings-may-display-incorrectly/){:target="_blank"}
