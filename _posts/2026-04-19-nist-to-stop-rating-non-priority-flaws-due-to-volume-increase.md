---
title: 'NIST to stop rating non-priority flaws due to volume increase'
date: 2026-04-19
permalink: /posts/2026/04/19/nist-to-stop-rating-non-priority-flaws-due-to-volume-increase/
tags:
- veille-cyber
- bleepingcomp
---
### Évolution de la gestion des vulnérabilités au NIST

Face à une explosion de 263 % du volume de soumissions de vulnérabilités, le NIST a annoncé une modification majeure dans le fonctionnement de la *National Vulnerability Database* (NVD). Pour pallier l'incapacité opérationnelle à enrichir l'intégralité des entrées, l'organisme concentre désormais ses ressources d'analyse sur les failles présentant un risque systémique majeur.

**Points clés :**
*   **Changement opérationnel :** Le NIST cessera d'assigner des scores de sévérité et des détails techniques détaillés aux vulnérabilités jugées de « basse priorité ».
*   **Statut « Not Scheduled » :** Les failles ne répondant pas aux critères de priorité seront listées sans analyse approfondie par le NIST. Seule la notation initiale fournie par la *CVE Numbering Authority* (CNA) d'origine sera conservée.
*   **Critères de priorisation :** Seules les vulnérabilités remplissant l'un des critères suivants bénéficieront d'une analyse complète :
    *   Présence dans le catalogue *Known Exploited Vulnerabilities* (KEV) de la CISA.
    *   Impact sur les logiciels du gouvernement fédéral américain.
    *   Classification en tant que « logiciel critique » selon l'Executive Order 14028.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée, car la mesure s'applique de manière générale à toutes les futures soumissions ne répondant pas aux nouveaux critères de priorité.

**Recommandations :**
*   **Vigilance accrue :** Les organisations ne doivent plus compter exclusivement sur l'analyse enrichie du NIST pour évaluer le risque de l'ensemble de leur parc informatique.
*   **Utilisation des sources primaires :** Il est conseillé de se référer directement aux informations fournies par les *CVE Numbering Authorities* (CNA) ou les éditeurs logiciels pour les vulnérabilités classées « Not Scheduled ».
*   **Demandes d'enrichissement :** Pour les failles non prioritaires jugées critiques par une organisation, le NIST accepte des demandes d'analyse manuelle via l'adresse de contact dédiée : `nvd@nist.gov`.

---
[Source](https://www.bleepingcomputer.com/news/security/nist-to-stop-rating-non-priority-flaws-due-to-volume-increase/){:target="_blank"}
