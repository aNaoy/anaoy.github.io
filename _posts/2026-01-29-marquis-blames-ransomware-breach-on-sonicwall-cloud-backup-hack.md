---
title: 'Marquis blames ransomware breach on SonicWall cloud backup hack'
date: 2026-01-29
permalink: /posts/2026/01/29/marquis-blames-ransomware-breach-on-sonicwall-cloud-backup-hack/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par Ransomware : Un Acteur Malveillant Exploite une Fuite de Sauvegardes SonicWall

Une société de services financiers, Marquis Software Solutions, attribue une cyberattaque par ransomware survenue en août 2025 à une faille de sécurité affectant le portail client en ligne MySonicWall de SonicWall, découverte un mois plus tard. L'incident a eu des répercussions sur des dizaines de banques et coopératives de crédit américaines.

Contrairement aux hypothèses initiales suggérant l'exploitation d'un pare-feu SonicWall non corrigé, les attaquants ont accédé aux systèmes de Marquis en utilisant des données de configuration de pare-feu volées lors d'une intrusion non autorisée dans le système de sauvegarde cloud de SonicWall.

SonicWall a initialement alerté ses clients le 17 septembre, leur demandant de réinitialiser leurs identifiants MySonicWall, et a indiqué que seulement 5 % des clients utilisant le service de sauvegarde cloud étaient affectés. Cependant, une mise à jour ultérieure a confirmé que la totalité des clients utilisant ce service avait été touchée. Une enquête a par la suite établi un lien entre cet incident et des pirates parrainés par un État. SonicWall a également précisé que cette faille était distincte d'autres attaques ciblant des comptes VPN protégés par authentification multifacteur.

**Points Clés :**

*   **Attribution de l'attaque :** Marquis Software Solutions attribue son attaque par ransomware à une faille de SonicWall.
*   **Méthode d'attaque :** Les attaquants ont utilisé des données de configuration de pare-feu dérobées via la plateforme MySonicWall de SonicWall.
*   **Impact :** L'incident a affecté des dizaines de banques et coopératives de crédit américaines via Marquis.
*   **Évolution de la communication de SonicWall :** La communication initiale de SonicWall sur l'ampleur de la brèche a été mise à jour plusieurs fois.

**Vulnérabilités :**

*   **Fuite de données de configuration de pare-feu :** Les informations de configuration des pare-feux, volées à partir des sauvegardes cloud de SonicWall, ont été exploitées.
*   **Aucun CVE spécifique n'est mentionné dans l'article.**

**Recommandations :**

*   **Réinitialisation des identifiants :** SonicWall a recommandé à ses clients de réinitialiser leurs identifiants MySonicWall.
*   **Évaluation des fournisseurs :** Marquis évalue ses options vis-à-vis de son fournisseur de pare-feu, y compris la possibilité de récupérer les dépenses engagées suite à l'incident.
*   **Sécurité des sauvegardes cloud :** Les entreprises devraient examiner la sécurité de leurs propres systèmes de sauvegarde et de leurs accès aux plateformes tierces.

---
[Source](https://www.bleepingcomputer.com/news/security/marquis-blames-ransomware-breach-on-sonicwall-cloud-backup-hack/){:target="_blank"}
