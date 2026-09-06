---
title: 'Attackers Hijack MikroTik Routers Through Internet-Exposed SSH Without Authentication'
date: 2026-09-06
permalink: /posts/2026/09/06/attackers-hijack-mikrotik-routers-through-internet-exposed-ssh-without-authentication/
tags:
- veille-cyber
- hackernews
---
### Exploitation active de vulnérabilités sur les routeurs MikroTik RouterOS

Des attaquants exploitent actuellement une chaîne de deux vulnérabilités (surnommée « MikroTrick ») dans le système RouterOS de MikroTik. Cette faille permet d'obtenir un contrôle administratif complet sur les routeurs via le service SSH, si celui-ci est exposé directement sur Internet.

**Points clés :**
*   **Vecteur d'attaque :** Accès non authentifié via le service SSH exposé sur le réseau public.
*   **Impact :** Compromission totale de l'appareil par les attaquants.
*   **Indicateurs de compromission :** Apparition de comptes administrateurs suspects, présence de journaux d'activité contenant `ssh:-2@`, ou déclenchement du mode « Flagged » par le système après une détection de configuration non autorisée.

**Vulnérabilités :**
*   Bien que le nom spécifique des CVE ne soit pas explicitement détaillé dans le rapport, la faille repose sur l'enchaînement de deux vulnérabilités non documentées au moment de la publication, affectant de nombreuses versions de RouterOS (v6.x et v7.x).

**Recommandations :**
*   **Mise à jour immédiate :** Installer les versions correctives fournies par MikroTik :
    *   Série 6.x : vers la version **6.49.21**.
    *   Série 7.x : vers la version **7.23.5** (branche Long-term) ou **7.24.2** (branche Stable).
*   **Sécurisation immédiate :** Si la mise à jour n'est pas possible, désactiver les services exposés sur Internet (SSH, WWW, bandwidth-test) ou restreindre leur accès à des réseaux de gestion de confiance.
*   **Audit après mise à jour :** Inspecter minutieusement les logs et la configuration à la recherche d'utilisateurs, de scripts ou de modifications non autorisés.
*   **Procédure de récupération :** En cas de compromission avérée, isoler le routeur, exporter les logs/configurations pour analyse (sans effacer le statut « Flagged »), réinitialiser l'appareil aux paramètres d'usine, et renouveler l'ensemble des mots de passe et clés cryptographiques. Ne pas restaurer une sauvegarde complète provenant d'un équipement compromis.

---
[Source](https://thehackernews.com/2026/09/attackers-hijack-mikrotik-routers.html){:target="_blank"}
