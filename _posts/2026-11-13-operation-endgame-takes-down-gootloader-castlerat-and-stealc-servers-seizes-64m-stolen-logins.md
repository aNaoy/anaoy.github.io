---
title: 'Operation Endgame Takes Down Gootloader, CastleRAT and StealC Servers, Seizes 6.4M Stolen Logins'
date: 2026-11-13
permalink: /posts/2026/11/13/operation-endgame-takes-down-gootloader-castlerat-and-stealc-servers-seizes-64m-stolen-logins/
tags:
- veille-cyber
- hackernews
---
### Opération Endgame : Démantèlement de réseaux cybercriminels majeurs

Une opération policière internationale, baptisée "Operation Endgame", a neutralisé les infrastructures des logiciels malveillants **Gootloader**, **CastleRAT** et **StealC**. Cette intervention a permis de saisir 235 serveurs, 257 noms de domaine et plus de 6,4 millions d'identifiants volés.

**Points clés :**
*   **Gootloader :** Utilisé pour le déploiement de ransomwares via l'empoisonnement SEO et des faux documents juridiques sur des sites WordPress piratés.
*   **CastleRAT :** Un cheval de Troie d'accès à distance (RAT) permettant un contrôle total des machines infectées.
*   **StealC :** Un logiciel de vol d'informations (infostealer) ciblant les identifiants de connexion.
*   **Impact :** Des millions d'ordinateurs infectés depuis 2020 et des dizaines de millions de dollars de pertes liées aux ransomwares.

**Vulnérabilités exploitées :**
L'article ne mentionne pas de CVE spécifique, mais souligne que les attaquants compromettent les sites web principalement via :
*   Des mots de passe administrateur faibles ou compromis.
*   Des vulnérabilités dans les thèmes et plugins WordPress non mis à jour.
*   L'absence d'authentification multifacteur (MFA).

**Recommandations pour les propriétaires de sites WordPress :**
*   **Authentification :** Implémenter l'authentification multifacteur (MFA) et utiliser des mots de passe uniques et complexes (au moins 12 caractères).
*   **Maintenance :** Mettre à jour systématiquement WordPress, ses thèmes et ses extensions. Supprimer les comptes administrateur suspects ou inutilisés.
*   **Sécurisation :** Restreindre l'accès à la page `/wp-admin` aux adresses IP approuvées uniquement.
*   **Nettoyage :** Supprimer tout code de porte dérobée (backdoor) identifié sur les sites compromis.

**Vérification pour les victimes :**
Les utilisateurs peuvent vérifier si leurs données ont été compromises via le service néerlandais [Check your hack](https://www.politie.nl/en/information/checkyourhack.html) ou via des plateformes comme *Have I Been Pwned*. Attention aux tentatives de phishing : la police n'envoie jamais de liens directs par e-mail pour ce type de vérification.

---
[Source](https://thehackernews.com/2026/11/operation-endgame-takes-down-gootloader.html){:target="_blank"}
