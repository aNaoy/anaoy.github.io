---
title: 'Russian COLD RELIC Hackers Use Stolen Google Workspace Data to Breach Second U.S. Organization'
date: 2026-11-18
permalink: /posts/2026/11/18/russian-cold-relic-hackers-use-stolen-google-workspace-data-to-breach-second-us-organization/
tags:
- veille-cyber
- hackernews
---
### Espionnage Cyber : La stratégie de rebond du groupe Cold Relic

Le groupe d'espionnage russe **Cold Relic** (également connu sous les noms de Callisto, Star Blizzard ou UNC4057) exploite des données volées lors de compromissions initiales pour lancer des attaques en chaîne contre des organisations tierces, en utilisant l'usurpation d'identité et l'ingénierie sociale.

**Points clés :**
*   **Mode opératoire :** Le groupe utilise des proxys résidentiels pour l'accès initial, puis s'appuie sur des attaques de fatigue MFA et l'usurpation de comptes Super Admin.
*   **Persistance :** Les attaquants enregistrent leurs propres appareils MFA, des *passkeys* et des codes de secours, ce qui leur permet de maintenir l'accès même après des réinitialisations de mots de passe ou de sessions.
*   **Mouvement latéral :** Une fois le premier environnement cloud (Google Workspace) compromis, ils utilisent les informations extraites (annuaires, historique d'e-mails) pour piéger des contacts professionnels via des services de messagerie sécurisés.
*   **Abus de services légitimes :** Utilisation de Google Takeout pour exfiltrer des données massives et manipulation des logs de sécurité pour effacer leurs traces.

**Vulnérabilités exploitées :**
L'article ne mentionne pas de CVE spécifique, car il s'agit d'une exploitation de **vulnérabilités de processus et de gestion des identités** :
*   Sensibilité à la fatigue des notifications MFA (Push).
*   Persistance des *passkeys* non révoqués lors des procédures de sécurité standards.
*   Abus de privilèges Super Admin sans contrôle d'accès suffisant sur les outils d'exportation (Google Takeout).

**Recommandations :**
*   **Sécurité MFA :** Privilégier les méthodes d'authentification résistantes au phishing (clés de sécurité physiques FIDO2) plutôt que les notifications push classiques.
*   **Gestion des accès :** Auditer régulièrement les appareils enregistrés dans la console d'administration et supprimer les *passkeys* ou appareils non reconnus.
*   **Visibilité et logs :** Surveiller les alertes liées à l'exportation massive de données (Google Takeout) et aux modifications de paramètres de sécurité par les comptes à hauts privilèges.
*   **Formation :** Sensibiliser les employés à la méfiance vis-à-vis des liens de partage de documents, même lorsqu'ils proviennent de contacts familiers ou de relations professionnelles établies, en raison du haut niveau d'usurpation pratiqué par le groupe.

---
[Source](https://thehackernews.com/2026/11/russian-cold-relic-hackers-use-stolen.html){:target="_blank"}
