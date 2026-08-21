---
title: 'Even MOAR Powershell, looking at Entra logins - the good, the bad and the password sprays, (Fri, Aug 21st)'
date: 2026-08-21
permalink: /posts/2026/08/21/even-moar-powershell-looking-at-entra-logins-the-good-the-bad-and-the-password-sprays-fri-aug-21st/
tags:
- veille-cyber
- sans-isc
---
### Surveillance et analyse des journaux de connexion Entra ID

La migration vers le cloud s'accompagne trop souvent d'un relâchement dans la surveillance proactive des journaux d'accès. L'utilisation des scripts PowerShell via le module `Microsoft.Graph` permet d'extraire des données critiques, souvent masquées dans l'interface standard, pour identifier des comportements malveillants tels que les attaques par "password spraying" (pulvérisation de mots de passe) ou des connexions géographiquement suspectes.

**Points clés**
*   **Visibilité accrue :** L'extraction granulaire des journaux de connexion (succès et échecs) révèle des informations essentielles comme la géolocalisation précise (ville, pays) et les raisons réelles des échecs d'authentification.
*   **Détection d'attaques :** L'analyse des échecs répétitifs permet d'identifier des attaques par force brute ou pulvérisation de mots de passe, souvent orchestrées via des services de proxy rotatifs.
*   **Analyse comportementale :** Filtrer les connexions réussies pour exclure les pays habituels de l'entreprise est une méthode efficace pour isoler des accès suspects provenant de régions non autorisées.

**Vulnérabilités associées**
*   **Exposition aux attaques de "Password Spraying" :** L'absence de surveillance des journaux d'échecs de connexion permet à des attaquants de tester des mots de passe courants sur de nombreux comptes sans déclencher d'alertes immédiates.
*   **Configuration inadéquate des politiques d'accès :** Des politiques d'accès conditionnel trop permissives permettent des connexions réussies depuis des zones géographiques atypiques.
*   *(Note : Aucune CVE spécifique n'est mentionnée, car il s'agit d'un problème de configuration et de monitoring opérationnel).*

**Recommandations**
*   **Automatiser l'audit :** Utiliser régulièrement les scripts PowerShell fournis pour extraire et analyser les journaux de connexion (`Get-MgAuditLogSignIn`).
*   **Renforcer l'accès conditionnel :** Ajuster les politiques d'accès conditionnel d'Entra ID en fonction des tendances observées dans les logs, notamment en restreignant les accès par zones géographiques.
*   **Surveiller les anomalies de localisation :** Mettre en place des alertes pour toute connexion réussie provenant de pays en dehors du périmètre habituel d'activité de l'organisation.
*   **Corrélation des alertes :** Porter une attention particulière aux alertes de type "IP address with malicious activity", qui indiquent souvent l'utilisation de services de proxy malveillants.

---
[Source](https://isc.sans.edu/diary/rss/33268){:target="_blank"}
