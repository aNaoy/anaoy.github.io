---
title: 'Open VSX Bug Let Malicious VS Code Extensions Bypass Pre-Publish Security Checks'
date: 2026-03-27
permalink: /posts/2026/03/27/open-vsx-bug-let-malicious-vs-code-extensions-bypass-pre-publish-security-checks/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité "Open Sesame" : Contournement des contrôles de sécurité sur Open VSX

Une faille critique, baptisée « Open Sesame », a été identifiée dans le processus de vérification automatique des extensions sur Open VSX, la plateforme utilisée par VS Code, Cursor et Windsurf. Cette vulnérabilité permettait à des extensions malveillantes de contourner totalement les analyses de sécurité obligatoires lors de leur publication.

**Points clés :**
*   **Défaut de conception (Fail-Open) :** Le pipeline de scan utilisait une valeur booléenne unique pour distinguer deux états : « aucun scanner configuré » et « échec du scan ». En cas de saturation du système, le service interprétait l'erreur comme une absence de scan nécessaire et autorisait la publication.
*   **Exploitation par déni de service :** Un attaquant pouvait saturer le pool de connexions à la base de données en inondant la plateforme d'extensions, forçant ainsi les scanners à échouer et déclenchant automatiquement la validation par défaut.
*   **Impact :** Cette méthode permettait à n'importe quel utilisateur disposant d'un compte développeur gratuit de déployer du code malveillant sans contrôle préalable.

**Vulnérabilité :**
*   Bien qu'aucune CVE spécifique n'ait été assignée à ce jour, le problème résidait dans une erreur de gestion d'état dans le service Java d'Open VSX.

**Recommandations :**
*   **Mise à jour :** La faille a été corrigée dans la version **0.32.0** d'Open VSX. Il est conseillé aux administrateurs de serveurs Open VSX privés de s'assurer que cette version (ou une plus récente) est déployée.
*   **Bonnes pratiques de développement :** Les systèmes de sécurité ne doivent jamais utiliser une logique de type « fail-open ». Les états d'échec doivent être explicitement distingués des états de réussite ou d'inactivité. En cas d'impossibilité d'exécuter un scan, le système doit par défaut bloquer la publication et placer l'extension en quarantaine pour une revue humaine.

---
[Source](https://thehackernews.com/2026/03/open-vsx-bug-let-malicious-vs-code.html){:target="_blank"}
