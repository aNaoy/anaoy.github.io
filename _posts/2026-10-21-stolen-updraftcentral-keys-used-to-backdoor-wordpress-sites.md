---
title: 'Stolen UpdraftCentral keys used to backdoor WordPress sites'
date: 2026-10-21
permalink: /posts/2026/10/21/stolen-updraftcentral-keys-used-to-backdoor-wordpress-sites/
tags:
- veille-cyber
- bleepingcomp
---
# Compromission des clés UpdraftCentral : vague d'attaques sur WordPress

La plateforme TeamUpdraft a subi une intrusion dans son infrastructure, permettant à des attaquants d'accéder à la base de données clients. Cette brèche expose potentiellement 400 000 sites utilisant UpdraftCentral, via l'utilisation de clés de connexion légitimes pour injecter des backdoors.

**Points clés**
* **Accès malveillant :** Les attaquants utilisent des clés de connexion volées pour envoyer des commandes à distance, contournant les protections serveurs classiques.
* **Impact :** Installation de plugins malveillants déguisés (ex: "Site Health Cache"), création de comptes administrateurs factices et exécution de code arbitraire.
* **Données compromises :** Hashes de mots de passe, paramètres 2FA, et clés de service pour UpdraftCentral, UpdraftVault et UpdraftClone.

**Vulnérabilités associées**
* **CVE-2026-10795 :** Vulnérabilité précédemment patchée, mais ici non exploitée, car l'attaque utilise des jetons d'authentification valides via le canal de gestion à distance.
* **Défaut de remédiation :** Un bug dans les versions 1.26.12/2.26.12 a empêché la suppression effective des clés compromises, facilitant la persistance des attaques.

**Recommandations**
* **Mise à jour immédiate :** Passer à la version **1.26.13 (version gratuite) ou 2.26.13 (version Premium)** ou supérieure.
* **Nettoyage des clés :** Après mise à jour, supprimer manuellement les clés de connexion existantes via : *Réglages → UpdraftPlus Backups → Outils avancés → UpdraftCentral → Gérer les clés*.
* **Sécurisation des comptes :** Réinitialiser le mot de passe du compte TeamUpdraft, révoquer toutes les sessions actives et configurer à nouveau le double facteur (2FA).
* **Audit de sécurité :** Inspecter les sites à la recherche de nouveaux comptes administrateurs suspects ou de plugins non autorisés, et restaurer les sites compromis à partir de sauvegardes saines.

---
[Source](https://www.bleepingcomputer.com/news/security/stolen-updraftcentral-keys-used-to-backdoor-wordpress-sites/){:target="_blank"}
