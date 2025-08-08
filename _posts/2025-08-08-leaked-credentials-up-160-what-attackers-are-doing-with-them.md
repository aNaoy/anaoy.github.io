---
title: 'Leaked Credentials Up 160%: What Attackers Are Doing With Them'
date: 2025-08-08
permalink: /posts/2025/08/08/leaked-credentials-up-160-what-attackers-are-doing-with-them/
tags:
- veille-cyber
- hackernews
---
**L'Explosion des Identifiants Compromis : Une Menace Ouvertement Exploitable**

Une augmentation alarmante de 160% des identifiants d'entreprise compromis a été observée en 2025, surpassant le phishing et même l'exploitation logicielle comme principal vecteur d'attaques, représentant 22% des brèches selon le rapport 2025 de Verizon. Ces données, compilées par Cyberint (désormais Check Point), révèlent que l'automatisation et l'accessibilité facilitent le vol et l'exploitation de ces informations sensibles. Des logiciels malveillants de type "infostealer" et des campagnes de phishing générées par IA permettent aux attaquants de grande échelle de récolter des identifiants, qui sont ensuite vendus sur des marchés clandestins ou partagés sur des plateformes comme Telegram. Les identifiants compromis, une fois trouvés sur des dépôts comme GitHub, peuvent rester exploitables pendant une moyenne de 94 jours sans détection.

**Points Clés :**

*   **Augmentation massive :** 160% d'augmentation des identifiants d'entreprise compromis en 2025 par rapport à l'année précédente.
*   **Vecteur principal d'attaques :** Les identifiants compromis représentent 22% de toutes les brèches en 2024, dépassant d'autres méthodes.
*   **Automatisation et accessibilité :** Facilité accrue du vol grâce aux infostealers et aux campagnes de phishing IA.
*   **Marchés clandestins :** Les identifiants sont vendus ou échangés sur le dark web et des plateformes comme Telegram.
*   **Délai de remédiation :** Une moyenne de 94 jours pour corriger les identifiants exposés sur GitHub, laissant une fenêtre d'exploitation.
*   **Usage multiple :** Les identifiants compromis mènent à la prise de contrôle de compte (ATO), au credential stuffing, à la distribution de spam et au chantage.
*   **Dispositifs non surveillés :** 46% des appareils liés à des fuites d'identifiants d'entreprise n'étaient pas couverts par une surveillance des points d'extrémité.
*   **Avantage compétitif :** La détection proactive des expositions avant leur utilisation est cruciale.

**Vulnérabilités et Exploitations :**

*   **Credential Stuffing :** Exploitation de la réutilisation des mots de passe par les utilisateurs sur différents services.
*   **Account Takeover (ATO) :** Prise de contrôle de comptes pour envoyer des e-mails de phishing, modifier des données ou lancer des fraudes financières.
*   **Distribution de Spam et Botnets :** Utilisation de comptes compromis pour des campagnes de désinformation ou promotionnelles.
*   **Chantage et Extorsion :** Menace d'exposition des identifiants en échange d'une rançon.

Aucune CVE spécifique n'est mentionnée dans l'article, mais le problème sous-jacent est lié à la mauvaise gestion et à la fuite d'informations d'identification sensibles.

**Recommandations :**

*   **Politique de mots de passe forts :** Imposer des changements réguliers et interdire la réutilisation sur différentes plateformes.
*   **Authentification à deux facteurs (MFA) et SSO :** Ajouter des couches de sécurité au-delà du mot de passe.
*   **Limitation du débit (Rate Limiting) :** Définir des seuils pour les tentatives de connexion afin de contrer les attaques par force brute et "credential spraying".
*   **Principe du moindre privilège (PoLP) :** Limiter l'accès des utilisateurs au strict nécessaire.
*   **Sensibilisation au phishing :** Former les utilisateurs aux techniques d'ingénierie sociale.
*   **Surveillance de l'exposition :** Mettre en place une détection active sur les forums, les places de marché et les sites de partage pour identifier les identifiants d'entreprise compromis.
*   **Intégration avec SIEM et SOAR :** Permettre des réponses automatisées comme la révocation d'accès ou la réinitialisation de mots de passe.
*   **Détection proactive :** Prioriser la découverte d'identifiants compromis avant leur exploitation.

---
[Source](https://thehackernews.com/2025/08/leaked-credentials-up-160-what.html){:target="_blank"}
