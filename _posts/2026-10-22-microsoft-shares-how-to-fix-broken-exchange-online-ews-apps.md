---
title: 'Microsoft shares how to fix broken Exchange Online EWS apps'
date: 2026-10-22
permalink: /posts/2026/10/22/microsoft-shares-how-to-fix-broken-exchange-online-ews-apps/
tags:
- veille-cyber
- bleepingcomp
---
### Transition vers Microsoft Graph : gestion de l'arrêt des services EWS

Microsoft a entamé le retrait progressif de l'API Exchange Web Services (EWS) dans Exchange Online, marquant la fin de cette technologie au profit de Microsoft Graph. Bien que le blocage par défaut ait débuté le 1er octobre 2026, les administrateurs peuvent temporairement restaurer l'accès jusqu'au retrait définitif prévu le 1er avril 2027.

**Points clés :**
*   **Impact :** Les applications dépendant d'EWS (compléments Outlook, clients mail, outils de calendrier) peuvent afficher des erreurs de connexion ou des demandes répétées d'authentification.
*   **Périmètre :** Cette mesure concerne exclusivement Microsoft 365 et Exchange Online. Les environnements Exchange Server sur site ne sont pas affectés.
*   **Obsolescence :** L'API EWS ne bénéficie plus de mises à jour fonctionnelles depuis 2018.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, mais le retrait des API EWS s'inscrit dans une démarche de sécurité continue visant à réduire la surface d'attaque et à moderniser les protocoles d'accès.

**Recommandations :**
*   **Solution temporaire :** Les administrateurs peuvent réactiver EWS via le centre d'administration Microsoft 365 (paramètre *Baseline Security Mode*) ou en utilisant la commande PowerShell : `Set-OrganizationConfig -EWSEnabled $true`.
*   **Solution pérenne :** Migrer impérativement les applications vers **Microsoft Graph API**, qui offre une parité fonctionnelle quasi complète.
*   **Action immédiate :** Contacter les éditeurs de logiciels pour obtenir des versions mises à jour des applications ou procéder à une réécriture du code propriétaire pour supprimer la dépendance à EWS avant avril 2027.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-shares-how-to-fix-broken-exchange-online-ews-apps/){:target="_blank"}
