---
title: 'Target employees confirm leaked code after accelerated Git lockdown'
date: 2026-01-13
permalink: /posts/2026/01/13/target-employees-confirm-leaked-code-after-accelerated-git-lockdown/
tags:
- veille-cyber
- bleepingcomp
---
**Vérification de la fuite de code interne chez Target**

Des employés actuels et anciens de Target ont confirmé l'authenticité du code source et de la documentation partagés en ligne par un acteur malveillant. Ces documents correspondent à des systèmes internes de l'entreprise, tels que des plateformes de déploiement d'applications nommées "BigRED" et "TAP [Provisioning]", des ensembles de données Hadoop, et une plateforme CI/CD personnalisée basée sur Vela, ainsi que l'utilisation d'outils comme JFrog Artifactory. La présence de noms de projets internes et d'identifiants spécifiques renforce la crédibilité de ces révélations.

Suite à la découverte de cette fuite, Target a rapidement mis en place des mesures de sécurité. L'accès au serveur Git interne de l'entreprise (git.target.com), qui héberge le code source développé en interne, est désormais restreint à la seule connexion via le réseau géré par Target (sur site ou par VPN). Cette modification, qualifiée d'"accélérée", a été déployée le jour suivant la prise de contact de BleepingComputer avec l'entreprise.

L'origine exacte de la fuite reste indéterminée. Cependant, des informations suggèrent qu'un poste de travail d'un employé de Target aurait été compromis par un logiciel espion (infostealer) fin septembre 2025, ayant permis un accès étendu aux services internes, y compris la gestion des identités et des accès (IAM), ainsi qu'à des wikis et Jira. Il n'est pas confirmé que cette infection soit directement liée à la vente actuelle du code source, mais des acteurs malveillants peuvent monétiser des données volées plusieurs mois après l'exfiltration. L'acteur malveillant prétend détenir un ensemble de données d'environ 860 Go, bien que seul un échantillon limité ait été examiné.

**Points Clés :**

*   Des employés confirment l'authenticité du code source et de la documentation de Target partagés en ligne.
*   Les documents divulgués contiennent des références à des systèmes internes spécifiques, des noms de projets et des identifiants uniques à l'entreprise.
*   Target a restreint l'accès à son serveur Git interne après avoir été informée de la fuite.
*   Une piste potentielle de compromission par logiciel espion sur le poste d'un employé est évoquée.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est explicitement mentionnée dans l'article comme étant la cause directe de la fuite. L'article suggère une possible compromission par un logiciel espion sur un poste de travail d'employé.

**Recommandations :**

*   **Pour Target (implicitement) :**
    *   Sécuriser rigoureusement les accès aux dépôts de code source internes.
    *   Mettre en place une surveillance continue des activités sur les serveurs Git et les systèmes internes.
    *   Renforcer la sécurité des postes de travail des employés, notamment contre les logiciels malveillants (infostealers).
    *   Mener une enquête approfondie pour déterminer la cause et l'étendue de la fuite.
*   **Pour les employés :**
    *   Faire preuve de vigilance face aux tentatives de phishing et aux logiciels malveillants.
    *   Respecter les politiques de sécurité de l'entreprise concernant l'accès aux systèmes et aux données sensibles.
    *   Signaler toute activité suspecte aux équipes de sécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/target-employees-confirm-leaked-code-after-accelerated-git-lockdown/){:target="_blank"}
