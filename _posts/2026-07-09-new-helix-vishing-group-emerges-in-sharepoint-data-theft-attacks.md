---
title: 'New Helix vishing group emerges in SharePoint data theft attacks'
date: 2026-07-09
permalink: /posts/2026/07/09/new-helix-vishing-group-emerges-in-sharepoint-data-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Émergence du groupe de cyber-extorsion Helix : Menaces sur SharePoint

Le groupe « Helix » s'est imposé comme une nouvelle menace spécialisée dans l'exfiltration de données via des environnements SharePoint. Ses opérations reposent sur une ingénierie sociale sophistiquée et une exploitation ciblée de l'identité numérique.

**Points clés :**
*   **Mode opératoire :** Le groupe utilise le *vishing* (phishing vocal) en se faisant passer pour des supérieurs hiérarchiques pour manipuler les employés.
*   **Techniques d'accès :** Les attaquants exploitent le flux d'authentification par code d'appareil (*device code phishing*) et contournent le MFA en enregistrant leur propre application d'authentification pour maintenir leur persistance.
*   **Exfiltration :** Une fois le compte compromis, Helix utilise des scripts automatisés (notamment via l'agent utilisateur `python-requests/2.28.1`) pour recenser et télécharger massivement les contenus SharePoint.
*   **Filiation probable :** Les chercheurs soupçonnent un lien direct ou une continuité avec les groupes disparus ShinyHunters et BlackFile, en raison de similitudes dans l'infrastructure utilisée et les méthodes d'ingénierie sociale.

**Vulnérabilités exploitées :**
*   **Abus du flux de code d'appareil :** Utilisation détournée de la fonctionnalité légitime permettant de lier des appareils à des comptes Microsoft 365.
*   **Faiblesse de la vérification d'identité :** Sensibilité des employés aux attaques de *vishing* et au spoofing de l'identité des cadres.
*   *Note : Aucune CVE spécifique n'est associée, car il s'agit d'une exploitation de fonctionnalités légitimes (abus de conception et ingénierie sociale).*

**Recommandations :**
*   **Désactivation du code d'appareil :** Désactiver l'authentification par code d'appareil dans les politiques Microsoft 365 chaque fois que cela est possible.
*   **Restriction des accès :** Limiter l'accès aux ressources SharePoint et aux données sensibles aux seuls appareils gérés et conformes.
*   **Filtrage réseau :** Bloquer les connexions provenant de domaines nouvellement enregistrés ou suspects, souvent utilisés par Helix pour ses campagnes.
*   **Sensibilisation :** Former les collaborateurs aux risques de *vishing* et aux procédures de vérification d'identité pour toute demande inhabituelle par téléphone.

---
[Source](https://www.bleepingcomputer.com/news/security/new-helix-vishing-group-emerges-in-sharepoint-data-theft-attacks/){:target="_blank"}
