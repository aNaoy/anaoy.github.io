---
title: 'Microsoft blames macOS update for undismissible Teams location prompts'
date: 2026-05-19
permalink: /posts/2026/05/19/microsoft-blames-macos-update-for-undismissible-teams-location-prompts/
tags:
- veille-cyber
- bleepingcomp
---
### Bug de localisation persistante sur Microsoft Teams pour macOS

Des utilisateurs de Microsoft Teams sur macOS signalent l'apparition récurrente de fenêtres contextuelles demandant l'accès à la localisation, rendant l'interface inutilisable en raison de l'impossibilité de les fermer.

**Points clés :**
* **Origine du problème :** Une récente mise à jour de sécurité de macOS empêche le système d'exploitation d'enregistrer correctement les préférences de permission de localisation définies pour l'application Teams.
* **Incident officiel :** Microsoft a confirmé l'incident (référence TM1315837) et collabore avec Apple pour déployer une résolution.
* **Vulnérabilité :** Aucune CVE n'est associée, il s'agit d'un conflit de fonctionnement entre la gestion des permissions de macOS et le client Teams.

**Recommandations :**
En attendant un correctif officiel, les utilisateurs impactés peuvent tenter de résoudre le problème via les réglages système :
1. Accéder à **Réglages Système > Confidentialité et sécurité > Service de localisation**.
2. Rechercher **"Microsoft Teams"** et **"Microsoft Teams ModuleHost"**.
3. Activer et désactiver les curseurs correspondants, puis les configurer à nouveau sur le choix souhaité pour réinitialiser la persistance du réglage.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-blames-undismissible-teams-location-prompts-on-macos-update/){:target="_blank"}
