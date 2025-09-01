---
title: 'Android Droppers Now Deliver SMS Stealers and Spyware, Not Just Banking Trojans'
date: 2025-09-01
permalink: /posts/2025/09/01/android-droppers-now-deliver-sms-stealers-and-spyware-not-just-banking-trojans/
tags:
- veille-cyber
- hackernews
---
**Droppers Android : Une Nouvelle Vague de Menaces Ciblent les SMS et l'Espionnage**

Les chercheurs en cybersécurité observent une évolution dans les campagnes malveillantes sur Android. Auparavant spécialisées dans la distribution de chevaux de Troie bancaires, les applications "droppers" (qui servent d'intermédiaires pour livrer d'autres malwares) diffusent désormais des logiciels plus simples mais tout aussi dangereux : des voleurs de SMS et des logiciels d'espionnage basiques. Ces campagnes utilisent des applications se faisant passer pour des services gouvernementaux ou bancaires, particulièrement en Inde et en Asie.

Cette mutation est une réponse directe aux nouvelles mesures de sécurité de Google, notamment un programme pilote visant à bloquer l'installation d'applications suspectes demandant des permissions sensibles comme l'accès aux SMS ou aux services d'accessibilité. Les opérateurs de ces malwares encapsulent donc des charges utiles plus simples dans des droppers pour contourner ces protections, tout en conservant la flexibilité de changer de cible ou de type de malware.

Une tactique consiste à présenter une fausse page de "mise à jour" qui trompe les systèmes de détection initiaux. Ce n'est qu'après l'interaction de l'utilisateur avec ce bouton que le véritable payload est téléchargé et sollicite les permissions nécessaires. Bien que Google Play Protect puisse alerter l'utilisateur, l'installation reste possible si celui-ci accepte malgré les avertissements, révélant ainsi une faille persistante.

**Points Clés :**

*   **Changement de stratégie des droppers Android :** Distribution de voleurs de SMS et d'espions à la place des chevaux de Troie bancaires.
*   **Ciblage géographique :** Principalement l'Inde et d'autres régions d'Asie.
*   **Motivations :** Contourner les nouvelles protections de Google et préparer de futures campagnes.
*   **Méthode :** Utilisation de fausses interfaces de mise à jour pour masquer le téléchargement du payload principal.
*   **Détection :** Google Play Protect peut être contourné si l'utilisateur confirme l'installation malgré les alertes.
*   **Exemples de droppers :** RewardDropMiner, SecuriDropper, Zombinder, BrokewellDropper, HiddenCatDropper, TiramisuDropper.
*   **Exemples d'applications compromises via RewardDropMiner (Inde) :** PM YOJANA 2025, RTO Challan, SBI Online, Axis Card.
*   **Campagnes associées :** Utilisation de publicités malveillantes sur Facebook pour distribuer le trojan bancaire Brokewell sous couvert d'applications de trading.

**Vulnérabilités (non spécifiées par CVE dans l'article) :**

*   La capacité des droppers à masquer leur véritable intention en se présentant comme des applications de mise à jour.
*   La permissivité du processus d'installation d'Android lorsque l'utilisateur ignore les alertes de sécurité.

**Recommandations (implicites) :**

*   **Prudence accrue des utilisateurs :** Ne pas télécharger d'applications depuis des sources non officielles et se méfier des applications demandant des permissions excessives.
*   **Vigilance face aux mises à jour :** Être sceptique quant aux pop-ups de mise à jour inattendus, surtout s'ils proviennent d'applications non sollicitées.
*   **Maintien de Google Play Protect actif :** S'assurer que Google Play Protect est activé et à jour pour bénéficier des dernières protections.
*   **Pour les développeurs et plateformes :** Continuer à renforcer les mécanismes de détection et de vérification des applications avant leur publication.

---
[Source](https://thehackernews.com/2025/09/android-droppers-now-deliver-sms.html){:target="_blank"}
