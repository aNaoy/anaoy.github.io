---
title: 'TeamFiltration Campaign Compromises Seven Microsoft 365 Accounts Using Default Passwords'
date: 2026-09-24
permalink: /posts/2026/09/24/teamfiltration-campaign-compromises-seven-microsoft-365-accounts-using-default-passwords/
tags:
- veille-cyber
- hackernews
---
### Campagne « UNK_CondorFiltration » : La menace des comptes de service oubliés

La campagne **UNK_CondorFiltration** a ciblé plus de 5 700 comptes Microsoft 365 au sein de 28 organisations, principalement dans les secteurs de la vente au détail et de la finance au Chili. Menée via le framework offensif **TeamFiltration**, cette opération a permis de compromettre sept comptes de service grâce à des attaques par force brute (password spraying).

**Points clés :**
*   **Mode opératoire :** Utilisation du framework légitime *TeamFiltration* pour énumérer des comptes, tester des mots de passe par défaut, exfiltrer des données et obtenir un accès persistant via Microsoft Graph API.
*   **Origine :** Le trafic provient de 1 487 adresses IP AWS EC2 distinctes.
*   **Cibles privilégiées :** Les comptes de service ou fonctionnels « non managés » et oubliés, plutôt que les comptes d'utilisateurs individuels.
*   **Impact :** Une fois l'accès obtenu, les attaquants pivotent vers des services comme OneDrive, SharePoint et le portail Azure, souvent via des nœuds VPN pour dissimuler leur origine.

**Vulnérabilités :**
*   **Absence de MFA :** Les comptes compromis n'étaient pas protégés par une authentification multifacteur.
*   **Gestion des identités :** Utilisation de mots de passe par défaut jamais renouvelés sur des comptes de service dormants, créant une surface d'attaque non surveillée.
*   *Note : Aucune CVE spécifique n'est associée, car il s'agit d'une exploitation de mauvaises pratiques de configuration (Security Misconfiguration).*

**Recommandations :**
*   **Audit des comptes de service :** Identifier et inventorier tous les comptes non humains au sein du tenant Microsoft 365.
*   **Rotation et durcissement :** Appliquer une politique de rotation régulière des mots de passe pour tous les comptes et supprimer systématiquement les comptes obsolètes.
*   **Généralisation du MFA :** Imposer l'authentification multifacteur sur tous les types de comptes, y compris les services techniques.
*   **Surveillance accrue :** Mettre en place une surveillance spécifique sur les activités anormales liées aux comptes de service (connexions inhabituelles, requêtes API intensives, accès aux données SharePoint/OneDrive).

---
[Source](https://thehackernews.com/2026/09/teamfiltration-compromises-seven.html){:target="_blank"}
