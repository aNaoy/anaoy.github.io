---
title: 'Microsoft releases Windows 10 KB5075912 extended security update'
date: 2026-02-11
permalink: /posts/2026/02/11/microsoft-releases-windows-10-kb5075912-extended-security-update/
tags:
- veille-cyber
- bleepingcomp
---
**Mise à jour de sécurité étendue pour Windows 10 : Renforcement contre les vulnérabilités**

Une mise à jour de sécurité étendue, désignée par le code KB5075912, a été publiée pour Windows 10. Cette mise à jour vise à corriger des failles de sécurité découvertes lors du "Patch Tuesday" de février 2026, incluant six vulnérabilités zero-day, et à poursuivre le déploiement de certificats Secure Boot de remplacement dont l'expiration est imminente.

Les systèmes concernés par cette mise à jour sont les versions Enterprise LTSC de Windows 10 ainsi que les machines inscrites au programme ESU (Extended Security Updates). L'installation s'effectue via Windows Update dans les paramètres du système. Après l'application, Windows 10 atteindra la version 19045.6937, et Windows 10 Enterprise LTSC 2021 la version 19044.6937.

**Points clés et Corrections :**

*   **Absence de nouvelles fonctionnalités :** La mise à jour KB5075912 ne contient que des correctifs de sécurité et des résolutions de bugs issus de mises à jour antérieures, le développement de nouvelles fonctionnalités pour Windows 10 étant terminé.
*   **Correction de 58 vulnérabilités :** Au total, 58 failles de sécurité ont été corrigées, dont six exploités activement sans connaissance préalable ("zero-days").
*   **Résolution d'un problème de démarrage/hibernation :** Un dysfonctionnement connu qui empêchait certains PC compatibles avec Secure Launch et ayant le mode sécurisé virtuel (VSM) activé de s'éteindre ou d'entrer en hibernation (redémarrant à la place) a été résolu.
*   **Mise à jour des certificats Secure Boot :** Dans le cadre de cette mise à jour, Microsoft continue de déployer de nouveaux certificats Secure Boot, essentiels pour la validation des composants de démarrage de Windows et des chargeurs de démarrage tiers. Ceci est crucial car plusieurs certificats Secure Boot datant de 2011 expireront en juin 2026, ce qui pourrait compromettre les protections si non mis à jour.
*   **Corrections mineures :** Des ajustements ont été apportés aux polices chinoises pour la conformité GB18030-2022A, ainsi qu'à la gestion du renommage de dossiers avec le fichier desktop.ini et à la stabilité de certains GPU.

**Vulnérabilités :**

L'article mentionne la correction de six vulnérabilités "zero-day" activement exploitées, mais les identifiants CVE spécifiques ne sont pas détaillés dans le texte. Il est également fait référence à la résolution d'un problème lié à Secure Launch et VSM qui pouvait affecter la fonction d'arrêt ou d'hibernation, bien que cela soit présenté comme un "problème connu" plutôt qu'une vulnérabilité CVE spécifique.

**Recommandations :**

*   Installer la mise à jour KB5075912 pour Windows 10, particulièrement pour les utilisateurs des versions Enterprise LTSC et du programme ESU.
*   Vérifier manuellement les mises à jour via "Paramètres" > "Windows Update" > "Vérification des mises à jour".
*   S'assurer que les certificats Secure Boot sont à jour pour maintenir l'intégrité des protections de démarrage.

Aucun problème connu n'est signalé par Microsoft concernant cette mise à jour.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-releases-windows-10-kb5075912-extended-security-update/){:target="_blank"}
