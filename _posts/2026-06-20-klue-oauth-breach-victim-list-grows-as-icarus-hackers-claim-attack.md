---
title: 'Klue OAuth breach victim list grows as Icarus hackers claim attack'
date: 2026-06-20
permalink: /posts/2026/06/20/klue-oauth-breach-victim-list-grows-as-icarus-hackers-claim-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de Klue : Vol de données Salesforce par le groupe Icarus

La plateforme de veille commerciale Klue a subi une intrusion le 12 juin, exploitant une faille dans son infrastructure d'intégration pour compromettre les données Salesforce de nombreux clients. Le groupe de cybercriminels « Icarus » a revendiqué l'attaque et menace de publier les informations dérobées.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation d'identifiants hérités (legacy) compromis associés à un service d'intégration pour générer des jetons OAuth.
*   **Impact :** Accès non autorisé aux instances Salesforce des clients. Les données volées incluent des contacts professionnels, des communications commerciales, des tarifs et divers documents internes.
*   **Victimes :** Plusieurs entreprises majeures (notamment Recorded Future, Tanium, Jamf, Sprout Social et Gong) ont confirmé l'incident.
*   **Portée :** Les données stockées directement sur la plateforme Klue semblent intactes ; l'incident est circonscrit aux intégrations tierces.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'exploitation de **jetons OAuth détournés** et de **crédentiels obsolètes**, illustrant un défaut de gestion des accès et du cycle de vie des identifiants API.

**Recommandations :**
*   **Audit des intégrations :** Révoquer systématiquement les jetons OAuth suspects et auditer les permissions accordées aux applications tierces connectées à Salesforce (principe du moindre privilège).
*   **Surveillance :** Surveiller les logs API Salesforce pour détecter des requêtes anormales ou massives, souvent initiées par des scripts automatisés.
*   **Vigilance accrue :** Les organisations affectées doivent se préparer à une recrudescence de campagnes de phishing, d'ingénierie sociale ou de tentatives d'extorsion basées sur les données exfiltrées.
*   **Gestion des accès :** Supprimer les identifiants et comptes hérités inutilisés ou obsolètes pour réduire la surface d'attaque.

---
[Source](https://www.bleepingcomputer.com/news/security/klue-oauth-breach-victim-list-grows-as-icarus-hackers-claim-attack/){:target="_blank"}
