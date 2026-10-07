---
title: 'Microsoft Outlook to block MSIX attachments starting November'
date: 2026-10-07
permalink: /posts/2026/10/07/microsoft-outlook-to-block-msix-attachments-starting-november/
tags:
- veille-cyber
- bleepingcomp
---
### Renforcement de la sécurité : Outlook bloque les fichiers MSIX

Dès le mois de novembre 2025, Microsoft déploiera une mise à jour visant à bloquer par défaut les pièces jointes aux formats `.msix` et `.msixbundle` dans Outlook sur le web ainsi que dans la nouvelle version d'Outlook pour Windows. Cette mesure préventive s'inscrit dans une stratégie globale visant à limiter l'exploitation de vecteurs d'attaque courants par des acteurs malveillants.

**Points clés :**
*   **Déploiement :** La mise à jour débutera début novembre pour atteindre une disponibilité générale à la mi-novembre.
*   **Impact :** Les utilisateurs ne pourront plus envoyer, recevoir, ouvrir ou télécharger ces types de fichiers.
*   **Contexte :** Cette décision fait suite à des mesures similaires prises récemment par Microsoft, notamment le blocage des fichiers `.library-ms`, `.search-ms` et le filtrage des images SVG intégrées, tous utilisés pour des campagnes de phishing et de distribution de malwares.
*   **Vulnérabilités :** Aucun identifiant CVE spécifique n'est associé à cette mesure, car il s'agit d'une réduction proactive de la surface d'attaque visant à prévenir l'utilisation abusive des formats d'installation Windows dans des scénarios malveillants.

**Recommandations :**
*   **Audit :** La plupart des organisations ne devraient pas être impactées par cette modification en raison de la faible utilisation de ces formats. Les administrateurs doivent vérifier si leurs flux de travail légitimes dépendent de ces extensions.
*   **Gestion des exceptions :** Si l'utilisation de fichiers `.msix` ou `.msixbundle` est requise pour des besoins métiers, les administrateurs informatiques peuvent ajouter ces extensions à la liste `AllowedFileTypes` au sein des objets `OwaMailboxPolicy` de leur tenant pour outrepasser le blocage par défaut.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-outlook-to-block-msix-attachments-used-in-attacks/){:target="_blank"}
