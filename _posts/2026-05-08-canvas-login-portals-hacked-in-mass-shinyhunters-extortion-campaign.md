---
title: 'Canvas login portals hacked in mass ShinyHunters extortion campaign'
date: 2026-05-08
permalink: /posts/2026/05/08/canvas-login-portals-hacked-in-mass-shinyhunters-extortion-campaign/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne d'extorsion massive par le groupe ShinyHunters contre Canvas

Le groupe de cybercriminels **ShinyHunters** a mené une nouvelle attaque contre Instructure, l'éditeur de la plateforme éducative Canvas. Les assaillants ont exploité une vulnérabilité système pour défigurer les portails de connexion de plus de 330 établissements d'enseignement, affichant un message de rançon menaçant de divulguer des données volées si un paiement n'est pas effectué avant le 12 mai 2026. Cette action fait suite à une compromission plus large ayant potentiellement exposé les enregistrements de 280 millions d'utilisateurs.

**Points clés :**
*   **Portée :** Environ 330 universités et établissements scolaires impactés par la défiguration des portails et de l'application Canvas.
*   **Mode opératoire :** Utilisation d'une vulnérabilité permettant de modifier les pages de connexion pour afficher un message d'extorsion.
*   **Contexte :** Cette attaque s'inscrit dans une compromission majeure impliquant le vol massif de données (messages privés, informations d'inscription, données de scolarité).
*   **Réponse d'Instructure :** L'entreprise a mis ses portails hors ligne pour tenter de contrer l'attaque, mais reste critiquée pour son manque de transparence sur la notification des victimes.

**Vulnérabilités :**
*   Aucune CVE spécifique n'a été publiée à ce jour concernant le vecteur exact utilisé pour la modification des portails, Instructure n'ayant pas encore détaillé la faille exploitée.

**Recommandations :**
*   **Pour les établissements :** Maintenir une surveillance accrue des logs d'accès et se préparer à une potentielle divulgation publique de données d'étudiants.
*   **Bonnes pratiques générales face au groupe ShinyHunters :**
    *   Renforcer la protection des accès via Single Sign-On (SSO) en évitant le recours exclusif aux SMS pour le MFA.
    *   Se protéger contre les attaques de type *vishing* (phishing vocal) ciblant le support technique pour usurper des sessions de connexion.
    *   Surveiller étroitement les accès aux environnements SaaS et aux intégrations tierces, vecteurs privilégiés par ce groupe.
    *   Ne jamais céder aux demandes de rançon et consulter des firmes spécialisées en cybersécurité pour gérer la réponse aux incidents.

---
[Source](https://www.bleepingcomputer.com/news/security/canvas-login-portals-hacked-in-mass-shinyhunters-extortion-campaign/){:target="_blank"}
