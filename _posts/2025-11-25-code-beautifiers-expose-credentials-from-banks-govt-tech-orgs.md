---
title: 'Code beautifiers expose credentials from banks, govt, tech orgs'
date: 2025-11-25
permalink: /posts/2025/11/25/code-beautifiers-expose-credentials-from-banks-govt-tech-orgs/
tags:
- veille-cyber
- bleepingcomp
---
**Exposition de Données Sensibles via des Outils de Formatage de Code**

Des milliers d'identifiants, clés d'authentification et données de configuration, affectant des organisations dans des secteurs critiques tels que le gouvernement, la banque, les infrastructures critiques, la santé et la technologie, ont été découverts dans des extraits JSON accessibles publiquement. Les outils en ligne JSONFormatter et CodeBeautify, utilisés pour formater le code, exposent ces informations sensibles via une fonctionnalité de "Liens Récents" non protégée.

**Points Clés :**

*   Plus de 80 000 "pâtes" utilisateur (données soumises) contenant plus de 5 Go de données sensibles ont été identifiées.
*   Ces données proviennent d'organisations des secteurs gouvernemental, bancaire, de la santé, de la cybersécurité, des télécommunications, de l'aérospatiale, des assurances et des infrastructures critiques.
*   La fonctionnalité "Liens Récents" de ces outils génère des URL prévisibles et non protégées pour les données sauvegardées, les rendant facilement accessibles aux outils d'exploration automatisée.
*   Des tests avec des honeypots ont montré des tentatives d'accès à des clés AWS factices peu après leur mise en ligne, prouvant que les acteurs malveillants scannent activement ces plateformes.
*   Malgré les alertes envoyées aux organisations concernées, beaucoup n'ont pas encore corrigé le problème.

**Vulnérabilités Exposées :**

*   Identifiants Active Directory
*   Identifiants de bases de données et cloud
*   Clés privées
*   Tokens de dépôts de code
*   Secrets CI/CD
*   Clés de passerelle de paiement
*   Tokens API
*   Enregistrements de sessions SSH
*   Informations personnelles identifiables (PII), y compris des données KYC
*   Identifiants AWS pour des systèmes de sécurité (ex: Splunk SOAR)
*   Mots de passe de clés privées de certificats SSL
*   Noms d'hôtes et adresses IP externes et internes
*   Chemins vers des clés, certificats et fichiers de configuration

**Recommandations :**

*   **Ne pas utiliser d'outils de formatage de code en ligne pour soumettre ou stocker des informations sensibles** telles que des identifiants, des clés d'API ou des données de configuration.
*   Mettre en place des politiques et des formations pour sensibiliser les développeurs aux risques liés à l'exposition de secrets.
*   Utiliser des solutions de gestion des secrets dédiées qui offrent un stockage sécurisé et un contrôle d'accès strict.
*   Les fournisseurs d'outils de formatage de code devraient implémenter des mesures de sécurité robustes pour protéger les données soumises par les utilisateurs, notamment par le chiffrement et un contrôle d'accès approprié.

---
[Source](https://www.bleepingcomputer.com/news/security/code-beautifiers-expose-credentials-from-banks-govt-tech-orgs/){:target="_blank"}
