---
title: 'Over 24,000 exposed server BMCs leak password hash via decades-old flaw'
date: 2026-07-28
permalink: /posts/2026/07/28/over-24000-exposed-server-bmcs-leak-password-hash-via-decades-old-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique sur les BMC : plus de 24 000 serveurs exposés

Plus de 24 000 serveurs accessibles sur Internet présentent une faille de sécurité majeure au niveau de leur interface de gestion (BMC). Cette vulnérabilité permet à des attaquants de récupérer des hashs de mots de passe pour effectuer des attaques par force brute hors ligne. Le risque est exacerbé par l'utilisation fréquente de mots de passe par défaut, facilement devinables via des dictionnaires ou les étiquettes constructeurs.

**Points clés :**
*   **Risque critique :** Le compromis d'un BMC permet un accès total au matériel, l'installation de firmwares malveillants et le contrôle du serveur en dehors du système d'exploitation.
*   **Surface d'exposition :** Plus de 36 000 serveurs utilisent le protocole IPMI via le port UDP 623, dont 24 650 sont directement exploitables.
*   **Impact :** La compromission d'un seul BMC peut servir de point de pivot pour infecter tout un réseau de gestion, particulièrement dangereux dans les environnements cloud ou IA où plusieurs clients partagent des ressources physiques.
*   **Activités malveillantes :** Des preuves de demandes de rançon ont déjà été observées sur des interfaces BMC exposées (notamment HPE iLO 4).

**Vulnérabilité associée :**
*   **CVE-2013-4786 :** Faiblesse d'authentification dans IPMI 2.0 (protocole datant de 2004) permettant la récupération de données d'authentification pour des attaques hors ligne.

**Recommandations :**
*   **Isolation réseau :** Ne jamais exposer les interfaces IPMI/Redfish directement sur Internet ; utiliser des réseaux de gestion isolés.
*   **Gestion des accès :** Modifier systématiquement les mots de passe par défaut des BMC lors de la mise en service.
*   **Durcissement :** Désactiver l'authentification IPMI héritée si elle n'est pas nécessaire.
*   **Surveillance :** Appliquer une rotation régulière des identifiants d'administration pour limiter l'efficacité des attaques par dictionnaire.

---
[Source](https://www.bleepingcomputer.com/news/security/over-24-000-exposed-server-bmcs-leak-password-hash-via-decades-old-flaw/){:target="_blank"}
