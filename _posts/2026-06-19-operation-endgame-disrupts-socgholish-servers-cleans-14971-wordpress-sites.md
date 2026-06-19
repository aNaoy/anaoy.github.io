---
title: 'Operation Endgame Disrupts SocGholish Servers, Cleans 14,971 WordPress Sites'
date: 2026-06-19
permalink: /posts/2026/06/19/operation-endgame-disrupts-socgholish-servers-cleans-14971-wordpress-sites/
tags:
- veille-cyber
- hackernews
---
### Démantèlement de l'infrastructure SocGholish par l'Opération Endgame

Une coalition internationale de forces de l'ordre (Pays-Bas, Canada, Allemagne, États-Unis) a neutralisé l'infrastructure du réseau malveillant **SocGholish** (également connu sous le nom de FakeUpdates). Cette opération a permis de mettre hors service 106 serveurs et de nettoyer près de 15 000 sites WordPress infectés.

**Points clés :**
*   **Activité :** Actif depuis 2017, SocGholish opère comme un courtier d'accès initial. Il utilise des sites web compromis pour distribuer des malwares via de fausses mises à jour logicielles (navigateurs, etc.).
*   **Modèle opérationnel :** Le groupe utilise des systèmes de redirection de trafic (TDS) pour filtrer les victimes selon leur géolocalisation, leur système d'exploitation et leur navigateur, avant de déployer des charges utiles (ransomwares, espionnage, RAT).
*   **Écosystème criminel :** SocGholish sert de vecteur d'entrée à des groupes majeurs comme Evil Corp, LockBit, RansomHub et Raspberry Robin. 
*   **Techniques de compromission :** Injection directe de JavaScript sur des sites WordPress et utilisation du "Domain Shadowing" (création de sous-domaines malveillants sur des domaines légitimes via un accès DNS compromis).

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur la compromission directe des comptes d'administration des sites WordPress, des comptes de fournisseurs DNS/registrars, et sur l'ingénierie sociale (fausses mises à jour).

**Recommandations pour les propriétaires de sites WordPress :**
*   **Mise à jour :** Maintenir le CMS, les thèmes et les extensions à jour pour combler les failles exploitables.
*   **Authentification :** Modifier immédiatement tous les identifiants d'accès (mots de passe, clés API).
*   **Audit de sécurité :** Supprimer tout compte utilisateur suspect ou inconnu ajouté sur le site.
*   **Surveillance DNS :** Vérifier régulièrement les enregistrements DNS pour détecter toute création de sous-domaines non autorisée (Shadowing).

---
[Source](https://thehackernews.com/2026/06/operation-endgame-disrupts-socgholish.html){:target="_blank"}
