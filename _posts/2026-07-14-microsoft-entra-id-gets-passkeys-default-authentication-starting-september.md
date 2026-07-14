---
title: 'Microsoft Entra ID gets passkeys default authentication starting September'
date: 2026-07-14
permalink: /posts/2026/07/14/microsoft-entra-id-gets-passkeys-default-authentication-starting-september/
tags:
- veille-cyber
- bleepingcomp
---
# Transition vers l'authentification par passkeys dans Microsoft Entra ID

Dès septembre 2026, Microsoft instaurera les passkeys comme méthode d'authentification par défaut dans Entra ID. Cette mesure vise à remplacer les méthodes basées sur les SMS et les appels vocaux, qui seront définitivement retirées le 1er février 2027.

### Points clés
*   **Automatisation :** Les utilisateurs exploitant actuellement l'authentification par SMS ou téléphone seront automatiquement basculés vers les passkeys lors de leur prochaine connexion.
*   **Méthodes persistantes :** Les utilisateurs utilisant déjà des méthodes résistantes au phishing (Windows Hello, FIDO2, smart cards) ne sont pas concernés par ce changement.
*   **Risque accru :** L'utilisation de méthodes basées sur la téléphonie est devenue une cible privilégiée des attaquants, notamment via des campagnes de phishing assistées par IA et des attaques sur le SSO.

### Vulnérabilités et risques
*   **Phishing traditionnel et IA :** Les méthodes SMS/voix sont vulnérables au phishing. Microsoft souligne que les campagnes de phishing dopées à l'IA atteignent désormais des taux de clic de 54 %.
*   **Vol d'identifiants :** Les attaques sur les comptes SSO (comme celles observées récemment avec le groupe ShinyHunters) exploitent la fragilité des facteurs d'authentification phishables pour voler des données SaaS.
*   *Note : Aucune CVE spécifique n'est mentionnée, le risque est structurel aux méthodes d'authentification obsolètes.*

### Recommandations
*   **Anticipation :** Migrer les utilisateurs vers des méthodes résistantes au phishing avant la date limite de février 2027 pour éviter toute interruption de service.
*   **Audit :** Utiliser le script PowerShell [Entra SMS/Voice Policy Scanner](https://github.com/microsoft/entra-sms-voice-usage-analyzer) pour identifier les utilisateurs encore dépendants des méthodes basées sur la téléphonie.
*   **Continuité :** Pour les organisations ayant une dépendance impérative aux services télécoms, configurer des fournisseurs tiers via le Microsoft Security Store avant le retrait des capacités natives de Microsoft.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-entra-id-gets-passkeys-default-authentication-starting-september/){:target="_blank"}
