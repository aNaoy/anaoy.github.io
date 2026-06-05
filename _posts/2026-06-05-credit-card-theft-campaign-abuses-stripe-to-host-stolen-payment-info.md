---
title: 'Credit card theft campaign abuses Stripe to host stolen payment info'
date: 2026-06-05
permalink: /posts/2026/06/05/credit-card-theft-campaign-abuses-stripe-to-host-stolen-payment-info/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement d'infrastructures de confiance pour le vol de données bancaires

Une nouvelle campagne de type Magecart exploite les infrastructures légitimes de Google Tag Manager (GTM) et de l'API Stripe pour orchestrer le vol de données de cartes bancaires sur des plateformes e-commerce, notamment Magento/Adobe Commerce. En utilisant des domaines de confiance, les attaquants contournent les politiques de sécurité (CSP) et les filtres réseau qui bloquent habituellement les connexions vers des domaines malveillants inconnus.

**Points clés :**
*   **Mode opératoire :** Le code malveillant est injecté via un conteneur GTM. Il intercepte les données de paiement lors de la validation du panier.
*   **Stockage détourné :** Au lieu d'exfiltrer directement les données, le malware les dissimule temporairement en local avant de les transmettre à l'API Stripe, où elles sont enregistrées dans les champs de métadonnées de faux clients créés par les attaquants.
*   **Évasion :** L'usage de services légitimes (api.stripe.com, Google Firestore) permet au trafic malveillant de passer inaperçu parmi les communications légitimes.
*   **Historique :** La campagne semble active depuis au moins fin décembre 2025.

**Vulnérabilités :**
*   Il n'existe pas de CVE spécifique, car il s'agit d'un abus de fonctionnalités légitimes et non d'une faille logicielle classique. La vulnérabilité réside dans la **confiance implicite** accordée aux domaines tiers (GTM, Stripe) dans les règles de filtrage de contenu et de sécurité réseau.

**Recommandations :**
*   **Surveillance stricte :** Auditer régulièrement les conteneurs Google Tag Manager pour détecter tout script non autorisé ou suspect.
*   **Durcissement CSP :** Affiner les politiques de sécurité du contenu (Content Security Policy) pour restreindre non seulement les domaines autorisés, mais aussi les méthodes d'exécution de scripts (`unsafe-eval` doit être proscrit).
*   **Intégrité du code :** Mettre en place des mécanismes d'intégrité des ressources (Subresource Integrity - SRI) lorsque cela est possible.
*   **Protection des utilisateurs :** Encourager les clients à utiliser des cartes de paiement virtuelles à usage unique, limitant ainsi l'impact en cas de compromission des données.

---
[Source](https://www.bleepingcomputer.com/news/security/credit-card-theft-campaign-abuses-stripe-to-host-stolen-payment-info/){:target="_blank"}
