---
title: 'Vercel confirms breach as hackers claim to be selling stolen data'
date: 2026-04-19
permalink: /posts/2026/04/19/vercel-confirms-breach-as-hackers-claim-to-be-selling-stolen-data/
tags:
- veille-cyber
- bleepingcomp
---
### Incident de sécurité chez Vercel : Compromission de données internes

La plateforme de développement cloud Vercel a confirmé une intrusion non autorisée dans ses systèmes internes. Bien que les services de la plateforme restent opérationnels, un acteur malveillant prétend détenir des données dérobées et tente de les vendre sur un forum spécialisé, évoquant une demande de rançon de 2 millions de dollars.

**Points clés**
*   **Accès non autorisé :** Des cybercriminels auraient accédé à des systèmes internes, incluant des déploiements, des clés d'API (NPM, GitHub) et du code source.
*   **Données exposées :** Un échantillon de 580 enregistrements contenant des informations d'employés (noms, emails, statuts) a été publié comme preuve.
*   **Revendication contestée :** L'auteur se revendique du groupe « ShinyHunters », bien que des membres associés à ce collectif aient démenti toute implication dans cette attaque précise.
*   **Statut de l'enquête :** Vercel a engagé des experts en réponse aux incidents et a alerté les autorités compétentes.

**Vulnérabilités**
*   Aucune CVE spécifique n'a été identifiée dans le cadre de cet incident ; il s'agit d'une intrusion directe dans les systèmes internes (compromission de comptes/accès privilégiés).

**Recommandations**
*   **Audit des variables d'environnement :** Examiner minutieusement les variables d'environnement actives sur la plateforme.
*   **Sécurisation des secrets :** Utiliser la fonctionnalité dédiée aux « Sensitive Environment Variables » de Vercel.
*   **Rotation des accès :** Procéder immédiatement à une rotation des clés d'API, des jetons GitHub et NPM, ainsi que de tout autre secret potentiellement exposé.

---
[Source](https://www.bleepingcomputer.com/news/security/vercel-confirms-breach-as-hackers-claim-to-be-selling-stolen-data/){:target="_blank"}
