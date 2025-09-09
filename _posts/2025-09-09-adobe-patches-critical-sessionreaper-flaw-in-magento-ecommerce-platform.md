---
title: 'Adobe patches critical SessionReaper flaw in Magento eCommerce platform'
date: 2025-09-09
permalink: /posts/2025/09/09/adobe-patches-critical-sessionreaper-flaw-in-magento-ecommerce-platform/
tags:
- veille-cyber
- bleepingcomp
---
**Adobe Corrige une Faillesse Critique dans Magento**

Adobe a déployé un correctif pour une vulnérabilité sévère, surnommée "SessionReaper", affectant ses plateformes Adobe Commerce et Magento Open Source. Cette faille (CVE-2025-54236) permet une prise de contrôle des comptes clients via l'API REST sans authentification préalable. Bien qu'Adobe n'ait pas connaissance d'exploitations actives, une fuite récente d'un correctif préliminaire pourrait avoir donné un avantage aux cybercriminels. L'exploitation semble dépendre de la configuration par défaut du stockage des données de session sur le système de fichiers.

**Points Clés:**

*   **Vulnérabilité :** SessionReaper (CVE-2025-54236)
*   **Produits Affectés :** Adobe Commerce et Magento Open Source
*   **Impact Potentiel :** Prise de contrôle des comptes clients, contournement des fonctionnalités de sécurité, élévation de privilèges, accès aux services internes, exécution de code.
*   **Mode d'Exploitation :** Via l'API REST Commerce, sans authentification préalable.
*   **Conditions d'Exploitation :** Semble dépendre du stockage des données de session sur le système de fichiers (configuration par défaut).
*   **État de la Vulnérabilité :** Bien qu'Adobe n'ait pas connaissance d'exploitations en cours, un correctif a fuité, potentiellement exposant la faille.
*   **Gravité :** Considérée comme l'une des failles les plus critiques dans l'historique de Magento.

**Vulnérabilités :**

*   **CVE-2025-54236** : "SessionReaper"

**Recommandations :**

*   **Appliquer immédiatement le correctif disponible** pour Adobe Commerce et Magento Open Source.
*   Tester le correctif avant son déploiement, car il pourrait affecter des fonctionnalités internes ou du code personnalisé.
*   Les utilisateurs d'Adobe Commerce sur Cloud bénéficient d'une protection intermédiaire via un pare-feu d'application Web (WAF).
*   Consulter la documentation mise à jour par Adobe concernant les modifications de l'injection de paramètres dans le constructeur de l'API REST Adobe Commerce.

---
[Source](https://www.bleepingcomputer.com/news/security/adobe-patches-critical-sessionreaper-flaw-in-magento-ecommerce-platform/){:target="_blank"}
