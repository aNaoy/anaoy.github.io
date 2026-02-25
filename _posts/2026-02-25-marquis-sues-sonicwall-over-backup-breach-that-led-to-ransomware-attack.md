---
title: 'Marquis sues SonicWall over backup breach that led to ransomware attack'
date: 2026-02-25
permalink: /posts/2026/02/25/marquis-sues-sonicwall-over-backup-breach-that-led-to-ransomware-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par Ransomware Suite à une Compromission de Sauvegarde Cloud

Une entreprise de solutions logicielles a intenté une action en justice contre un fournisseur de cybersécurité, l'accusant de négligence grave et de fausse déclaration ayant conduit à une attaque par ransomware. Cette attaque a perturbé les opérations de 74 banques américaines.

Le piratage, survenu en août 2025, a permis le vol de fichiers contenant des informations personnelles sensibles, notamment des noms, adresses, numéros de sécurité sociale et informations de compte financier. L'agresseur a compromis un pare-feu du fournisseur de cybersécurité et a utilisé des données de configuration extraites de l'infrastructure de sauvegarde cloud du vendeur.

La faille de sécurité provenait d'une modification de code d'API dans le service de sauvegarde cloud, permettant un accès non autorisé aux fichiers de sauvegarde des pare-feux, qui contenaient des identifiants chiffrés, des données de configuration et des codes de réinitialisation pour l'authentification multifacteur (MFA). L'attaque aurait été menée par des pirates parrainés par un État.

Le fournisseur de cybersécurité a divulgué l'incident avec un délai de trois semaines et a initialement estimé qu'il n'impactait qu'une petite partie de sa clientèle, avant de confirmer que tous les clients utilisant la sauvegarde cloud étaient concernés.

L'entreprise attaquée affirme que ses propres mesures de sécurité étaient à jour et que le pirate a exploité les informations exposées via la faille de la sauvegarde cloud. Elle allègue également que le fournisseur de cybersécurité a retenu des informations cruciales concernant la contournement de la MFA.

En conséquence, l'entreprise attaquée cherche à obtenir des dommages-intérêts, une indemnisation et d'autres recours, faisant état de pertes de clients, de atteinte à sa réputation et de poursuites judiciaires de masse.

**Points Clés :**

*   Une attaque par ransomware a touché 74 banques suite à une compromission de sauvegarde cloud d'un fournisseur de cybersécurité.
*   Des informations personnelles sensibles ont été volées.
*   La faille provenait d'une modification du code d'API du service de sauvegarde cloud, exposant les données de configuration des pare-feux.
*   L'attaque a été attribuée à des pirates parrainés par un État.
*   L'entreprise victime poursuit le fournisseur de cybersécurité pour négligence et fausse déclaration.

**Vulnérabilités :**

*   Faille de sécurité dans le service de sauvegarde cloud de SonicWall suite à un changement de code API en février 2025.
*   Accès non autorisé aux fichiers de sauvegarde des pare-feux stockés dans le cloud de SonicWall.
*   Exposition d'identifiants chiffrés AES-256, de données de configuration et de codes MFA.
*   (Aucune CVE spécifique n'est mentionnée dans l'article).

**Recommandations :**

*   Les clients utilisant le service de sauvegarde cloud de SonicWall ont été invités à réinitialiser leurs identifiants.
*   La nécessité de sécuriser les données de configuration des pare-feux et les informations d'identification.
*   L'importance d'une divulgation rapide et transparente des incidents de sécurité par les fournisseurs.
*   La vigilance accrue face aux potentielles attaques par des acteurs étatiques.

---
[Source](https://www.bleepingcomputer.com/news/security/marquis-sues-sonicwall-over-backup-breach-that-led-to-ransomware-attack/){:target="_blank"}
