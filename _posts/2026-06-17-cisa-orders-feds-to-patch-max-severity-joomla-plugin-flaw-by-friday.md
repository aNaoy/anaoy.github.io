---
title: 'CISA orders feds to patch max severity Joomla plugin flaw by Friday'
date: 2026-06-17
permalink: /posts/2026/06/17/cisa-orders-feds-to-patch-max-severity-joomla-plugin-flaw-by-friday/
tags:
- veille-cyber
- bleepingcomp
---
### Urgence cybersécurité : Correction critique pour l'extension Joomla JCE

La CISA a ordonné aux agences fédérales américaines de corriger d'urgence une vulnérabilité critique affectant l'extension *Widget Factory Joomla Content Editor* (JCE), actuellement exploitée par des attaquants dans des campagnes automatisées.

**Points clés :**
* **Nature de la menace :** La faille permet à un utilisateur non authentifié d'exécuter du code PHP arbitraire, offrant un accès total au système ciblé.
* **Gravité :** Évaluée comme étant de sévérité maximale, elle fait l'objet d'exploits publics et d'attaques automatisées massives.
* **Directive CISA :** En vertu de la directive BOD 26-04, les agences fédérales doivent impérativement appliquer le correctif avant ce vendredi.

**Vulnérabilité :**
* **CVE-2026-48907 :** Problème de contrôle d'accès inapproprié permettant la création de profils d'éditeur malveillants et l'upload de code PHP par des utilisateurs non authentifiés.

**Recommandations :**
* **Mise à jour immédiate :** Installer la version **JCE Pro 2.9.99.6** ou supérieure.
* **Procédure post-compromission :** La mise à jour ne nettoie pas les fichiers déjà déposés par un attaquant. Si le site a été compromis, il est nécessaire de :
    1. Sauvegarder les profils suspects pour analyse.
    2. Supprimer les profils créés illégitimement.
    3. Réinitialiser tous les mots de passe (administrateur, base de données, hébergement).
    4. Effectuer un scan complet du serveur pour détecter et supprimer tout logiciel malveillant ou porte dérobée résiduelle.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-orders-feds-to-patch-max-severity-joomla-plugin-flaw-by-friday/){:target="_blank"}
