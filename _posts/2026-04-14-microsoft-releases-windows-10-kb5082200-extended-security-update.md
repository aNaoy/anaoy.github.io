---
title: 'Microsoft releases Windows 10 KB5082200 extended security update'
date: 2026-04-14
permalink: /posts/2026/04/14/microsoft-releases-windows-10-kb5082200-extended-security-update/
tags:
- veille-cyber
- bleepingcomp
---
### Mise à jour de sécurité étendue Windows 10 KB5082200

Microsoft a déployé la mise à jour KB5082200 destinée aux versions Enterprise LTSC et aux abonnés du programme ESU (Extended Security Update) de Windows 10. Cette mise à jour corrige 167 vulnérabilités recensées lors du "Patch Tuesday" d'avril 2026, incluant deux failles zero-day.

**Points clés :**
*   **Protection RDP renforcée :** Introduction de mesures contre le phishing via fichiers `.rdp`, incluant un affichage détaillé des paramètres de connexion et un avertissement de sécurité lors de l'ouverture d'un fichier.
*   **Suivi du Secure Boot :** Ajout d'indicateurs de statut dans l'application *Sécurité Windows* pour surveiller le déploiement des nouveaux certificats de démarrage sécurisé.
*   **Correctifs système :** Résolution d'un problème de connexion aux services Microsoft (ex: Teams) causé par une erreur de détection réseau, et correction d'un bug provoquant le déclenchement intempestif de la récupération BitLocker sur certains systèmes Intel après une mise à jour du *Secure Boot*.

**Vulnérabilités :**
*   Le bulletin d'avril 2026 traite 167 vulnérabilités au total, dont deux zero-days. (Note : les identifiants CVE spécifiques n'ont pas été détaillés dans le texte source).

**Recommandations :**
*   **Installation :** Les utilisateurs éligibles (Enterprise LTSC ou ESU) doivent effectuer la mise à jour manuellement via *Paramètres > Windows Update > Rechercher des mises à jour*.
*   **Vérification :** Après installation, le système passera au build 19045.7184 (ou 19044.7184 pour LTSC 2021).
*   **Sécurité :** Il est conseillé de vérifier les nouveaux indicateurs de statut dans *Sécurité Windows* pour s'assurer que les certificats *Secure Boot* sont correctement mis à jour avant l'expiration des anciens certificats prévue en juin 2026.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-windows-10-kb5082200-extended-security-update/){:target="_blank"}
