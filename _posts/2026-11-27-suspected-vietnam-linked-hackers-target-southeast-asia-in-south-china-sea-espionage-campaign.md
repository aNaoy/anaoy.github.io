---
title: 'Suspected Vietnam-Linked Hackers Target Southeast Asia in South China Sea Espionage Campaign'
date: 2026-11-27
permalink: /posts/2026/11/27/suspected-vietnam-linked-hackers-target-southeast-asia-in-south-china-sea-espionage-campaign/
tags:
- veille-cyber
- hackernews
---
### Espionnage cybernétique en Asie du Sud-Est : La campagne RedOps

Le groupe de hackers « WeaveLotus », soupçonné d'agir pour le compte du Vietnam, a mené entre août et septembre 2026 une campagne d'espionnage (« RedOps ») visant à recueillir des renseignements stratégiques sur les accords militaires en mer de Chine méridionale. Les cibles principales incluent des organisations gouvernementales, militaires et législatives en Thaïlande et aux Philippines, tandis que des activités de reconnaissance ont été observées en Indonésie.

**Points clés :**
*   **Objectif :** Exfiltration de données confidentielles pour soutenir les intérêts géopolitiques et la politique étrangère du Vietnam.
*   **Méthodologie :** Utilisation intensive d'OSINT (Bing), de tunnels SSH inversés pour maintenir la persistance, de techniques d'OCR pour scanner des images, et d'attaques par pulvérisation de mots de passe.
*   **Signes distinctifs :** Commentaires de code en vietnamien, activité alignée sur le fuseau horaire UTC+07:00 et ciblage exclusif du secteur public.

**Vulnérabilités exploitées :**
*   **CVE-2024-36401 (Score 9.8) :** Faille critique dans GeoServer permettant l'exécution de commandes à distance.
*   **CVE-2021-42235 (Score 9.8) :** Injection SQL dans osTicket permettant l'extraction de bases de données.
*   **Mauvaises configurations :** Utilisation d'identifiants par défaut (ex: `jasperadmin:jasperadmin` pour JasperReports) et mode debug exposé (Laravel).
*   **Failles applicatives :** Exploitation de serveurs Keycloak, d'APIs Directus CMS non authentifiées et usage de la procédure `xp_cmdshell` sur Microsoft SQL Server.

**Recommandations de sécurité :**
*   **Gestion des accès :** Imposer une authentification multifacteur (MFA) robuste sur tous les services exposés et supprimer systématiquement les identifiants par défaut.
*   **Durcissement des serveurs :** Désactiver les fonctionnalités inutilisées ou dangereuses comme `xp_cmdshell` et s'assurer que les modes de débogage (Laravel, etc.) sont désactivés en production.
*   **Mise à jour des systèmes :** Appliquer les correctifs de sécurité dès leur publication, particulièrement pour les logiciels open-source comme GeoServer ou osTicket.
*   **Surveillance réseau :** Détecter et bloquer les flux inhabituels, notamment les tunnels SSH inversés et les scans Nmap provenant de segments internes.
*   **Gestion des mots de passe :** Proscrire l'usage de données personnelles facilement devinables (noms, dates de naissance ou calendriers locaux) pour les mots de passe des comptes administratifs.

---
[Source](https://thehackernews.com/2026/11/suspected-vietnam-linked-hackers-target.html){:target="_blank"}
