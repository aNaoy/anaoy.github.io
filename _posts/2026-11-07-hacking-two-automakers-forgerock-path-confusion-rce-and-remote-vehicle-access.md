---
title: 'Hacking Two Automakers: ForgeRock Path Confusion, RCE, and Remote Vehicle Access'
date: 2026-11-07
permalink: /posts/2026/11/07/hacking-two-automakers-forgerock-path-confusion-rce-and-remote-vehicle-access/
tags:
- veille-cyber
- zerodaysfans
---
# Vulnérabilité critique : Accès aux véhicules via ForgeRock

Des chercheurs en sécurité ont découvert une chaîne de vulnérabilités permettant d'obtenir l'exécution de code à distance (RCE) sur les serveurs ForgeRock de deux constructeurs automobiles. En exploitant cet accès, il était possible de prendre le contrôle total des comptes clients et, par extension, de piloter à distance les véhicules connectés (localisation, déverrouillage, démarrage).

### Points clés
*   **Chaîne d'exploitation :** Contournement du WAF (Web Application Firewall) → Accès à la console d'administration Apache Felix → Exécution de scripts Groovy via le planificateur OpenIDM → Installation d'un servlet malveillant.
*   **Contrôle total :** L'accès au processus interne d'OpenIDM permettait de contourner les restrictions réseau et de modifier les données clients (email, mot de passe) pour usurper leur identité.
*   **Accès véhicule :** Une fois connecté au compte de la victime, les chercheurs utilisaient les APIs télématiques légitimes pour envoyer des commandes aux véhicules comme le ferait l'application mobile officielle.
*   **Rapidité de correction :** Les deux constructeurs ont remédié à la faille en moins de deux heures après le signalement.

### Vulnérabilités identifiées
*   **Contournement de WAF par normalisation de chemin :** Utilisation de caractères spéciaux (`/static%2f..;/`) pour tromper les filtres de sécurité et atteindre des routes administratives (`/system/console`) non protégées en externe.
*   **Exécution de code à distance (RCE) :** Exploitation du service de script Groovy d'OpenIDM via la configuration des tâches planifiées.
*   **Utilisation de paramètres par défaut :** Présence d'identifiants administratifs par défaut (`admin:admin`) sur la console Apache Felix.

### Recommandations
*   **Renforcement de la configuration (Hardening) :** Désactiver ou supprimer systématiquement la console d'administration Apache Felix (`/system/console`) dans les environnements de production.
*   **Sécurisation des services internes :** Ne jamais exposer les interfaces de gestion (ConfigMgr, Felix) même via des tentatives d'obscurcissement d'URL.
*   **Gestion des accès :** Modifier immédiatement les identifiants par défaut après toute installation logicielle et mettre en œuvre une authentification forte pour les interfaces d'administration.
*   **Filtrage WAF strict :** S'assurer que le WAF effectue une normalisation approfondie des URL avant l'analyse pour éviter les techniques de "path traversal" ou de détournement de servlet.
*   **Zero Trust interne :** Ne pas se reposer uniquement sur le WAF externe ; appliquer des politiques de moindre privilège aux processus internes capables d'interagir avec les bases de données d'identités (OpenIDM).

---
[Source](https://samcurry.net/forgerock){:target="_blank"}
