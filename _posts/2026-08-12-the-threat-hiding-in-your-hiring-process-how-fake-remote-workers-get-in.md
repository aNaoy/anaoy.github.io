---
title: 'The Threat Hiding in Your Hiring Process: How Fake Remote Workers Get In'
date: 2026-08-12
permalink: /posts/2026/08/12/the-threat-hiding-in-your-hiring-process-how-fake-remote-workers-get-in/
tags:
- veille-cyber
- bleepingcomp
---
### La menace des faux travailleurs distants dans le processus de recrutement

Les entreprises sont de plus en plus ciblées par des fraudeurs, notamment des travailleurs nord-coréens, qui usurpent des identités pour obtenir des emplois en télétravail. Une fois en poste, ils utilisent leur accès légitime pour exfiltrer des données propriétaires, voler du code source ou mener des activités d'extorsion.

**Points clés :**
*   **Stratégie sophistiquée :** Les attaquants exploitent les failles des processus de vérification traditionnels en combinant de faux CV, des documents falsifiés et l'usage de l'IA pour créer des profils crédibles.
*   **Infrastructure de fraude :** Utilisation de "fermes d'ordinateurs" où des facilitateurs locaux reçoivent le matériel informatique de l'entreprise, permettant aux fraudeurs à l'étranger de piloter les accès à distance via VPN ou logiciels de prise de contrôle.
*   **Risque métier :** Le simple contrôle des antécédents ne garantit pas que la personne interviewée est celle qui utilise réellement la machine au quotidien.

**Vulnérabilités :**
Cet article ne cite pas de CVE spécifique, car il s'agit d'une menace basée sur l'ingénierie sociale et le contournement de processus métier plutôt que sur une faille logicielle. La vulnérabilité réside dans le **déficit de preuve d'identité persistante** : le décalage entre la validation d'un candidat lors du recrutement et l'utilisation réelle des comptes d'accès.

**Signes d'alerte :**
*   Incohérences entre le nom du titulaire du compte et les détails bancaires.
*   Utilisation multiple d'une même identité pour divers comptes.
*   Connexions répétées depuis des adresses IP suspectes ou incohérentes.
*   Volume d'heures travaillées anormalement élevé.

**Recommandations :**
*   **Vérification biométrique :** Implémenter des solutions de vérification d'identité utilisant la numérisation de documents officiels couplée à une détection de présence réelle (*liveness detection*) pour contrer les deepfakes ou les enregistrements vidéo.
*   **Preuve d'identité continue :** Ne pas considérer l'identité comme un enregistrement figé. Exiger une nouvelle confirmation d'identité avant toute intervention sensible du service desk ou lors des changements d'accès.
*   **Contrôles croisés :** Renforcer les processus de livraison de matériel et les méthodes de paiement pour limiter l'usage d'intermédiaires ou de crypto-monnaies non traçables.

---
[Source](https://www.bleepingcomputer.com/news/security/the-threat-hiding-in-your-hiring-process-how-fake-remote-workers-get-in/){:target="_blank"}
