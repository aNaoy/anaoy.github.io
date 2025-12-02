---
title: 'North Korea lures engineers to rent identities in fake IT worker scheme'
date: 2025-12-02
permalink: /posts/2025/12/02/north-korea-lures-engineers-to-rent-identities-in-fake-it-worker-scheme/
tags:
- veille-cyber
- bleepingcomp
---
Une nouvelle tactique de contournement des sanctions par la Corée du Nord

Des chercheurs en cybersécurité ont révélé que la Corée du Nord, par l'intermédiaire du groupe Lazarus et de sa faction "Famous Chollima", met en œuvre une opération complexe pour générer des fonds illicites en exploitant des ingénieurs en informatique.

Cette escroquerie consiste à recruter des développeurs qui acceptent de louer leur identité et leur matériel informatique pour permettre à des agents nord-coréens d'obtenir des emplois dans des entreprises occidentales. Les recruteurs, souvent à l'aide d'IA et de vidéos deepfake, font passer des entretiens pour le compte des véritables ingénieurs. Le "frontman" reçoit une commission variant de 20% à 35% du salaire, tandis que l'accès à son ordinateur permet aux agents nord-coréens de dissimuler leur localisation et leurs activités malveillantes. L'ingénieur compromis assume seul l'entière responsabilité des préjudices causés.

Des annonces de recrutement sont diffusées sur des plateformes comme GitHub, promettant des salaires attractifs (environ 3000 $ par mois) tout en minimisant l'importance des compétences techniques requises, le recruteur promettant une aide pour répondre aux questions d'entretien. L'objectif est d'obtenir les informations personnelles de l'ingénieur, incluant potentiellement des numéros de sécurité sociale et des informations de visa, ainsi qu'un accès à distance complet à son ordinateur, souvent via des outils comme AnyDesk et des VPN tels qu'Astrill VPN.

Les chercheurs ont utilisé des environnements simulés (honeypots) pour piéger ces recruteurs, observant l'utilisation d'outils tels que des extensions d'IA pour remplir des candidatures et répondre lors d'entretiens, le recours à des plateformes de vérification d'identité (KYC), et des techniques de reconnaissance système. L'analyse des comptes compromis a révélé des échanges avec d'autres individus impliqués dans cette opération et l'utilisation d'une équipe de plusieurs membres.

Points clés :
* Exploitation d'ingénieurs par la Corée du Nord via le groupe Lazarus ("Famous Chollima").
* Utilisation de fausses identités et d'IA (deepfake, autofill) pour obtenir des emplois dans des entreprises cibles.
* Les ingénieurs sont incités à louer leur identité et leur matériel informatique moyennant une commission.
* L'objectif est de générer des fonds pour le régime nord-coréen et de mener des activités d'espionnage.

Vulnérabilités :
* Pas de CVE spécifiques mentionnés dans l'article, mais la méthode exploite les vulnérabilités sociales (confiance, cupidité) et les lacunes dans les processus de recrutement et de vérification d'identité des entreprises.

Recommandations :
* Renforcer les processus de vérification d'identité des employés, particulièrement pour les postes à distance.
* Mettre en place des contrôles de sécurité stricts sur l'accès à distance et l'utilisation des équipements informatiques professionnels.
* Sensibiliser les employés aux risques de phishing, de social engineering et aux offres d'emploi suspectes.
* Surveiller les communications et les activités suspectes sur les plateformes de développement et de recrutement.
* Encourager le partage d'informations sur les menaces entre organisations pour anticiper les tactiques des acteurs malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/north-korea-lures-engineers-to-rent-identities-in-fake-it-worker-scheme/){:target="_blank"}
