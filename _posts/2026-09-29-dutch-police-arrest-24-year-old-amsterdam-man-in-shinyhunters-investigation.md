---
title: 'Dutch Police Arrest 24-Year-Old Amsterdam Man in ShinyHunters Investigation'
date: 2026-09-29
permalink: /posts/2026/09/29/dutch-police-arrest-24-year-old-amsterdam-man-in-shinyhunters-investigation/
tags:
- veille-cyber
- hackernews
---
### Arrestation liée au groupe ShinyHunters : Enquête et vulnérabilités

Les autorités néerlandaises ont arrêté Pepijn van der Stap, un homme de 24 ans soupçonné de liens avec le groupe de cybercriminels **ShinyHunters**. L'individu, actuellement responsable de la sécurité offensive chez Neo Security, avait déjà été interpellé en 2023 pour des faits similaires alors qu'il travaillait pour des entreprises de cybersécurité légitimes. De son côté, le groupe ShinyHunters dément formellement toute implication avec le suspect.

**Points clés :**
* **Arrestation :** Pepijn van der Stap a été arrêté le 15 septembre 2026 dans le cadre de l'enquête sur ShinyHunters. Son procès est prévu pour septembre 2026.
* **Contexte :** ShinyHunters a récemment revendiqué le piratage du portail de recrutement du FBI (`apply.fbijobs.gov`), affirmant qu'il s'agissait d'une campagne de communication plutôt que d'une tentative d'extorsion financière.
* **Revendication du groupe :** Le groupe assure ne pas être motivé par l'argent dans cette affaire et nie tout lien avec le suspect arrêté, qualifiant l'action de la police néerlandaise de manœuvre opportuniste.

**Vulnérabilité exploitée :**
* Le piratage a été rendu possible en contournant les règles de sécurité d'un pare-feu applicatif (WAF) protégeant contre la vulnérabilité **CVE-2026-35273** (affectant Oracle PeopleSoft). Les attaquants ont utilisé une technique d'encodage d'URL pour outrepasser les protections en place.

**Recommandations :**
* **Renforcement des WAF :** Il est impératif de s'assurer que les règles de filtrage WAF sont correctement configurées pour bloquer non seulement les signatures connues, mais aussi les tentatives de contournement par encodage (URL encoding, double encoding).
* **Mise à jour des systèmes :** Appliquer immédiatement les correctifs pour les vulnérabilités identifiées dans les plateformes de gestion comme Oracle PeopleSoft.
* **Surveillance des accès :** Maintenir une surveillance accrue sur les accès aux serveurs hébergeant des données sensibles, en particulier pour les interfaces publiques comme les portails de recrutement ou de candidatures.

---
[Source](https://thehackernews.com/2026/09/dutch-police-arrest-24-year-old.html){:target="_blank"}
