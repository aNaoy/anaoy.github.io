---
title: 'IQVIA fined $7.8 million for failing to properly anonymize health data'
date: 2026-10-05
permalink: /posts/2026/10/05/iqvia-fined-78-million-for-failing-to-properly-anonymize-health-data/
tags:
- veille-cyber
- bleepingcomp
---
### Condamnation d'IQVIA pour défaut d'anonymisation de données de santé

L'autorité italienne de protection des données (GPDP) a infligé une amende de 7,8 millions de dollars à la multinationale IQVIA pour des pratiques de traitement des données non conformes. Une enquête a révélé qu'une base de données regroupant les informations d'un million de patients était vulnérable à la réidentification, malgré l'usage de pseudonymes.

**Points clés :**
*   **Risque de réidentification :** L'utilisation de codes uniques associés à des informations détaillées (diagnostics, traitements, localisation) permettait de suivre et d'identifier individuellement les patients.
*   **Données sensibles exposées :** Pour 3 300 patients, la base contenait des données nominatives (noms, adresses, numéros fiscaux).
*   **Absence de gouvernance :** IQVIA n'a pas défini de période de rétention des données, conservant des informations remontant jusqu'à 2001.
*   **Violations du RGPD :** Défaut de base légale pour le traitement et absence d'information des personnes concernées.

**Vulnérabilités :**
Aucune CVE n'est associée, car il s'agit d'une défaillance de conformité et de conception de protection des données (Privacy by Design) plutôt que d'une faille logicielle spécifique. La vulnérabilité réside dans une **pseudonymisation insuffisante** (réversibilité de l'anonymisation).

**Recommandations :**
*   **Renforcement de l'anonymisation :** Mettre en œuvre des techniques robustes empêchant la réidentification croisée.
*   **Politique de rétention :** Appliquer strictement des cycles de suppression des données pour limiter l'exposition temporelle.
*   **Conformité légale :** S'assurer qu'une base juridique explicite est établie et que les patients sont dûment informés du traitement de leurs données.
*   **Mise en conformité :** IQVIA dispose de 120 jours pour aligner ses pratiques avec les exigences de l'autorité italienne.

---
[Source](https://www.bleepingcomputer.com/news/security/iqvia-fined-78-million-for-failing-to-properly-anonymize-health-data/){:target="_blank"}
