---
title: 'Claude Cowork Flaw Could Let AI Agent Escape Its VM and Access Mac Files'
date: 2026-07-23
permalink: /posts/2026/07/23/claude-cowork-flaw-could-let-ai-agent-escape-its-vm-and-access-mac-files/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique "SharedRoot" dans Claude Cowork

Des chercheurs en cybersécurité ont identifié une vulnérabilité d'évasion de bac à sable (sandbox escape) baptisée **SharedRoot**, affectant les sessions locales de l'agent IA *Claude Cowork* sur macOS. Cette faille permet à un agent malveillant de s'extraire de sa machine virtuelle (VM) Linux pour accéder librement au système de fichiers de l'hôte (le Mac), compromettant potentiellement des données sensibles comme des clés SSH ou des identifiants cloud.

**Points clés :**
*   **Mécanisme :** Le démon `coworkd` partage l'intégralité du système de fichiers de l'hôte (`/`) avec la VM en mode lecture-écriture (`/mnt/.virtiofs-root`).
*   **Exploitation :** En utilisant les espaces de noms utilisateur, l'agent obtient les privilèges `CAP_NET_ADMIN`, ce qui lui permet d'exploiter des vulnérabilités du noyau Linux pour devenir "root" au sein de la VM. Une fois root dans la VM, l'attaquant accède directement au système de fichiers du Mac.
*   **Risque structurel :** Les chercheurs soulignent que cette vulnérabilité fait partie d'une classe de bugs récurrents dans le noyau Linux, rendant la simple correction logicielle insuffisante face à de nouvelles variantes.

**Vulnérabilité identifiée :**
*   **CVE-2026-46331 (pedit COW) :** Faille exploitée dans le sous-système de filtrage de paquets (`act_pedit`) du noyau Linux permettant une élévation de privilèges vers "guest-root".

**Recommandations :**
*   **Pour les utilisateurs :** Privilégier l'exécution de *Claude Cowork* via le cloud plutôt qu'en mode local.
*   **Pour l'architecture système :**
    *   Désactiver les espaces de noms utilisateur non privilégiés.
    *   Restreindre le partage de fichiers au sein de la VM aux seuls répertoires strictement nécessaires (au lieu de la racine `/`) et privilégier le mode lecture seule.
    *   Durcir la configuration de `coworkd` (ex: `ProtectSystem=strict`).
    *   Empêcher le chargement automatique des modules noyau inutilisés.

---
[Source](https://thehackernews.com/2026/07/claude-cowork-flaw-could-let-ai-agent.html){:target="_blank"}
