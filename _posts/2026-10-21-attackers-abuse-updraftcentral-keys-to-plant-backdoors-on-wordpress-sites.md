---
title: 'Attackers Abuse UpdraftCentral Keys to Plant Backdoors on WordPress Sites'
date: 2026-10-21
permalink: /posts/2026/10/21/attackers-abuse-updraftcentral-keys-to-plant-backdoors-on-wordpress-sites/
tags:
- veille-cyber
- hackernews
---
### Compromission des clés UpdraftCentral : Campagne de portes dérobées sur WordPress

Une intrusion sur les serveurs de TeamUpdraft a permis à des attaquants de dérober les clés de connexion des services UpdraftCentral, UpdraftVault et UpdraftClone. En exploitant ces clés valides, les pirates ont pu envoyer des commandes distantes aux sites WordPress connectés afin d'installer des extensions malveillantes agissant comme des portes dérobées (backdoors).

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de clés API légitimes pour injecter des plugins malveillants via le canal RPC distant d'UpdraftPlus.
*   **Impact :** Création de comptes administrateurs factices, exécution de code arbitraire et persistance après la suppression du plugin malveillant.
*   **Vulnérabilité connexe :** Rappel de la vulnérabilité **CVE-2026-10795** (CVSS 8.1), permettant une falsification de commandes sans clé, qui souligne la nécessité de maintenir le plugin à jour.

**Indicateurs de compromission :**
*   **Comptes suspects :** `system_team850`, `web.tech988`, `cmseditor170`, etc.
*   **Plugins malveillants :** Noms variés comme "Site Health Cache", "Asset Forge 2" ou "Style Bridge 8F5".
*   **Adresses IP :** `43.250.53.42` et `2a09:bac5:4e21:2e3c::49b:9`.

**Recommandations pour les administrateurs :**
1.  **Mise à jour :** Installer immédiatement UpdraftPlus version 1.26.13 (gratuit) ou 2.26.13 (Premium).
2.  **Nettoyage :** Supprimer tout compte utilisateur ou plugin non reconnu, en vérifiant particulièrement l'onglet "Must-Use" des extensions.
3.  **Réinitialisation :** Supprimer la clé de connexion UpdraftCentral actuelle dans les outils avancés du plugin, puis reconnecter le service pour générer une nouvelle clé.
4.  **Sécurité des accès :** Modifier les mots de passe de tous les comptes administrateurs et activer l'authentification à deux facteurs (2FA).
5.  **Audit :** En cas de doute sur l'intégrité du site, restaurer une sauvegarde antérieure au 17 octobre 2026.

---
[Source](https://thehackernews.com/2026/10/attackers-abuse-updraftcentral-keys-to.html){:target="_blank"}
