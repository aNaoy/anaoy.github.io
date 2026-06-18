---
title: 'The Scripts on Your Checkout Page Are Now a PCI DSS Problem'
date: 2026-06-18
permalink: /posts/2026/06/18/the-scripts-on-your-checkout-page-are-now-a-pci-dss-problem/
tags:
- veille-cyber
- hackernews
---
### La conformité PCI DSS v4.0.1 face aux attaques de scripts tiers

Les pages de paiement modernes dépendent d'une multitude de scripts tiers (analytics, outils de support, gestionnaires de balises) qui constituent des vecteurs d'attaque majeurs, notamment pour le "web skimming" (type Magecart). Une fois qu'un fournisseur tiers est compromis, le code malveillant s'exécute via des scripts légitimes et approuvés, rendant la détection par simple vérification de hash inefficace. 30 % des scripts de paiement changent tous les quinze jours, rendant le contrôle manuel non viable.

**Points clés**
*   **Nouvelles exigences PCI DSS v4.0.1 :** 
    *   **6.4.3 :** Inventaire, autorisation et preuve d'intégrité de chaque script présent sur les pages de paiement.
    *   **11.6.1 :** Détection de toute altération des contenus de page et des en-têtes HTTP lors de la réception par le navigateur.
*   **Limites des iFrames :** Même avec un iframe sécurisé, un script malveillant sur la page parente peut intercepter les données avant qu'elles n'atteignent le cadre de paiement.
*   **Vulnérabilités :** Attaques de type *Supply-Chain* et *Web Skimming* (pas de CVE spécifique, car il s'agit d'une menace liée aux comportements de scripts et non à des vulnérabilités logicielles statiques).

**Recommandations**
*   **Surveillance comportementale :** Privilégier des solutions qui analysent le comportement des scripts (tentatives d'accès aux données) plutôt que la simple intégrité des fichiers (hash), car les attaquants injectent souvent du code au sein de scripts valides.
*   **Automatisation de l'audit :** Utiliser des outils capables de fournir une piste d'audit continue pour répondre aux exigences des auditeurs (QSA) sans alourdir la gestion quotidienne.
*   **Évaluation de conformité :** Les marchands utilisant des iframes doivent impérativement valider que leur environnement n'est pas vulnérable au détournement de saisie, conformément à la FAQ #1588 du PCI SSC, pour prétendre à une exemption sur les contrôles 6.4.3 et 11.6.1.

---
[Source](https://thehackernews.com/2026/06/the-scripts-on-your-checkout-page-are.html){:target="_blank"}
