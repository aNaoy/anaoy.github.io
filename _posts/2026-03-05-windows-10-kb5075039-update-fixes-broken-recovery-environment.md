---
title: 'Windows 10 KB5075039 update fixes broken Recovery Environment'
date: 2026-03-05
permalink: /posts/2026/03/05/windows-10-kb5075039-update-fixes-broken-recovery-environment/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour de l'environnement de récupération Windows 10**

Microsoft a publié la mise à jour KB5075039 pour corriger un problème persistant qui empêchait l'accès à l'environnement de récupération Windows (WinRE) sur Windows 10. Cet environnement est essentiel pour le dépannage, la réparation du système d'exploitation et la suppression de logiciels malveillants.

**Points clés :**

*   La mise à jour KB5075039 résout un problème où WinRE ne démarrait pas correctement après l'installation de la mise à jour KB5068164 d'octobre 2025.
*   Ce problème affectait l'environnement de récupération Windows 10.
*   Une pré-condition pour installer cette mise à jour est que la partition WinRE doit avoir une taille minimale de 256 Mo.

**Vulnérabilités :**

*   **Problème non spécifié dans l'article sous forme de CVE :** L'article mentionne un dysfonctionnement de l'environnement de récupération suite à une mise à jour précédente (KB5068164), mais sans fournir de numéro CVE spécifique pour cette faille.

**Recommandations :**

*   Installer la mise à jour KB5075039 pour corriger le problème d'accès à WinRE.
*   S'assurer que la partition WinRE dispose d'une taille d'au moins 256 Mo. Si ce n'est pas le cas, il faut l'agrandir en suivant les instructions fournies par Microsoft (lien donné dans l'article).
*   Il est conseillé de sauvegarder les données avant toute opération de redimensionnement de partition.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/windows-10-kb5075039-update-fixes-broken-recovery-environment/){:target="_blank"}
