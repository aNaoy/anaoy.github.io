---
title: 'Over 20,000 Instagram accounts stolen in Meta AI support hack'
date: 2026-06-08
permalink: /posts/2026/06/08/over-20000-instagram-accounts-stolen-in-meta-ai-support-hack/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement massif de comptes Instagram via l'IA de support Meta

Plus de 20 000 comptes Instagram ont été piratés suite à l'exploitation d'une faille dans l'outil de support automatisé par IA de Meta, le *High Touch Support* (HTS). 

**Points clés :**
* **Mécanisme d'attaque :** L'outil HTS permettait aux utilisateurs de demander une réinitialisation de mot de passe par e-mail. Une vulnérabilité dans le code empêchait la vérification de la correspondance entre l'e-mail fourni et celui associé au compte Instagram.
* **Conséquences :** Les attaquants pouvaient demander un lien de réinitialisation pour n'importe quel compte et en prendre le contrôle, à condition que l'authentification à deux facteurs (2FA) ne soit pas activée.
* **Données exposées :** Les attaquants ont potentiellement accédé aux informations de contact, messages privés, photos, vidéos, historiques d'activité et aux services liés aux comptes.

**Vulnérabilités :**
* **Défaut de validation des entrées (Improper Verification) :** Le système de réinitialisation ne vérifiait pas l'association entre l'e-mail du demandeur et le compte cible. 
* *Note : Aucune CVE spécifique n'a été attribuée à cette faille logicielle propriétaire interne.*

**Recommandations :**
* **Pour les utilisateurs :** Activer systématiquement l'authentification à deux facteurs (2FA) pour protéger les comptes contre les réinitialisations de mot de passe non autorisées.
* **Pour Meta :**
    * Correction immédiate du flux de validation dans l'outil de récupération de compte.
    * Audit complet des processus de support automatisé sur l'ensemble des plateformes de l'entreprise.
    * Renforcement des checkpoints de sécurité pour les comptes potentiellement compromis (réinitialisation forcée des mots de passe).

---
[Source](https://www.bleepingcomputer.com/news/security/meta-ai-support-data-breach-affects-20-000-instagram-accounts/){:target="_blank"}
