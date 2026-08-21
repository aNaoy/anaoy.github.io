---
title: 'Who Got Missed in the MFA Rollout&#x3f; More Powershell &#x2b; Graph &#x2b; Entra scripting&#x21;, (Fri, Aug 21st)'
date: 2026-08-21
permalink: /posts/2026/08/21/who-got-missed-in-the-mfa-rolloutx3f-more-powershell-x2b-graph-x2b-entra-scriptingx21-fri-aug-21st/
tags:
- veille-cyber
- sans-isc
---
### Optimisation du déploiement MFA via Microsoft Graph PowerShell

Le déploiement de l'authentification multifacteur (MFA) dans une organisation nécessite un suivi rigoureux pour identifier les comptes non protégés. L'utilisation de scripts PowerShell permet d'automatiser cette surveillance, évitant ainsi la vérification manuelle fastidieuse via l'interface web.

**Points clés :**
*   **Automatisation :** Utilisation du module `Microsoft.Graph.Beta` pour extraire les données d'enregistrement MFA des utilisateurs.
*   **Visibilité :** Création d'une liste dynamique filtrant les utilisateurs n'ayant pas activé la MFA (`IsMfaRegistered -eq $false`).
*   **Audit approfondi :** Possibilité d'auditer les méthodes d'authentification faibles (comme le SMS ou les appels vocaux) pour renforcer la sécurité globale.

**Vulnérabilités :**
*   **Absence de MFA :** Les comptes utilisateurs sans MFA constituent une porte d'entrée critique pour les attaques par compromission de mots de passe.
*   **Méthodes d'authentification obsolètes :** L'usage du SMS ou de l'appel vocal (`voiceMobile`) est vulnérable aux techniques de *SIM swapping* et d'interception. 
*   *Note : Aucune CVE spécifique n'est associée à cet article, car il traite de bonnes pratiques de configuration plutôt que de failles logicielles.*

**Recommandations :**
*   **Généraliser la MFA :** Identifier et forcer l'enregistrement MFA pour l'ensemble des utilisateurs actifs.
*   **Audit régulier :** Utiliser les commandes Graph pour auditer périodiquement les méthodes d'authentification et supprimer les options moins sécurisées (SMS/Voix).
*   **Utilisation des permissions :** Lors de l'exécution du script, limiter les accès au strict nécessaire (`AuditLog.Read.All` et `User.Read.All`).

---
[Source](https://isc.sans.edu/diary/rss/33272){:target="_blank"}
