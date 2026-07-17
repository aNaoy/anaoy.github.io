---
title: 'Claude Chrome extension flaw lets malicious extensions trigger AI actions'
date: 2026-07-17
permalink: /posts/2026/07/17/claude-chrome-extension-flaw-lets-malicious-extensions-trigger-ai-actions/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité d'automatisation dans l'extension Chrome de Claude

Une faille de sécurité critique dans l'extension Chrome d'Anthropic permet à des extensions malveillantes de déclencher les flux de travail automatisés de Claude sans intervention réelle de l'utilisateur. En injectant du JavaScript sur le domaine `claude.ai`, une extension frauduleuse peut simuler des clics utilisateur et forcer l'exécution de tâches liées aux services connectés (Gmail, Google Docs, Google Calendar, Salesforce).

**Points clés :**
*   **Vecteur d'attaque :** Une extension malveillante installée sur le navigateur peut manipuler le contenu de la page `claude.ai` pour déclencher des actions pré-configurées.
*   **Absence de vérification :** L'extension Claude ne vérifie pas la propriété `Event.isTrusted` des événements de clic, acceptant ainsi des interactions générées par script comme s'il s'agissait d'actions légitimes de l'utilisateur.
*   **Portée :** L'attaque est limitée aux neuf flux de travail prédéfinis de l'extension. L'impact est amplifié si l'utilisateur a activé l'option « Act without asking » (Agir sans demander).
*   **Vulnerabilités :** 
    *   **Défaut de validation des clics :** Absence de contrôle de confiance sur les événements déclencheurs.
    *   **Bypass de permissions :** Présence d'un paramètre interne `skipPermissions=true` potentiellement exploitable en combinaison avec d'autres failles.
    *   *Note : Aucune CVE n'a été attribuée à ce jour pour ces vulnérabilités.*

**Recommandations :**
*   **Désactiver l'automatisation :** Éviter d'activer le paramètre « Act without asking » dans les réglages de l'extension Claude pour forcer une confirmation humaine avant toute action sensible.
*   **Prudence avec les extensions :** Installer uniquement des extensions de confiance, car une extension malveillante avec accès aux permissions sur le domaine `claude.ai` peut exploiter cette faille.
*   **Veille :** Surveiller les futures mises à jour de l'extension (version 1.0.80 actuelle toujours vulnérable) pour l'application d'un correctif de la part d'Anthropic.

---
[Source](https://www.bleepingcomputer.com/news/security/claude-chrome-extension-flaw-lets-malicious-extensions-trigger-ai-actions/){:target="_blank"}
