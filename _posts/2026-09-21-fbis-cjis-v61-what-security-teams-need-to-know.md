---
title: 'FBIs CJIS v6.1: What Security Teams Need to Know.'
date: 2026-09-21
permalink: /posts/2026/09/21/fbis-cjis-v61-what-security-teams-need-to-know/
tags:
- veille-cyber
- bleepingcomp
---
### Évolution de la politique de sécurité CJIS v6.1 : ce qu'il faut savoir

La version 6.1 de la politique de sécurité du CJIS (FBI), publiée en juin 2026, consolide les réformes introduites par la version 6.0 tout en renforçant les exigences techniques. L'accent est mis sur une transition vers une évaluation continue de la conformité, plutôt que sur des audits ponctuels triennaux.

**Points clés**
* **Changement de paradigme :** Les audits deviennent plus fréquents et exigent désormais des preuves constantes du bon fonctionnement des contrôles, au-delà de leur simple existence.
* **Calendrier de conformité :** Si les contrôles de priorité 1 sont sanctionnables depuis octobre 2024, ceux des priorités 2 à 4 bénéficient d'une période de transition jusqu'au 30 septembre 2027.
* **Tendance « Zero Trust » :** Bien que non explicitement nommé, le cadre évolue vers une vérification stricte de l'identité des utilisateurs et de l'état de sécurité des appareils, indépendamment de leur emplacement réseau.

**Renforcement des exigences techniques**
* **Chiffrement :** Les exigences de chiffrement pour les données en transit (SC-13) et au repos (SC-28) passent d'un standard de 128 bits à un minimum de 256 bits.
* **Gestion des vulnérabilités :** La fréquence des scans de vulnérabilités, incluant les logiciels et micrologiciels, est portée de trimestrielle à mensuelle.
* **Authentification (IA-2 & IA-5) :** L'authentification multi-facteurs (MFA) reste obligatoire pour tous les comptes (privilégiés ou non). Les politiques de mots de passe imposent une comparaison trimestrielle des secrets mémorisés avec une liste de mots de passe compromis ou couramment utilisés.

**Vulnérabilités et points de vigilance récurrents**
Les audits récents (notamment au Michigan) soulignent des failles récurrentes dans les domaines suivants :
* Absence ou mauvaise implémentation du MFA.
* Procédures BYOD (Bring Your Own Device) inadaptées ou inexistantes.
* Lacunes dans la gestion des politiques de sécurité, des journaux d'événements (logging) et de la formation du personnel.

**Recommandations pour les équipes sécurité**
* **Audit préalable :** Utiliser des outils d'audit d'Active Directory pour identifier les mots de passe compromis et les failles de stratégie avant les contrôles officiels.
* **Automatisation :** Mettre en œuvre des solutions capables de bloquer les mots de passe compromis en temps réel lors de leur création ou modification.
* **Couverture MFA étendue :** Déployer le MFA non seulement pour les accès distants, mais également pour l'ouverture de session locale et RDP, afin de garantir une conformité totale avec les exigences d'identité.
* **Coordination :** Vérifier systématiquement les attentes spécifiques auprès des agences étatiques (CSA), car les calendriers de transition peuvent varier localement.

---
[Source](https://www.bleepingcomputer.com/news/security/fbis-cjis-v61-what-security-teams-need-to-know/){:target="_blank"}
