---
title: 'Why the shift left dream has become a nightmare for security and developers'
date: 2026-02-20
permalink: /posts/2026/02/20/why-the-shift-left-dream-has-become-a-nightmare-for-security-and-developers/
tags:
- veille-cyber
- bleepingcomp
---
### Le "Shift Left" : Un Rêve de Sécurité Devenu Cauchemar

La stratégie "shift left", visant à intégrer la sécurité plus tôt dans le cycle de développement logiciel, s'est avérée inefficace, voire contre-productive. Au lieu de renforcer la sécurité, elle a exacerbé les tensions entre la nécessité de rapidité des développeurs et les exigences de sécurité, surchargeant davantage les développeurs déjà sous pression. Les impératifs commerciaux de vitesse, de qualité et de coût ont relégué la sécurité au second plan, entraînant une perte de contrôle sur les environnements informatiques.

L'utilisation généralisée d'images de conteneurs publiques, comme celles disponibles sur Docker Hub, repose sur une confiance injustifiée. Une analyse récente de plus de 34 000 images a révélé que 7,3 % d'entre elles étaient malveillantes, contenant notamment des logiciels de minage de cryptomonnaies ou des secrets exposés (clés d'accès, tokens, identifiants). Les méthodes d'attaque comme le typosquatting rendent cette pratique encore plus risquée.

Le véritable problème réside dans le fait que les développeurs, bien que compétents, sont incités à privilégier la vélocité des fonctionnalités au détriment de la sécurité, car leurs performances sont souvent mesurées à l'aune de la livraison rapide. La stratégie "shift left" a simplement déplacé cette charge cognitive vers les développeurs, sans résoudre le conflit fondamental.

Une approche plus prometteuse, qualifiée de "shift down", propose de déplacer la responsabilité de la sécurité vers la couche d'infrastructure, gérée par des équipes d'ingénierie plateforme dédiées. Cela permet de créer des chemins sécurisés par défaut pour les développeurs.

**Points Clés :**

*   L'objectif initial du "shift left" (intégrer la sécurité plus tôt dans le développement) a échoué en raison des pressions accrues sur les développeurs et du conflit entre vitesse et sécurité.
*   Les équipes de développement sont surchargées et réagissent aux incitations, favorisant la vitesse lorsque la sécurité ralentit les processus.
*   Les entreprises ont perdu le contrôle de leurs environnements en raison de l'automatisation et de la confiance aveugle envers les registres d'images publiques.
*   L'utilisation d'images de conteneurs publiques présente des risques significatifs, notamment la présence de logiciels malveillants et de secrets exposés.
*   La stratégie "shift down" vise à rendre la sécurité intrinsèque à l'infrastructure et aux processus automatisés, plutôt que de la laisser à la charge des développeurs individuels.

**Vulnérabilités :**

*   **Présence de logiciels malveillants dans les images de conteneurs publiques :** 7,3% des images analysées contenaient des logiciels malveillants, dont 70% dédiés au cryptominage.
*   **Exposition de secrets dans les images de conteneurs :** 42% des images contenaient plus de cinq secrets (clés d'accès AWS, tokens GitHub, identifiants de base de données) susceptibles de permettre un accès non autorisé.
*   **Typosquatting :** Technique courante utilisée par les attaquants pour distribuer des conteneurs malveillants en profitant d'erreurs de frappe dans les noms d'images.
*   **Manque de visibilité et de contrôle sur le code et les dépendances déployés.**

**Recommandations :**

*   **Ne pas laisser les développeurs tirer directement depuis des registres publics :** Introduire une couche de proxy interne (entrepôt d'artefacts) agissant comme une zone de quarantaine pour les images externes.
*   **Mettre en place un "chemin d'or" (golden path) pour les développeurs :** Utiliser des modèles standard, des images de base approuvées et des pipelines CI/CD officiels où la sécurité est intégrée par défaut. Les déviations nécessitent des revues de sécurité et des configurations manuelles supplémentaires.
*   **Déplacer la responsabilité de la sécurité vers la couche d'infrastructure (Shift Down) :** Les équipes d'ingénierie plateforme doivent gérer les politiques de sécurité de manière automatisée (ex: Terraform, Crossplane, OPA) pour empêcher les erreurs de configuration ou l'utilisation d'images non conformes.
*   **Automatiser la remédiation :** Les plateformes devraient automatiquement générer des demandes de mise à jour pour les vulnérabilités découvertes ou prendre des mesures d'isolement en cas de comportement suspect des conteneurs.
*   **Favoriser une collaboration étroite entre les équipes de développement et de sécurité :** Les deux équipes doivent travailler ensemble pour définir les exigences et s'assurer que les livrables sont sécurisés dès le départ.
*   **Communiquer les coûts de sécurité à l'entreprise :** Présenter un front uni sur les implications financières des décisions prises en matière de sécurité et de développement.

---
[Source](https://www.bleepingcomputer.com/news/security/why-the-shift-left-dream-has-become-a-nightmare-for-security-and-developers/){:target="_blank"}
