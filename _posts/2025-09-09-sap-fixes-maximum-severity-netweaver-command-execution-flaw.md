---
title: 'SAP fixes maximum severity NetWeaver command execution flaw'
date: 2025-09-09
permalink: /posts/2025/09/09/sap-fixes-maximum-severity-netweaver-command-execution-flaw/
tags:
- veille-cyber
- bleepingcomp
---
**SAP Corrige des Vulnérabilités Critiques dans NetWeaver**

SAP a corrigé 21 nouvelles vulnérabilités dans ses produits, dont trois de gravité critique affectant sa solution logicielle NetWeaver, fondamentale pour de nombreuses applications d'entreprise SAP.

**Points Clés :**

*   SAP NetWeaver est la base de produits SAP comme ERP, CRM, SRM et SCM, largement déployée dans les réseaux d'entreprise.
*   Les produits SAP, souvent porteurs de données critiques, sont des cibles privilégiées pour les acteurs malveillants.

**Vulnérabilités Identifiées :**

*   **CVE-2025-42944** (Gravité : 10/10) : Vulnérabilité d'désérialisation non sécurisée dans SAP NetWeaver (RMIP4), ServerCore 7.50. Permet à un attaquant non authentifié d'exécuter des commandes arbitraires sur le système d'exploitation via le module RMI-P4. Bien que le port P4 soit ouvert sur l'hôte, des mauvaises configurations de pare-feu peuvent l'exposer à des réseaux plus larges, voire à Internet.
*   **CVE-2025-42922** (Gravité : 9.9/10) : Bug de traitement de fichiers non sécurisé dans NetWeaver AS Java (Deploy Web Service), J2EE-APPS 7.50. Un attaquant authentifié avec des privilèges non administratifs peut exploiter cette faille pour télécharger des fichiers arbitraires, potentiellement compromettant le système.
*   **CVE-2025-42958** (Gravité : 9.1/10) : Vérification d'authentification manquante dans NetWeaver. Permet à des utilisateurs non autorisés et hautement privilégiés de lire, modifier ou supprimer des données sensibles et d'accéder à des fonctionnalités administratives.

D'autres vulnérabilités de haute gravité ont également été corrigées, notamment :

*   CVE-2025-42933 (SAP Business One SLD) : Stockage non sécurisé de données sensibles.
*   CVE-2025-42929 (SLT Replication Server) : Validation d'entrée manquante, pouvant corrompre ou manipuler des données répliquées.
*   CVE-2025-42916 (S/4HANA) : Validation d'entrée manquante dans les composants centraux, risquant la manipulation non autorisée de données.

Il est à noter qu'une vulnérabilité critique de code injection (CVE-2025-42957) affectant S/4HANA, Business One et NetWeaver est déjà exploitée en attaque.

**Recommandations :**

Les administrateurs système sont fortement encouragés à appliquer les correctifs et les mesures d'atténuation recommandés par SAP pour ces trois failles critiques. Les détails sont disponibles via les notes SAP destinées aux clients.

---
[Source](https://www.bleepingcomputer.com/news/security/sap-fixes-maximum-severity-netweaver-command-execution-flaw/){:target="_blank"}
