---
title: 'Microsoft Patches Severe Entra ID Flaw (CVSS 10.0) Allowing Remote Code Execution'
date: 2026-08-21
permalink: /posts/2026/08/21/microsoft-patches-severe-entra-id-flaw-cvss-100-allowing-remote-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique corrigée dans Microsoft Entra ID

Microsoft a corrigé une faille de sécurité critique au sein de son service de gestion des identités et des accès, Microsoft Entra ID (anciennement Azure Active Directory). Bien qu'initialement signalée comme étant exploitée, l'entreprise a rectifié l'information : aucune exploitation active n'a été détectée.

**Points clés :**
*   **Vulnérabilité :** Exécution de code à distance (RCE) due à une désérialisation de données non fiables.
*   **CVE :** CVE-2026-69836.
*   **Sévérité :** Score CVSS de 10.0 (critique).
*   **Origine :** La faille provient d'un traitement incorrect des données fournies par l'utilisateur lors de la désérialisation, permettant à un attaquant non autorisé d'exécuter du code sur le réseau.
*   **Découverte :** Signalée par Robert Fitzpatrick, ingénieur en sécurité chez Microsoft.

**Recommandations :**
*   **Aucune action requise :** Microsoft a intégralement déployé les correctifs nécessaires côté serveur. Les utilisateurs du service n'ont aucune mesure corrective à effectuer.

---
[Source](https://thehackernews.com/2026/08/microsoft-entra-id-flaw-cvss-100.html){:target="_blank"}
