---
title: 'Pixel 10 fights AI fakes with new Android photo verification tech'
date: 2025-09-10
permalink: /posts/2025/09/10/pixel-10-fights-ai-fakes-with-new-android-photo-verification-tech/
tags:
- veille-cyber
- bleepingcomp
---
**Authentification des images sur Pixel 10 : Lutte contre les faux générés par IA**

Les nouveaux appareils Pixel 10 intègrent la technologie C2PA Content Credentials pour permettre aux utilisateurs de distinguer les images authentiques des contenus modifiés ou générés par intelligence artificielle. Cette fonctionnalité, intégrée à l'appareil photo et à l'application Google Photos, ajoute des informations de provenance à chaque photo JPEG capturée.

Les "Content Credentials" fournissent des détails sur la création et les modifications apportées à un média, sécurisés par une technologie de signature numérique éprouvée. Ce système vise à renforcer la transparence et la confiance dans l'IA générative, permettant d'identifier les contenus synthétiques. Même lors de modifications avec des outils d'IA ou non, Google Photos enregistre les nouvelles informations de provenance, conservant ainsi un historique des modifications.

Le système fonctionne hors ligne, est protégé contre les interférences externes et préserve l'anonymat de l'utilisateur tout en garantissant la vérifiabilité. Plusieurs couches de sécurité sont implémentées pour assurer l'intégrité et la résistance aux manipulations des "Content Credentials" :

*   **Signature cryptographique :** La modification des métadonnées invalide la signature numérique.
*   **Stockage sécurisé des clés :** Les clés cryptographiques sont générées et stockées dans le composant Android StrongBox du Titan M2.
*   **Attestation des clés Android :** Permet aux autorités de certification C2PA de Google de vérifier l'authenticité du matériel et de l'application.
*   **Clés à usage unique par image :** Chaque photo est signée avec une clé cryptographique unique pour préserver la confidentialité.
*   **Horodatage de confiance sur l'appareil :** Un horloge interne sécurisée par la puce Tensor permet d'ajouter des horodatages vérifiables même hors ligne.

Bien qu'actuellement limitée aux Pixel 10, Google envisage d'étendre cette fonctionnalité à d'autres appareils Android à l'avenir. L'entreprise encourage l'adoption généralisée de ces "Content Credentials" pour lutter efficacement contre la désinformation et les "deepfakes".

**Points clés :**

*   Intégration de C2PA Content Credentials sur Pixel 10.
*   Vérification de l'authenticité des images et historique des modifications.
*   Protection contre les contenus générés ou modifiés par IA.
*   Système sécurisé, fonctionnant hors ligne et préservant la vie privée.

**Vulnérabilités :**
Aucune vulnérabilité spécifique n'est mentionnée dans l'article.

**Recommandations :**

*   Adopter une approche standardisée comme les "Content Credentials" pour lutter contre la désinformation.
*   Favoriser une adoption large de la technologie à travers l'écosystème des appareils.

---
[Source](https://www.bleepingcomputer.com/news/security/pixel-10-fights-ai-fakes-with-new-android-photo-verification-tech/){:target="_blank"}
