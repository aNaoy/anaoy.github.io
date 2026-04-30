---
title: 'Bypassing Windows authentication reflection mitigations for SYSTEM shells - Part ②'
date: 2026-04-30
permalink: /posts/2026/04/30/bypassing-windows-authentication-reflection-mitigations-for-system-shells-part/
tags:
- veille-cyber
- zerodaysfans
---
### Contournement des mitigations de réflexion d'authentification Windows

Cette recherche explore de nouvelles méthodes pour contourner les protections contre la réflexion d'authentification Kerberos sur les systèmes Windows, permettant une élévation de privilèges (LPE) et une exécution de code à distance (RCE).

#### Points clés
*   **Technique de coercition :** L'utilisation de caractères Unicode (ex: `SⓇV1․AD․LOCAL`) permet de contourner les vérifications du service `DnsCache` et les conflits de nom DNS. Cela force la machine cible à s'authentifier auprès d'un serveur contrôlé par l'attaquant.
*   **Fonctionnement :** La réflexion exploite le fait que certaines fonctions de normalisation Windows (utilisées dans Active Directory et le DNS) considèrent des caractères Unicode comme équivalents aux caractères standards, permettant de générer des tickets Kerberos valides pour des comptes machines tout en évitant les collisions de records.
*   **Impact :** La technique permet d'obtenir une session SMB authentifiée en tant que `NT AUTHORITY\SYSTEM`. Bien que le vecteur principal via SMB ait été mitigé, d'autres services HTTP (ADCS, SCCM AdminService) restent vulnérables.

#### Vulnérabilités identifiées
*   **CVE-2026-24294 :** Abus de montage SMB sur des ports TCP arbitraires (Windows 11 24H2 / Server 2025).
*   **CVE-2025-33073 (Bypass) :** Technique de coercition Kerberos basée sur Unicode.
*   **CVE-2025-58726 :** Variantes de réflexion Kerberos via SMB.
*   **CVE-2026-26128 :** LPE via réflexion Kerberos locale (relais d'AP-REQ via IP locale).

#### Recommandations de sécurité
*   **Forcer l'intégrité SMB :** Activer systématiquement la signature SMB sur toutes les machines du domaine (notamment pour l'infrastructure SCCM).
*   **Sécuriser les services HTTP :** Désactiver les connecteurs HTTP non sécurisés et forcer l'utilisation du *Channel Binding* (liaison de canal) pour les services HTTPS.
*   **Filtrage réseau :** Restreindre strictement les flux réseau vers les services critiques comme le *SMS Provider* (SCCM) et les instances MSSQL.
*   **Gestion des services :** Auditer les services exposés ne supportant pas l'intégrité des communications, car ils restent des cibles privilégiées pour la réflexion Kerberos.
*   **Mises à jour :** Appliquer les correctifs cumulatifs de Microsoft, car les mitigations se concentrent désormais sur l'obligation de signature pour les connexions "loopback".

---
[Source](https://www.synacktiv.com/en/publications/bypassing-windows-authentication-reflection-mitigations-for-system-shells-part){:target="_blank"}
