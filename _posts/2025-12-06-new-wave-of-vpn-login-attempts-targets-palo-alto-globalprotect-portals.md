---
title: 'New wave of VPN login attempts targets Palo Alto GlobalProtect portals'
date: 2025-12-06
permalink: /posts/2025/12/06/new-wave-of-vpn-login-attempts-targets-palo-alto-globalprotect-portals/
tags:
- veille-cyber
- bleepingcomp
---
**Vague d'attaques ciblant les portails VPN d'entreprises**

Une campagne d'attaques par force brute visant les portails GlobalProtect de Palo Alto Networks a été observée, suivie par des scans dirigés vers les points d'API de SonicWall SonicOS. Ces activités, initiées depuis l'infrastructure d'une société allemande (3xK GmbH) et impliquant plus de 7 000 adresses IP, ont débuté début décembre. Des schémas d'empreintes digitales observés précédemment indiquent qu'il s'agit du même acteur.

**Points Clés :**

*   **Ciblage :** Portails VPN Palo Alto GlobalProtect et API SonicWall SonicOS.
*   **Méthodes :** Attaques par force brute sur les identifiants et scans d'API.
*   **Origine :** Infrastructure de 3xK GmbH, avec une concentration d'IP allemandes.
*   **Contexte :** Les scans d'API SonicWall pourraient préparer l'exploitation de vulnérabilités futures ou identifier des erreurs de configuration.
*   **Déclaration de Palo Alto Networks :** La société confirme des scans accrus, les qualifie d'attaques basées sur des identifiants et non d'exploits de vulnérabilités logicielles, et assure qu'il n'y a pas eu de compromission de ses produits.

**Vulnérabilités :**

*   Aucune vulnérabilité logicielle spécifique (CVE) n'est mentionnée comme étant directement exploitée dans cette campagne. Les attaques ciblent principalement des tentatives d'authentification par identifiants (credential-based attacks) sur GlobalProtect et des scans sur les API SonicWall.

**Recommandations :**

*   Mettre en œuvre l'authentification multifacteur (MFA) pour contrer les attaques par identifiants.
*   Surveiller les surfaces d'authentification pour une vitesse inhabituelle ou des échecs répétés.
*   Suivre les empreintes digitales récurrentes des clients.
*   Utiliser un blocage dynamique et contextuel plutôt que des listes de réputation statiques.
*   Surveiller et bloquer les adresses IP associées à ce type d'activité.

---
[Source](https://www.bleepingcomputer.com/news/security/new-wave-of-vpn-login-attempts-targets-palo-alto-globalprotect-portals/){:target="_blank"}
