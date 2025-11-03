---
title: 'Researchers Uncover BankBot-YNRK and DeliveryRAT Android Trojans Stealing Financial Data'
date: 2025-11-03
permalink: /posts/2025/11/03/researchers-uncover-bankbot-ynrk-and-deliveryrat-android-trojans-stealing-financial-data/
tags:
- veille-cyber
- hackernews
---
**Menaces Mobiles : BankBot-YNRK et DeliveryRAT Ciblent les Données Financières sur Android**

Deux familles de malwares Android, BankBot-YNRK et DeliveryRAT, ont été identifiées par des chercheurs en cybersécurité. Ces menaces visent à dérober des informations financières sensibles sur les appareils compromis.

BankBot-YNRK utilise des techniques avancées pour éviter la détection, notamment en vérifiant s'il s'exécute dans un environnement virtualisé ou émulé. Il cible spécifiquement certains fabricants et modèles d'appareils, comme Google Pixel et Samsung, et peut déguiser son nom et son icône pour ressembler à des applications légitimes, telles qu'une application gouvernementale indonésienne ou Google News. Le malware cherche à obtenir des permissions élevées via les services d'accessibilité, bien que cette méthode soit limitée sur Android 14 et versions ultérieures. Il est capable de collecter une large gamme de données, y compris les contacts, les SMS, la localisation, la liste des applications installées et le contenu du presse-papiers. Il peut également usurper l'interface d'applications bancaires pour dérober des identifiants et automatiser des transactions frauduleuses sur les portefeuilles de cryptomonnaies. La liste des applications financières ciblées comprend 62 applications.

DeliveryRAT, quant à lui, est proposé en tant que service (malware-as-a-service) via Telegram et cible principalement les utilisateurs d'appareils Android en Russie. Il se présente sous le déguisement d'applications de livraison de nourriture, de marketplaces, de services bancaires ou de suivi de colis. Une fois installé, il demande l'accès aux notifications et aux optimisations de batterie pour collecter discrètement des données sensibles et s'exécuter en arrière-plan. Il peut également accéder aux SMS et à l'historique des appels, masquer sa propre icône, et dans certaines variantes, mener des attaques par déni de service distribué (DDoS).

Il est à noter que ces découvertes surviennent alors que des rapports font état de plus de 760 applications Android utilisant la communication en champ proche (NFC) pour dérober des données de paiement et les transmettre à des acteurs malveillants, ciblant notamment des institutions financières russes, mais aussi brésiliennes, polonaises, tchèques et slovaques.

**Points Clés :**

*   Deux malwares Android, BankBot-YNRK et DeliveryRAT, ciblent les données financières.
*   Ils utilisent l'ingénierie sociale et l'usurpation d'identité pour tromper les utilisateurs.
*   Les services d'accessibilité sont exploités pour obtenir des permissions accrues (limitée sur Android 14+).
*   Collecte de données bancaires, d'identifiants, de SMS, de contacts, de localisation, et du contenu du presse-papiers.
*   Possibilité de réaliser des transactions frauduleuses et des attaques DDoS.
*   Une tendance émergente concerne l'exploitation de la technologie NFC pour le vol de données de paiement.

**Vulnérabilités exploitées :**

*   Les versions d'Android jusqu'à Android 13 sont vulnérables à l'exploitation des services d'accessibilité pour obtenir des permissions supplémentaires de manière automatique.
*   La confiance des utilisateurs dans les applications légitimes et l'utilisation de techniques d'ingénierie sociale pour distribuer les malwares.
*   L'exploitation de la fonction d'émulation de carte basée sur l'hôte (HCE) d'Android pour le vol de données NFC.

**Recommandations :**

*   Être vigilant face aux applications non officielles et vérifier la légitimité des applications téléchargées, particulièrement celles demandant des permissions inhabituelles.
*   Maintenir le système d'exploitation Android à jour pour bénéficier des correctifs de sécurité, notamment ceux d'Android 14 qui limitent l'exploitation des services d'accessibilité.
*   Désactiver les services d'accessibilité pour les applications non fiables.
*   Éviter de télécharger des applications depuis des sources non officielles ou de suivre des liens suspects reçus par messagerie.
*   Pour les transactions, privilégier les méthodes de paiement sécurisées et surveiller attentivement les relevés bancaires.
*   Se méfier des demandes d'informations personnelles ou financières par des canaux non sécurisés.

---
[Source](https://thehackernews.com/2025/11/researchers-uncover-bankbot-ynrk-and.html){:target="_blank"}
