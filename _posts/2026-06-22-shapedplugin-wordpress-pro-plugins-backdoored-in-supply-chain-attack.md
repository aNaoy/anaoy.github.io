---
title: 'ShapedPlugin WordPress Pro Plugins Backdoored in Supply Chain Attack'
date: 2026-06-22
permalink: /posts/2026/06/22/shapedplugin-wordpress-pro-plugins-backdoored-in-supply-chain-attack/
tags:
- veille-cyber
- hackernews
---
### Attaque par chaîne d'approvisionnement sur les plugins WordPress de ShapedPlugin

Des attaquants ont compromis le pipeline de distribution de l'éditeur ShapedPlugin, injectant un code malveillant dans les versions « Pro » de plusieurs plugins officiels. Contrairement aux versions gratuites hébergées sur WordPress.org, cette attaque a ciblé directement les clients ayant téléchargé les mises à jour via l'infrastructure de licence du vendeur.

**Points clés :**
* **Méthode :** Un chargeur malveillant est déclenché sur les pages d'administration, récupérant un payload distant qui s'installe comme un plugin fantôme.
* **Persistance et vol de données :** Le malware exfiltre des données sensibles (identifiants de base de données via `wp-config.php`, accès SMTP, données de paiement WooCommerce, comptes administrateurs) avant de s'auto-supprimer pour effacer ses traces.
* **Fonctionnalités malveillantes :** Installation de web shells, exécution de commandes arbitraires et capture de mots de passe ainsi que de codes 2FA.

**Vulnérabilités identifiées :**
* **CVE-2026-49777 (Score 10.0) :** Compromis spécifique sur *Product Slider Pro for WooCommerce*.
* **CVE-2026-10735 (Score 9.8) :** Identifiant global pour l'ensemble de l'incident.

**Plugins impactés :**
* *Product Slider Pro for WooCommerce* (versions < 3.5.4)
* *Real Testimonials Pro* (version 3.2.5)
* *Smart Post Show Pro* (versions < 4.0.2)

**Recommandations :**
* Mettre à jour immédiatement vers les versions corrigées dès leur disponibilité.
* Réinitialiser tous les mots de passe des utilisateurs (particulièrement les administrateurs).
* Révoquer et régénérer tous les secrets liés à l'authentification à deux facteurs (2FA).
* Auditer les comptes administrateurs pour détecter d'éventuels ajouts non autorisés.
* Vérifier la configuration des plugins de messagerie (SMTP) pour s'assurer qu'aucune modification des identifiants n'a été effectuée.

---
[Source](https://thehackernews.com/2026/06/shapedplugin-wordpress-pro-plugins.html){:target="_blank"}
