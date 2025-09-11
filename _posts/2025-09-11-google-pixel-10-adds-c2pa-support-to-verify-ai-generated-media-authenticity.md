---
title: 'Google Pixel 10 Adds C2PA Support to Verify AI-Generated Media Authenticity'
date: 2025-09-11
permalink: /posts/2025/09/11/google-pixel-10-adds-c2pa-support-to-verify-ai-generated-media-authenticity/
tags:
- veille-cyber
- hackernews
---
### Pixels 10 : Certification de l'authenticité des médias

Les nouveaux téléphones Google Pixel 10 intègrent désormais la norme C2PA (Coalition for Content Provenance and Authenticity) pour garantir la véracité et l'historique des contenus numériques. Cette fonctionnalité, intégrée aux applications Pixel Camera et Google Photos, vise à accroître la transparence des médias numériques.

Les "Content Credentials" de la C2PA fonctionnent comme une étiquette nutritionnelle numérique. Elles fournissent des informations sur le créateur d'une image, vidéo ou fichier audio, la manière dont il a été produit, et s'il a été généré par intelligence artificielle. Cette métadonnée est protégée contre les altérations grâce à une signature cryptographique.

L'application Pixel Camera a obtenu le niveau de sécurité le plus élevé défini par le programme de conformité C2PA, le Niveau 2 d'assurance, une performance rendue possible sur la plateforme Android grâce à une combinaison de technologies :

*   **Puces Google Tensor G5 et Titan M2** : Ces éléments matériels, associés aux fonctionnalités de sécurité intégrées à Android, permettent une vérification robuste de l'authenticité.
*   **Horodatage de confiance sur l'appareil** : Les images capturées par l'application native peuvent être fiables même après l'expiration du certificat, et ce, indépendamment de la connexion internet du téléphone au moment de la prise de vue.
*   **Android Key Attestation** : Permet de vérifier l'authenticité des appareils et s'assure que la génération de clés de signature C2PA provient d'applications légitimes.
*   **Génération et stockage sécurisés des clés** : Les clés cryptographiques sont générées et stockées dans la puce Titan M2 pour une résistance accrue aux manipulations.
*   **Attestation anonyme et matérielle** : Les nouvelles clés cryptographiques sont certifiées sans identifier l'utilisateur.
*   **Certificats uniques** : Chaque image est signée individuellement, rendant impossible la désanonymisation du créateur par des moyens cryptographiques.
*   **Composant d'horodatage hors ligne** : Un module présent dans la puce Tensor applique des horodatages signés cryptographiquement au moment de la capture, même sans connexion internet.

Bien que la C2PA ne soit pas une solution unique pour tous les problèmes de provenance des médias, elle représente une avancée significative pour la transparence et la confiance dans un monde de plus en plus influencé par l'intelligence artificielle.

**Points clés :**

*   Intégration de la norme C2PA sur les Google Pixel 10.
*   Fonctionnalité "Content Credentials" pour l'authentification des médias.
*   Utilisation de technologies matérielles et logicielles pour garantir la sécurité et la vérifiabilité.
*   Niveau de sécurité élevé atteint par l'application Pixel Camera.
*   Support de l'horodatage hors ligne pour une fiabilité accrue.

**Vulnérabilités :**

L'article ne mentionne aucune vulnérabilité spécifique par son identifiant CVE. La technologie est présentée comme une mesure visant à **prévenir** les problèmes liés à la falsification et à la désinformation des médias.

**Recommandations :**

L'article ne fournit pas de recommandations au sens d'actions à entreprendre par les utilisateurs face à des menaces spécifiques. Il présente plutôt une **solution technologique** pour améliorer la confiance dans les médias numériques :

*   Adoption de la norme C2PA par les fabricants d'appareils et les développeurs d'applications.
*   Exploitation des technologies de sécurité matérielle (comme les puces Titan M2 et Tensor G5) et logicielle (Android Key Attestation) pour implémenter la certification des médias.
*   Mise en œuvre de signatures cryptographiques robustes et d'horodatages fiables pour garantir la provenance des contenus.

---
[Source](https://thehackernews.com/2025/09/google-pixel-10-adds-c2pa-support-to.html){:target="_blank"}
