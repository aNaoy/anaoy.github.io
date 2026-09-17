---
title: 'Brevo supply-chain attack injected ClickFix scripts on customer sites'
date: 2026-09-17
permalink: /posts/2026/09/17/brevo-supply-chain-attack-injected-clickfix-scripts-on-customer-sites/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par chaîne d'approvisionnement via Brevo : Injection de scripts ClickFix

Brevo a été victime d'une attaque par chaîne d'approvisionnement le 14 septembre, où des attaquants ont utilisé une clé d'API Cloudflare piratée pour injecter des scripts malveillants via un Cloudflare Worker. Cette manipulation a permis de modifier dynamiquement le contenu diffusé aux utilisateurs finaux sans altérer les serveurs d'origine, contournant ainsi les contrôles d'intégrité standards.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'une clé d'API Cloudflare à privilèges élevés, codée en dur dans le code source de l'application.
*   **Impact :** Environ 100 000 sites web utilisant les widgets ou SDK Brevo ont été touchés pendant environ 5 heures et demie.
*   **Méthodologie :** Les visiteurs étaient redirigés vers de fausses pages de vérification Cloudflare (attaques "ClickFix"). Pour les administrateurs WordPress, une extension malveillante ("Web Media Optimizer") était proposée, créant une porte dérobée persistante permettant de générer des sessions administrateur sans mot de passe.
*   **Indicateurs :** L'attaque a supprimé les en-têtes de sécurité (Content-Security-Policy) lors du processus de réécriture à la périphérie (edge) du réseau.

**Vulnérabilités :**
*   **Exposition de secrets :** Stockage de clés d'API sensibles en clair dans le code source (*Hardcoded credentials*).
*   **Permis excessifs :** Utilisation d'une clé d'API avec des droits administrateur complets pour des fonctions limitées.

**Recommandations :**
*   **Audit immédiat (WordPress) :** Les administrateurs ayant accédé à un site affecté le 14 septembre doivent vérifier la présence d'extensions suspectes, les supprimer et réinitialiser les mots de passe administrateur.
*   **Gestion des secrets :** Ne jamais coder en dur des clés d'API ; utiliser des gestionnaires de secrets ou des variables d'environnement sécurisées.
*   **Principe du moindre privilège :** Restreindre strictement les permissions des clés d'API Cloudflare au périmètre minimal nécessaire.
*   **Surveillance :** Mettre en place des alertes sur la création ou la modification de "Cloudflare Workers" et de routes DNS non autorisées.

---
[Source](https://www.bleepingcomputer.com/news/security/brevo-supply-chain-attack-injected-clickfix-scripts-on-customer-sites/){:target="_blank"}
