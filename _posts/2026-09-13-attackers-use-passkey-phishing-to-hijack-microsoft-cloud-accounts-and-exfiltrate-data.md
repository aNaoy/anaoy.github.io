---
title: 'Attackers Use Passkey Phishing to Hijack Microsoft Cloud Accounts and Exfiltrate Data'
date: 2026-09-13
permalink: /posts/2026/09/13/attackers-use-passkey-phishing-to-hijack-microsoft-cloud-accounts-and-exfiltrate-data/
tags:
- veille-cyber
- hackernews
---
### Menaces sur les environnements cloud : Phishing par Passkey et Fraude aux virements

Microsoft a mis en lumière deux campagnes d'attaques sophistiquées exploitant l'ingénierie sociale et les infrastructures de services tiers pour compromettre les environnements cloud et détourner des fonds.

**Points clés :**
*   **Fraude financière (BEC) :** Utilisation de l'IA générative pour créer des emails personnalisés et usurper l'identité de dirigeants (CEO/CFO). Les attaquants envoient de fausses factures (ex: ServiceNow) pour inciter les services comptables à effectuer des virements ACH.
*   **Ingénierie sociale "Passkey" :** Les attaquants contactent les employés par téléphone ou SMS en se faisant passer pour le support informatique. Ils incitent les victimes à mettre à jour leur configuration de sécurité (passkey, MFA) sur des sites frauduleux pour capturer les jetons d'authentification ou mener des attaques par "adversary-in-the-middle" (AitM).
*   **Persistance et exfiltration :** Une fois l'accès obtenu, les attaquants enregistrent leur propre méthode MFA pour maintenir une persistance, puis utilisent l'API Microsoft Graph pour explorer les données, extraire des documents de SharePoint/OneDrive et collecter des emails.
*   **Tactiques d'évasion :** Rotation fréquente des adresses IP et des infrastructures pour éviter la détection réseau, couplée à une utilisation légitime mais malveillante des API cloud.

**Vulnérabilités :**
L'attaque ne repose pas sur une CVE spécifique, mais sur l'exploitation des flux d'authentification (Device Code, AitM) et l'abus de l'API Microsoft Graph, qui, isolée, ne semble pas suspecte aux outils de surveillance classiques.

**Recommandations :**
*   **Analyse comportementale :** Ne pas se fier à une détection basée sur un seul appel API, mais corréler les événements de manière holistique pour identifier des progressions anormales.
*   **Renforcement de l'authentification :** Privilégier les clés de sécurité physiques FIDO2 qui résistent au phishing AitM, contrairement aux méthodes basées sur les SMS ou les OTP logiciels.
*   **Sensibilisation :** Alerter les employés sur les appels téléphoniques non sollicités prétendant provenir du support informatique concernant la mise à jour des accès MFA.
*   **Surveillance des logs :** Surveiller étroitement l'enregistrement de nouvelles méthodes MFA ou de nouveaux dispositifs d'authentification sur les comptes utilisateurs sensibles.
*   **Zero Trust :** Appliquer le principe du moindre privilège, particulièrement pour l'accès aux API Graph, et auditer régulièrement les permissions d'applications et les accès externes.

---
[Source](https://thehackernews.com/2026/09/attackers-use-passkey-phishing-to.html){:target="_blank"}
