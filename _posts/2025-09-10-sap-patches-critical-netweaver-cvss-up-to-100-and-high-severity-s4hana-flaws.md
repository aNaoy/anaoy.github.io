---
title: 'SAP Patches Critical NetWeaver (CVSS Up to 10.0) and High-Severity S/4HANA Flaws'
date: 2025-09-10
permalink: /posts/2025/09/10/sap-patches-critical-netweaver-cvss-up-to-100-and-high-severity-s4hana-flaws/
tags:
- veille-cyber
- hackernews
---
**Mises à jour de sécurité critiques pour SAP NetWeaver et S/4HANA**

SAP a publié des correctifs pour plusieurs vulnérabilités, dont trois critiques dans SAP NetWeaver et une de gravité élevée dans SAP S/4HANA.

**Points clés :**

*   Trois vulnérabilités critiques dans SAP NetWeaver menacent l'exécution de code et le téléchargement de fichiers arbitraires.
*   Une vulnérabilité de gravité élevée dans SAP S/4HANA permet la suppression de données dans des tables de base de données non protégées.
*   Ces correctifs interviennent alors qu'une autre vulnérabilité critique dans SAP S/4HANA, corrigée précédemment, est activement exploitée.

**Vulnérabilités :**

*   **CVE-2025-42944 (CVSS 10.0) :** Vulnérabilité de désérialisation dans SAP NetWeaver permettant l'exécution de commandes système via le module RMI-P4 par un attaquant non authentifié.
*   **CVE-2025-42922 (CVSS 9.9) :** Vulnérabilité d'opérations de fichiers non sécurisées dans SAP NetWeaver AS Java permettant à un utilisateur non administratif de télécharger un fichier arbitraire.
*   **CVE-2025-42958 (CVSS 9.1) :** Manque de vérification d'authentification dans SAP NetWeaver sur IBM i-series permettant à des utilisateurs non autorisés de lire, modifier ou supprimer des informations sensibles, et d'accéder à des fonctionnalités administratives.
*   **CVE-2025-42916 (CVSS 8.1) :** Manque de validation d'entrée dans SAP S/4HANA permettant à un attaquant privilégié de supprimer le contenu de tables de base de données arbitraires si elles ne sont pas protégées.

**Recommandations :**

Il est crucial d'appliquer ces mises à jour dès que possible pour assurer une protection optimale. Les utilisateurs de CVE-2025-42944 sont invités à implémenter un filtrage du port P4 au niveau de l'ICM comme solution de contournement temporaire.

---
[Source](https://thehackernews.com/2025/09/sap-patches-critical-netweaver-cvss-up.html){:target="_blank"}
