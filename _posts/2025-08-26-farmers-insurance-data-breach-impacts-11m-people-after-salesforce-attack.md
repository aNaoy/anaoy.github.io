---
title: 'Farmers Insurance data breach impacts 1.1M people after Salesforce attack'
date: 2025-08-26
permalink: /posts/2025/08/26/farmers-insurance-data-breach-impacts-11m-people-after-salesforce-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Fuite de Données chez Farmers Insurance suite à une Compromission Salesforce**

Un incident de cybersécurité a touché Farmers Insurance, exposant les informations personnelles de plus de 1,1 million de clients. L'attaque, survenue le 29 mai 2025, a été détectée par un fournisseur tiers de l'entreprise. Les données dérobées incluent des noms, adresses, dates de naissance, numéros de permis de conduire et les quatre derniers chiffres des numéros de sécurité sociale. Farmers Insurance a commencé à informer les personnes affectées le 22 août.

Il a été révélé que cette fuite est liée aux attaques généralisées visant les clients Salesforce par le groupe de menaces UNC6040 (ou UNC6240) et le groupe de cybercriminalité ShinyHunters. Les pirates utilisent des techniques d'ingénierie sociale, notamment le vishing (hameçonnage vocal), pour inciter les employés à autoriser des applications malveillantes via OAuth, leur donnant ainsi accès aux bases de données Salesforce. Ces informations sont ensuite utilisées pour des demandes d'extorsion. ShinyHunters a indiqué que les attaques impliquent plusieurs groupes collaborant sur différentes phases du processus. D'autres entreprises de renom, telles que Google, Cisco, Workday, Adidas, Qantas, Allianz Life et plusieurs filiales de LVMH (Louis Vuitton, Dior, Tiffany & Co.), ont également été victimes de ces attaques similaires.

**Points Clés:**

*   **Victime:** Farmers Insurance
*   **Nombre de personnes affectées:** 1 111 386 clients
*   **Date de la brèche:** 29 mai 2025
*   **Nature de l'incident:** Vol de données via une compromission de base de données chez un fournisseur tiers.
*   **Cause présumée:** Attaques généralisées sur les clients Salesforce menées par les groupes UNC6040/UNC6240 et ShinyHunters.
*   **Méthode d'attaque:** Ingénierie sociale (vishing) via des applications OAuth malveillantes liées à des instances Salesforce.
*   **Motif des attaquants:** Extorsion.

**Vulnérabilités/Tactiques:**

*   **Ingénierie Sociale (Vishing):** Tromperie des employés par téléphone pour obtenir des accès non autorisés.
*   **Autorisation d'applications Malveillantes (OAuth):** Exploitation du mécanisme d'autorisation pour lier des applications compromises à des plateformes d'entreprise.
*   **Compromission de Fournisseur Tiers:** La sécurité des données d'une entreprise dépend également de celle de ses partenaires.

**Recommandations Générales (Déduites du contexte de l'article):**

*   **Renforcer les défenses contre le vishing:** Sensibilisation des employés aux tentatives d'hameçonnage vocal et aux demandes d'autorisations inhabituelles.
*   **Auditer et surveiller les intégrations d'applications:** Examiner régulièrement les applications autorisées à accéder aux plateformes critiques comme Salesforce et révoquer les accès non nécessaires ou suspects.
*   **Mettre en place une segmentation et une gestion rigoureuses des accès:** S'assurer que les employés n'ont accès qu'aux données strictement nécessaires à leurs fonctions.
*   **Améliorer la sécurité des fournisseurs tiers:** Mettre en place des audits de sécurité réguliers et des clauses contractuelles strictes concernant la protection des données pour les partenaires.
*   **Réagir rapidement aux alertes de sécurité:** Mettre en place des systèmes de surveillance pour détecter et contenir rapidement les activités suspectes.

---
[Source](https://www.bleepingcomputer.com/news/security/farmers-insurance-data-breach-impacts-11m-people-after-salesforce-attack/){:target="_blank"}
