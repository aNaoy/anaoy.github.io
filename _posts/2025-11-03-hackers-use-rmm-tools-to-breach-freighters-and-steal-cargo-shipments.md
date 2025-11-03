---
title: 'Hackers use RMM tools to breach freighters and steal cargo shipments'
date: 2025-11-03
permalink: /posts/2025/11/03/hackers-use-rmm-tools-to-breach-freighters-and-steal-cargo-shipments/
tags:
- veille-cyber
- bleepingcomp
---
### Piratage de cargaisons grâce aux outils RMM

Des groupes de cybercriminels ciblent des courtiers en fret et des transporteurs routiers en utilisant des liens et des emails malveillants pour déployer des outils de surveillance et de gestion à distance (RMM). Ces outils permettent aux attaquants de prendre le contrôle de systèmes informatiques, de détourner des chargements et de voler des marchandises physiques. Ces campagnes, observées depuis janvier, se multiplient depuis août, envoyant des milliers de messages. Les cibles sont principalement en Amérique du Nord, mais des activités similaires ont été signalées dans plusieurs autres pays.

Le vol de cargaison, qui représente des milliards de dollars de pertes annuelles aux États-Unis, exploite désormais les failles numériques de la chaîne d'approvisionnement. Les criminels cherchent à installer des RMM comme ScreenConnect, SimpleHelp, PDQ Connect, Fleetdeck, N-able, et LogMeIn Resolve pour obtenir un contrôle total, effectuer de la reconnaissance et voler des identifiants. Ils parviennent à leurs fins en utilisant des comptes compromis sur des plateformes de fret pour publier de fausses annonces, ou en piratant des emails de courtiers et de répartiteurs pour rediriger les victimes vers des URL malveillants.

Ces attaques s'appuient sur l'ingénierie sociale, utilisant des messages d'urgence pour la négociation de fret et exploitant la confiance dans les documents de transport. Les pages de phishing, bien conçues et imitant les marques des transporteurs légitimes, incitent au téléchargement de fichiers exécutables ou de fichiers MSI qui installent les outils RMM. Ces derniers permettent ensuite aux attaquants de modifier les réservations, de bloquer les notifications, d'ajouter leurs propres appareils aux extensions téléphoniques des répartiteurs et de réserver des chargements sous l'identité de l'entreprise piratée. Les RMM sont parfois utilisés conjointement, par exemple, PDQ Connect peut installer ScreenConnect et SimpleHelp. Après l'accès initial, des outils de récolte d'informations comme WebBrowserPassView sont déployés.

Ces attaques démontrent une connaissance précise des itinéraires, des horaires et des types de cargaisons à haute valeur, suggérant une collaboration avec des groupes du crime organisé. Les cargaisons volées, comprenant des denrées alimentaires, des boissons et de l'électronique, sont interceptées ou réacheminées puis vendues en ligne ou expédiées à l'étranger. Des logiciels espions tels que NetSupport, DanaBot, Lumma Stealer et StealC ont également été utilisés dans des activités connexes.

**Points Clés :**

*   Les attaquants exploitent les outils RMM pour le vol de cargaisons.
*   L'ingénierie sociale et la compromission des emails sont des vecteurs d'attaque courants.
*   Les RMM permettent un contrôle total des systèmes compromis, la modification des réservations et l'usurpation d'identité.
*   Les attaquants possèdent des informations détaillées sur les opérations logistiques.
*   Il existe une possible collaboration avec des groupes du crime organisé.

**Vulnérabilités (sans CVE spécifiques mentionnées dans l'article) :**

*   Manque de sécurité dans la gestion des emails et des pièces jointes.
*   Vulnérabilité à l'ingénierie sociale exploitant la confiance et l'urgence.
*   Absence de contrôle sur l'installation d'outils RMM légitimes mais mal utilisés.
*   Faiblesses dans la sécurisation des plateformes de fret et des communications inter-entreprises.

**Recommandations :**

*   Restreindre l'installation d'outils RMM non approuvés.
*   Surveiller l'activité du réseau.
*   Bloquer les pièces jointes .EXE et .MSI au niveau de la passerelle email.
*   Mettre en place des contrôles d'accès stricts et une authentification forte.
*   Sensibiliser le personnel aux risques de phishing et d'ingénierie sociale.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-use-rmm-tools-to-breach-freighters-and-steal-cargo-shipments/){:target="_blank"}
