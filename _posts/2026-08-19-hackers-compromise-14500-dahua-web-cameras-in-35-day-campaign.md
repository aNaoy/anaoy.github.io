---
title: 'Hackers compromise 14,500 Dahua web cameras in 35-day campaign'
date: 2026-08-19
permalink: /posts/2026/08/19/hackers-compromise-14500-dahua-web-cameras-in-35-day-campaign/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne CameraSwarm : compromission massive de caméras Dahua

Une opération malveillante baptisée « CameraSwarm » a compromis plus de 14 500 caméras IP Dahua entre le 17 juin et le 22 juillet. Les attaquants ont exploité des vulnérabilités connues, des faiblesses d'authentification et des mécanismes de récupération de compte basés sur le numéro de série des appareils.

**Points clés :**
*   **Envergure :** 14 530 caméras compromises, principalement en Russie et en Ukraine.
*   **Méthodes d'attaque :**
    1.  Attaques par force brute sur le port TCP 37777.
    2.  Exploitation de vulnérabilités logicielles pour installer une porte dérobée persistante.
    3.  Abus des fonctionnalités cloud utilisant les numéros de série pour générer des codes de récupération sans mot de passe administrateur.
*   **Découverte :** Les chercheurs de Hunt.io ont identifié la campagne en accédant à un serveur HTTP non protégé contenant les outils, les logs et les preuves de l'attaque.

**Vulnérabilités exploitées :**
*   **CVE-2021-33044** et **CVE-2021-33045** : Utilisées pour installer le compte backdoor « p2pwn », qui survit aux changements de mot de passe et aux réinitialisations d'usine sur la plupart des firmwares.

**Recommandations :**
*   **Audit immédiat :** Vérifier la présence du compte utilisateur « p2pwn » sur les caméras Dahua et le supprimer si nécessaire.
*   **Mise à jour :** Appliquer le correctif de firmware **SA-2021-0130** (ou une version plus récente) pour neutraliser les vulnérabilités CVE-2021-33044 et CVE-2021-33045.
*   **Durcissement :** Désactiver la fonctionnalité P2P si elle n'est pas strictement nécessaire.
*   **Attention :** La simple suppression du compte backdoor ne suffit pas à invalider les codes de récupération générés par les attaquants via le mécanisme cloud ; une mise à jour globale côté serveur par Dahua est requise pour une protection complète.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-compromise-14-500-dahua-web-cameras-in-35-day-campaign/){:target="_blank"}
