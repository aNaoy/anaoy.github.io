---
title: 'Chinese cyberspies breach Singapores four largest telcos'
date: 2026-02-10
permalink: /posts/2026/02/10/chinese-cyberspies-breach-singapores-four-largest-telcos/
tags:
- veille-cyber
- bleepingcomp
---
**Cyberattaques ciblées contre les télécoms à Singapour**

Des acteurs malveillants chinois, identifiés sous le nom de UNC3886, ont réussi à pénétrer au moins une fois les quatre principaux fournisseurs de services de télécommunication de Singapour (Singtel, StarHub, M1 et Simba) durant l'année écoulée. Ces incursions ont permis aux attaquants d'obtenir un accès limité à des systèmes critiques, sans toutefois atteindre une profondeur suffisante pour perturber les services.

En réponse à ces intrusions, Singapour a lancé l'opération "Cyber Guardian" afin de contrer l'activité de l'adversaire sur les réseaux des opérateurs. Les autorités ont indiqué que l'attaque n'avait pas entraîné de fuite de données clients sensibles ni d'interruption de services. Les investigations ont révélé l'utilisation par UNC3886 d'une faille zero-day pour contourner les pare-feu périmétriques et voler des données techniques. Dans d'autres cas, des rootkits ont été employés pour maintenir une présence furtive.

**Points clés :**

*   **Cible :** Les quatre plus grands opérateurs de télécommunications de Singapour.
*   **Acteur :** UNC3886, groupe de cyberespionnage chinois.
*   **Date des intrusions :** Au moins une fois l'année dernière.
*   **Accès :** Limité à des systèmes critiques, sans perturbation de services ni vol de données clients confirmé.
*   **Techniques :** Exploitation de vulnérabilités zero-day et utilisation de rootkits pour la persistance.
*   **Réponse :** Déploiement de l'opération "Cyber Guardian" par les autorités singapouriennes.

**Vulnérabilités (avec CVE si possible) :**

*   Une vulnérabilité zero-day non spécifiée a été utilisée à Singapour pour contourner les pare-feu.
*   UNC3886 a déjà exploité des vulnérabilités zero-day dans :
    *   FortiGate firewalls (CVE-2022-41328)
    *   VMware ESXi (CVE-2023-20867)
    *   VMware vCenter Server (CVE-2023-34048)

**Recommandations :**

*   Les détails spécifiques des vulnérabilités exploitées à Singapour n'ont pas été partagés, rendant difficile la formulation de recommandations précises pour cet incident particulier.
*   Les attaques antérieures attribuées à UNC3886 soulignent l'importance de la sécurisation des pare-feu et des environnements de virtualisation (VMware ESXi, vCenter).
*   La surveillance continue des réseaux et la mise en place de mécanismes de détection et de réponse rapides sont cruciales pour contenir les menaces persistantes avancées.
*   La collaboration entre les opérateurs, les autorités et les chercheurs en cybersécurité est essentielle pour identifier et contrer ces menaces.

---
[Source](https://www.bleepingcomputer.com/news/security/chinese-cyberspies-breach-singapores-four-largest-telcos/){:target="_blank"}
