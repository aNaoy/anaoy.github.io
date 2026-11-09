---
title: 'Default admin:admin Server Password Helps Researchers Hack Two Automakers, Unlock and Start Cars'
date: 2026-11-09
permalink: /posts/2026/11/09/default-adminadmin-server-password-helps-researchers-hack-two-automakers-unlock-and-start-cars/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans les systèmes d'identité de véhicules connectés

Deux chercheurs en cybersécurité ont démontré qu'il était possible de prendre le contrôle total de comptes clients auprès de deux constructeurs automobiles, permettant notamment le déverrouillage et le démarrage à distance de leurs véhicules. L'attaque exploitait une mauvaise configuration de la plateforme de gestion d'identité **ForgeRock** (désormais Ping Identity), utilisée par les constructeurs pour leurs applications mobiles.

**Points clés :**
* **Accès non autorisé :** En accédant à la console d'administration **OpenIDM** laissée avec ses identifiants par défaut (`admin:admin`), les chercheurs ont pu exécuter du code arbitraire sur le serveur.
* **Élévation de privilèges :** Via l'interface d'administration, les attaquants ont accédé aux bases de données clients, leur permettant de modifier les emails et mots de passe des utilisateurs légitimes pour s'emparer de leurs comptes.
* **Contournement de sécurité :** Les chercheurs ont utilisé une technique d'encodage (path traversal/obfuscation) pour tromper les filtres de sécurité en périphérie (WAF/Edge) et accéder à une console normalement protégée.
* **Risque global :** Une seconde vulnérabilité liée à des identifiants de test codés en dur dans l'application a permis d'étendre les risques aux utilisateurs en Australie, en plus des États-Unis et du Canada.

**Vulnérabilités :**
* **Pas de CVE assignée :** Il ne s'agit pas d'une faille logicielle intrinsèque, mais d'une erreur de configuration humaine (non-respect des guides de durcissement/hardening).
* **Usage de paramètres par défaut :** Utilisation du compte `admin:admin` sur la console Apache Felix.
* **Exposition de données sensibles :** Absence de suppression des outils de développement/administration en environnement de production.

**Recommandations :**
* **Durcissement des systèmes :** Supprimer systématiquement les consoles d'administration inutiles (ex: Apache Felix via `/system/console`) ou modifier immédiatement les identifiants par défaut avant la mise en service.
* **Ne pas se fier aux pare-feux applicatifs (WAF) :** Ne pas considérer le masquage des URL par les équipements de périphérie comme une mesure de sécurité suffisante ; les différences d'interprétation des chemins entre le serveur et l'équipement de sécurité peuvent être exploitées.
* **Audit du code :** Scanner le code applicatif pour supprimer toute référence à des identifiants de test ou des configurations de débogage avant le déploiement en production.

---
[Source](https://thehackernews.com/2026/11/default-adminadmin-server-password.html){:target="_blank"}
