---
title: 'FBI Warns of UNC6040 and UNC6395 Targeting Salesforce Platforms in Data Theft Attacks'
date: 2025-09-13
permalink: /posts/2025/09/13/fbi-warns-of-unc6040-and-unc6395-targeting-salesforce-platforms-in-data-theft-attacks/
tags:
- veille-cyber
- hackernews
---
**Menaces sur Salesforce : UNC6040 et UNC6395 ciblent les données d'entreprise**

Le FBI a diffusé des alertes concernant deux groupes de cybercriminels, UNC6040 et UNC6395, qui ciblent activement les plateformes Salesforce dans le cadre d'attaques visant le vol et l'extorsion de données. Ces groupes utilisent divers vecteurs d'accès initiaux pour compromettre les environnements Salesforce.

**UNC6395** est notamment suspecté d'une campagne étendue de vol de données en août 2025, exploitant des jetons OAuth compromis liés à l'application Salesloft Drift. La compromission du compte GitHub de Salesloft entre mars et juin 2025 a facilité cette attaque. En réponse, Salesloft a isolé l'infrastructure de Drift, mis l'application hors ligne et procède à des renforcements de sécurité, incluant la rotation des identifiants et la mise en place d'une authentification multi-facteurs. L'entreprise recommande aux clients de considérer toutes les données et intégrations Drift comme potentiellement compromises.

**UNC6040**, actif depuis octobre 2024, mène des campagnes de vishing (hameçonnage vocal) pour obtenir un accès initial aux instances Salesforce. Ce groupe utilise une version modifiée de Salesforce Data Loader et des scripts Python personnalisés pour exfiltrer de grandes quantités de données. Les attaques sont souvent suivies d'activités d'extorsion, parfois plusieurs mois après le vol de données initial. UNC6040 utilise des panneaux de phishing pour rediriger les victimes, puis des requêtes API pour l'exfiltration massive de données.

L'extorsion fait suite à ces intrusions et est attribuée à un autre groupe, UNC6240, qui se fait passer pour le groupe ShinyHunters. Google a également signalé que des acteurs utilisant la marque "ShinyHunters" pourraient envisager de lancer un site de fuite de données (DLS) pour accroître la pression sur les victimes.

Dans un développement récent, les groupes ShinyHunters, Scattered Spider et LAPSUS$ ont annoncé la consolidation de leurs efforts criminels sous le nom "scattered LAPSUS$ hunters 4.0". Cependant, ils ont ensuite déclaré "rentrer dans l'ombre" (go dark), potentiellement pour éviter l'attention des forces de l'ordre suite à des arrestations présumées. Les experts soulignent que ces annonces sont rarement synonymes de retraite définitive, les groupes ayant tendance à se scinder, se rebrandir et resurgir sous de nouvelles identités. La vigilance reste donc de mise, car le risque demeure même en l'absence d'opérations publiques visibles.

**Points Clés:**

*   Le FBI alerte sur les groupes UNC6040 et UNC6395 ciblant les plateformes Salesforce.
*   UNC6395 a exploité des jetons OAuth compromis pour accéder à des données via l'application Salesloft Drift.
*   UNC6040 utilise le vishing et des outils personnalisés pour le vol de données à grande échelle depuis Salesforce, suivi d'extorsion.
*   Un groupe d'acteurs, incluant ShinyHunters, Scattered Spider et LAPSUS$, a annoncé une "pause" dans ses activités.
*   Les experts préviennent que la discrétion de ces groupes ne signifie pas une disparition de la menace, mais plutôt une possible adaptation et un changement de nom.

**Vulnérabilités/Mécanismes d'Attaque:**

*   Exploitation de jetons OAuth compromis (associé à UNC6395 et Salesloft Drift).
*   Compromission de comptes de développement (ex: compte GitHub de Salesloft).
*   Ingénierie sociale (vishing) pour obtenir un accès initial (associé à UNC6040).
*   Utilisation d'outils personnalisés (version modifiée de Salesforce Data Loader, scripts Python) pour l'exfiltration de données (associé à UNC6040).
*   Requêtes API pour l'exfiltration massive de données (associé à UNC6040).

**Recommandations:**

*   **Pour les clients Salesloft:** Traiter toutes les intégrations et données relatives à l'application Drift comme potentiellement compromises.
*   **Pour toutes les organisations utilisant Salesforce:** Renforcer la sécurité des plateformes, incluant la mise en place et le renforcement de l'authentification multi-facteurs.
*   **Général:** Maintenir une vigilance constante face aux menaces évolutives, même lorsque les groupes de cybercriminels déclarent se retirer ou changer de nom. Les organisations doivent supposer que la menace persiste et s'adapte.

---
[Source](https://thehackernews.com/2025/09/fbi-warns-of-unc6040-and-unc6395.html){:target="_blank"}
