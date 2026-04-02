---
title: 'Over 14,000 F5 BIG-IP APM instances still exposed to RCE attacks'
date: 2026-04-02
permalink: /posts/2026/04/02/over-14000-f5-big-ip-apm-instances-still-exposed-to-rce-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Menace persistante sur les instances F5 BIG-IP APM

Plus de 14 000 instances de F5 BIG-IP APM restent exposées en ligne, vulnérables à des attaques d'exécution de code à distance (RCE) activement exploitées. Bien que cette faille ait initialement été classée comme un problème de déni de service, sa reclassification en RCE critique a poussé la CISA à inclure le correctif dans son catalogue des vulnérabilités connues exploitées (KEV).

**Points clés :**
*   **Vulnérabilité :** CVE-2025-53521.
*   **Nature du risque :** Permet à un attaquant non authentifié d'exécuter du code à distance sur les systèmes BIG-IP APM disposant de politiques d'accès configurées sur un serveur virtuel.
*   **Situation :** Malgré les alertes de sécurité, plus de 14 000 équipements restent accessibles publiquement, selon les données de Shadowserver.
*   **Impact :** Historiquement, les failles sur les solutions F5 sont ciblées par des groupes cybercriminels et des États-nations pour infiltrer des réseaux d'entreprise, dérober des données ou installer des malwares persistants.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer les correctifs fournis par F5, qui adressent désormais officiellement le vecteur RCE.
*   **Audit de sécurité :** Vérifier les journaux, les disques et l'historique des terminaux à la recherche d'indicateurs de compromission (IOC) fournis par l'éditeur.
*   **Réinstallation recommandée :** En cas de suspicion de compromission, F5 préconise de reconstruire intégralement le système à partir d'une source saine. Les sauvegardes de configuration (UCS) risquent de contenir des malwares persistants et ne doivent pas être utilisées pour restaurer un système potentiellement corrompu.

---
[Source](https://www.bleepingcomputer.com/news/security/over-14-000-f5-big-ip-apm-instances-still-exposed-to-rce-attacks/){:target="_blank"}
