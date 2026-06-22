---
title: 'Google Sets Sept. 30 Deadline for Android Developer Verification in Four Countries'
date: 2026-06-22
permalink: /posts/2026/06/22/google-sets-sept-30-deadline-for-android-developer-verification-in-four-countries/
tags:
- veille-cyber
- hackernews
---
### Renforcement de la vérification des développeurs Android : Nouvelles restrictions de Google

À compter du 30 septembre 2026, Google imposera une procédure de vérification d'identité pour tous les développeurs d'applications Android au Brésil, en Indonésie, à Singapour et en Thaïlande. Cette mesure, visant à limiter la propagation de logiciels malveillants et d'escroqueries, affectera l'installation d'applications sur les appareils certifiés (plus de 95 % des terminaux hors Chine).

**Points clés :**
*   **Service de vérification :** Un nouveau service système (*Android Developer Verifier*) vérifiera la signature et l'enregistrement de chaque application avant son installation.
*   **Périmètre :** La restriction s'applique aux applications provenant du Google Play Store ainsi que des boutiques tierces (Samsung, Xiaomi, Oppo, etc.).
*   **Parcours dégradé :** Les applications non vérifiées pourront toujours être installées via des méthodes complexes (ADB ou flux avancé nécessitant 24 heures d'attente et une réauthentification), mais ne bénéficieront plus d'une installation fluide.
*   **Exceptions :** Un programme pour les développeurs indépendants, étudiants et hobbyistes permettra une distribution limitée (jusqu'à 20 appareils) sans frais ni exigence d'identité gouvernementale.

**Vulnérabilités et risques associés :**
*   **Cybercriminalité :** Google justifie cette mesure par la recrudescence des applications malveillantes provenant de sources hors Play Store, souvent utilisées dans des campagnes d'escroquerie ciblées.
*   **Centralisation :** La communauté open-source (notamment F-Droid) dénonce un risque de contrôle excessif, où Google devient l'arbitre unique de la légitimité des logiciels, menaçant le développement anonyme et les projets communautaires.
*   **Absence de CVE :** Cette mesure est une évolution de politique de sécurité et de filtrage applicatif, non liée à une faille technique spécifique identifiée par un CVE.

**Recommandations pour les développeurs :**
*   **Enregistrement :** Les développeurs doivent fournir une identité légale (nom, adresse, pièce d'identité) et prouver la propriété de leurs applications via leur clé privée de signature.
*   **Utilisation des API :** Google met à disposition des outils pour la vérification en masse et l'intégration avec des boutiques tierces pour faciliter la conformité.
*   **Anticipation :** Les organisations utilisant des canaux de distribution indépendants doivent se préparer à l'extension mondiale du dispositif prévue pour 2027, en évaluant si leurs modèles de distribution (notamment open-source) peuvent s'adapter aux exigences d'enregistrement.

---
[Source](https://thehackernews.com/2026/06/google-sets-sept-30-deadline-for.html){:target="_blank"}
