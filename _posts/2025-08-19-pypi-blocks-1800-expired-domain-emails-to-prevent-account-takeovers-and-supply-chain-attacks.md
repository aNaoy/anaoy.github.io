---
title: 'PyPI Blocks 1,800 Expired-Domain Emails to Prevent Account Takeovers and Supply Chain Attacks'
date: 2025-08-19
permalink: /posts/2025/08/19/pypi-blocks-1800-expired-domain-emails-to-prevent-account-takeovers-and-supply-chain-attacks/
tags:
- veille-cyber
- hackernews
---
### PyPI Renforce la Sécurité pour Prévenir les Compagnies de Domaines Expirés

Le dépôt Python Package Index (PyPI) a implémenté une nouvelle mesure de sécurité visant à contrer les attaques par résurrection de domaines. Cette initiative bloque les adresses e-mail associées à des domaines expirés, empêchant ainsi les acteurs malveillants de prendre le contrôle de comptes PyPI via des réinitialisations de mot de passe.

Depuis début juin 2025, PyPI a désactivé plus de 1 800 adresses e-mail dont les domaines sont entrés en phase d'expiration. Ce mécanisme vise à endiguer un vecteur d'attaque important et potentiellement difficile à détecter, surtout pour les paquets open-source abandonnés mais toujours largement utilisés.

Le risque survient lorsque les domaines enregistrés par les mainteneurs de paquets expirent. Si un attaquant acquiert ensuite ce domaine, il peut intercepter les e-mails de réinitialisation de mot de passe et accéder au compte. Un cas notable s'est produit en 2022 avec le paquet `ctx`, où un attaquant a utilisé cette technique pour publier des versions non autorisées.

Cette protection s'applique spécifiquement aux comptes utilisant des adresses e-mail associées à des noms de domaine personnalisés. PyPI utilise l'API Status de Fastly pour vérifier le statut des domaines tous les 30 jours et désactiver les adresses correspondantes si le domaine a expiré.

**Points Clés :**

*   **Objectif :** Prévenir les prises de contrôle de compte et les attaques sur la chaîne d'approvisionnement par le biais de domaines expirés.
*   **Mécanisme :** Désactivation des adresses e-mail liées à des domaines expirés.
*   **Impact :** Plus de 1 800 adresses désactivées depuis début juin 2025.
*   **Technologie utilisée :** API Status de Fastly pour la vérification des domaines.
*   **Vulnérabilité ciblée :** Prise de contrôle de compte (ATO) via la réinitialisation de mot de passe sur des domaines expirés, y compris pour les comptes avec authentification à deux facteurs (2FA).
*   **Cas d'usage :** Attaques sur les comptes PyPI utilisant des adresses e-mail avec des domaines personnalisés.

**Recommandations :**

*   **Activer l'authentification à deux facteurs (2FA).**
*   **Ajouter une adresse e-mail de secours vérifiée** provenant d'un domaine majeur (comme Gmail ou Outlook) si le compte ne possède qu'une seule adresse e-mail vérifiée associée à un domaine personnalisé.

---
[Source](https://thehackernews.com/2025/08/pypi-blocks-1800-expired-domain-emails.html){:target="_blank"}
