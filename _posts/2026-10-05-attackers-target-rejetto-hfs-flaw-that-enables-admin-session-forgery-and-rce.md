---
title: 'Attackers Target Rejetto HFS Flaw That Enables Admin Session Forgery and RCE'
date: 2026-10-05
permalink: /posts/2026/10/05/attackers-target-rejetto-hfs-flaw-that-enables-admin-session-forgery-and-rce/
tags:
- veille-cyber
- hackernews
---
### Exploitation active de la faille critique dans Rejetto HFS

Une vulnérabilité critique dans le serveur Rejetto HTTP File Server (HFS) fait actuellement l'objet de tentatives d'exploitation réelles. Cette faille permet à un attaquant non authentifié de falsifier des sessions administrateur pour prendre le contrôle total du serveur et exécuter du code à distance.

**Points clés :**
*   **Mécanisme d'attaque :** Le serveur utilise un générateur de nombres pseudo-aléatoires non cryptographique (`Math.random()`) pour créer ses clés de signature de session. En collectant quelques réponses de connexion, un attaquant peut reconstruire l'état du générateur, récupérer la clé et forger un cookie de session administrateur valide.
*   **Impact :** Une fois l'accès administrateur obtenu, l'attaquant peut utiliser la fonctionnalité de configuration `server_code` pour exécuter du JavaScript arbitraire côté serveur.
*   **Contexte :** La faille a été découverte via le modèle d'IA "Mythos" d'Anthropic. Bien qu'un correctif soit disponible depuis juillet 2026, la publication récente d'un exploit PoC (Proof-of-Concept) a entraîné une augmentation des activités malveillantes, notamment des reconnaissances ciblées en provenance d'adresses IP localisées en Chine.

**Vulnérabilité :**
*   **CVE-2026-61500** (Score CVSS : 9.3) : Altération de session par prédictibilité du générateur de nombres aléatoires, menant à une exécution de code à distance (RCE).

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer le correctif en installant la version **3.2.1** ou ultérieure de Rejetto HFS.
*   **Surveillance :** Inspecter les journaux de connexion et de configuration du serveur à la recherche d'activités suspectes ou d'accès administrateur non autorisés.

---
[Source](https://thehackernews.com/2026/10/attackers-target-rejetto-hfs-flaw-that.html){:target="_blank"}
